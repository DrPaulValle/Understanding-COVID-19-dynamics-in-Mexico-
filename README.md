[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=DrPaulValle/Understanding-COVID-19-dynamics-in-Mexico-)

# Understanding COVID-19 dynamics in Mexico through mathematical modelling, biostatistics and in silico experimentation
Nonlinear mathematical modelling of COVID-19 dynamics in Mexico and fitting to observed data by means of nonlinear regression.

Paul A. Valle, Yolocuauhtli Salazar, Corina Plata, Luis N. Coriaa

Tecnológico Nacional de México / IT Tijuana, Departamento de Ingeniería Eléctrica y Electrónica, Grupo de Investigación BioMath. Blvd. Alberto Limón Padilla s/n, Tijuana 22454, México. paul.valle@tectijuana.edu.mx, luis.coria@tectijuana.edu.mx, corina.plata@tectijuana.edu.mx
Tecnológico Nacional de México / IT Durango, Departamento de Ingeniería Eléctrica y Electrónica. Blvd. Felipe Pescador 1830 Ote., Durango 34080, México. ysalazar@itdurango.edu.mx  

The spread of the SARS-CoV-2 in Mexico began with four confirmed cases of Mexican citizens who had recently traveled to Italy in February 2020. Then, the virus rapidly began to spread within the country infecting a total of 7,633,355 people by June 2023 from which 6,885,378 patients fully recovered and 334,336 died from COVID-19 [1]. Since the begging of the pandemic, different types of mathematical and computational models have been applied with the aim of forecasting either the contagion curve [2,3] or the total amount of deaths of a specific region [4,5]. In this work, we aim to understand the COVID-19 pandemic dynamics in Mexico by reconstructing the typical SIRD model [6] as a time-variant system of four nonlinear Ordinary Differential Equations as shown below:

(1)  dS/dt = -ρ1S - I(ρ2S - ρ3t),

(2)  dI/dt = +ρ4S + I(ρ5S - ρ6t),

(3)  dR/dt = +ρ7I(R - ρ8)^2,

(4)  dD/dt = +ρ9I(D - ρ10)^2,

where S(t) represents the susceptible population in Mexico, i.e., those who have not been infected with the virus, I(t) denotes the confirmed infected individuals which may develop the disease as asymptomatic, moderate, severe or critical, R(t) identifies the fully recovered patients, whereas D(t) follows the accumulated number of deaths from COVID-19. We were able to successfully fit Equations (1)-(4) by nonlinear regression to the data provided by the Government of Mexico on COVID-19 from February 2020 to June 2023 [1]. The algorithm was designed in MATLAB with the fitnlm function from the Statistics and Machine Learning Toolbox. The statistical significance of the results was established by analyzing the Standard Error, the 95% Confidence Intervals, and the p-value. The goodness of fit was evaluated quantitively with the R-squared and the Akaike Information Criterion, and qualitatively by means of in silico experimentation. Our mathematical model can accurately approximate the accumulated populations of susceptible people, infected individuals, recovered patients, and deaths from COVID-19.

# References
[1] Gobierno de México (n.d.). COVID-19 México [Online]. Available in: https://datos.covid-19.conacyt.mx/
[2] Febres, Gerardo L., and Carlos Gershenson. "A Deterministic–Statistical Hybrid Forecast Model: The Future of the COVID-19 Contagious Process in Several Regions of Mexico." Systems 10.5 (2022): 138. https://doi.org/10.3390/systems10050138
[3] Wyss, Alejandra, and Arturo Hidalgo. "Modeling COVID-19 Using a Modified SVIR Compartmental Model and LSTM-Estimated Parameters." Mathematics 11.6 (2023): 1436. https://doi.org/10.3390/math11061436
[4] Pham, Hoang. "On estimating the number of deaths related to Covid-19." Mathematics 8.5 (2020): 655. https://doi.org/10.3390/math8050655 
[5] Perone, Gaetano. "Using the SARIMA model to forecast the fourth global wave of cumulative deaths from COVID-19: Evidence from 12 hard-hit big countries." Econometrics 10.2 (2022): 18. https://doi.org/10.3390/econometrics10020018
[6] F. Brauer, C. Castillo-Chavez and Z. Feng, Mathematical models in epidemiology. Vol. 32. New York: Springer, 2019.
