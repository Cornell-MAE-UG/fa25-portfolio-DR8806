---
layout: project
title: E-Bus Mathematical Model
description: Optimization of Electric Bus Purchases by Metropolitian Cities
technologies: [MATLAB, R]
image: /assets/
---

## Summary

For the 2023 High School Mathematical Contest in Modeling, my team’s finalist-winning paper placed in the top 6% of 967 global submissions. I co-developed a comprehensive optimization model to guide the transition from diesel to battery electric bus (BEB) fleets in major U.S. metropolitan areas. Using MATLAB and R scripts, I integrated environmental data, public GTFS transit datasets, and economic cost structures to build a Lagrange Multiplier-based constrained optimization framework that minimized total electrification costs while meeting route energy demands. I applied this model to Boston, Detroit, and Philadelphia, using real transit data to determine the optimal combination and placement of BEBs and active chargers, supported by quadratic regressions linking stop frequency and charging demand. The project synthesized technical, financial, and ecological dimensions to quantify CO₂ reduction, noise abatement, and 10-year cost projections, producing actionable, data-driven electrification plans for sustainable urban transit development.

## Paper Submission

<iframe 
    src="https://cornell-mae-ug.github.io/fa25-portfolio-DR8806/assets/math-modeling-papers/HiMCM2023_E_Bus_Paper.pdf" 
    width="100%" 
    height="600px" 
    style="border:none;">
</iframe>

### Code Sample

```matlab

    C_a = -8.091*10^(-3); %degree 2 coeff of number of visits;
    C_b = 7.089*10^1; %degree 1 coeff of number of visits
    C_c = 6.959*10^3; %intercept of number of visit
    c = 45132.27 - (29100+ 0.8903*(C_a*x(1)^2+C_b*x(1)+C_c)+x(2)*125*0.8);
    % new one
    c = 45132.27 - (29100+ 0.2968*(C_a*x(1)^2+C_b*x(1)+C_c)+x(2)*125*0.8);

    %% Constants for Energy Constraint Equation
    b0   = 291;       % Number of buses
    c1   = 351;       % Battery capacity in kWh
    c2   = 150;       % Energy draw from active charger in kW
    t    = 0.00277778 * 2;  % Time at active charger in hours (2 minutes)
    c3   = 125;       % Range of bus in miles on a full charge
    DOD  = 0.8;       % Depth of Discharge parameter
    DOD_a = 25.3;
    DOD_b = 1.41;     % Exponent so DOD_a * DOD^(-b)
    O_c  = 10;        % Ownership cost period in years

    %% Load data
    Diesel_distance = readtable("/MATLAB Drive/Lagrange/Detroit/DDOTbuscyclesdf.csv");
    grouphours      = readtable("/MATLAB Drive/Lagrange/Detroit/DDOTgrouphours.csv");

    %% Constants for Price Optimization Equation
    c4  = 824400;   % Bus purchase price in $
    c5  = 495636;   % Purchase price of one active charger in $
    c6  = 50000;    % Purchase price of depot (plug-in) charger in $
    c7  = 202811;   % Installation cost of active charger in $
    c8  = 17050;    % Installation cost of depot charger in $
    % c9 = 0.64 * D * 365;   % Bus maintenance cost in $/year (commented out example)
    c10 = 18000;    % Active charger maintenance cost per year in $
    c11 = 0;        % Depot charger maintenance cost per year in $
    % c12 = battery price (not yet defined)
    c13 = 12;       % Battery claimed lifespan in years

    %% Compute hour-based costs
    hours_degree2 = c2 * t * (0.0468 * grouphours.C(1,:) + ...
                               0.0357 * grouphours.C(2,:) + ...
                               0.1652 * grouphours.C(3,:)) * 365 * O_c;

    hours_degree1 = c2 * t * (0.0468 * grouphours.B(1,:) + ...
                               0.0357 * grouphours.B(2,:) + ...
                               0.1652 * grouphours.B(3,:)) * 365 * O_c;

    hours_intercept = c2 * t * (0.0468 * grouphours.A(1,:) + ...
                                 0.0357 * grouphours.A(2,:) + ...
                                 0.1652 * grouphours.A(3,:)) * 365 * O_c;

    %% Define aggregated cost-terms
    G1 = hours_degree2;
    G2 = c5 + c7 + c10 * O_c + hours_degree1;
    G3 = c4 + 0.64 * 50 * 365 * O_c;  % 50 is an example miles/day
    G4 = (c4 + 0.64 * 50 * 365 * O_c + c6 + c8 + c11 * O_c) * b0 + hours_intercept;

    %% Objective function for optimization
    price = @(x) ( G1 .* x(1).^2 + G2 .* x(1) + G3 .* x(2) + G4 );

    %% Initial guess and bounds
    x0 = [50, 0];       % Initial guess [numberActiveChargers, numberBuses?]
    lb = [0, 0];        % Lower bounds
    ub = [];            % No upper bounds specified

    %% Run optimization
    [x_op, fval, exitflag, output, lambda, grad, hessian] = ...
        fmincon(price, x0, [], [], [], [], lb, ub, 'distancenonlinconDetroit');

    %% Output optimal price
    optimalPrice = price(x_op)
end
