[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=DrPaulValle/Understanding-COVID-19-dynamics-in-Mexico-)

# Reconstructing the SIRD System to Model the Dynamics of COVID-19 in Mexico
Nonlinear mathematical modelling of COVID-19 dynamics in Mexico and fitting to observed data by means of nonlinear regression.

Paul A. Valle, Luis N. Coria, Corina Plata-Ante and Yolocuauhtli Salazar

1 Postgraduate Program in Engineering Sciences, BioMath Research Group, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana 22454, Mexico; paul.valle@tectijuana.edu.mx (P.A.V.); luis.coria@tectijuana.edu.mx (L.N.C.)
2 Basic Sciences Department, BioMath Research Group, Tecnológico Nacional de México/IT Tijuana, Calzada del Tecnológico 12950 esquina Castillo de Chapultepec y calle Cuauhtemotzin, Tijuana 22414, Mexico; corina.plata@tectijuana.edu.mx (C.P.A.)
3 Postgraduate Program in Engineering, Tecnológico Nacional de México/IT Durango, Blvd. Felipe Pescador 1830 Ote., Durango 34080, Mexico; ysalazar@itdurango.edu.mx (Y.S.)
* Correspondence: luis.coria@tectijuana.edu.mx, paul.valle@tectijuana.edu.mx

# Abstract
The spread of SARS-CoV-2 in Mexico began with four confirmed cases of Mexican citizens who had recently traveled to Italy in February 2020. Subsequently, the virus spread rapidly within the country, ultimately infecting a total of 7,633,355 individuals by June 2023. Among these cases, 6,885,378 patients fully recovered, while 334,336 succumbed to COVID-19. Since the beginning of the pandemic, various mathematical and computational models have been applied to forecast either the contagion curve or the total number of deaths in specific regions. In this study, we aim to analyze the dynamics of the COVID-19 pandemic in Mexico by reconstructing the classical SIRD model as a time-variant system of four nonlinear ordinary differential equations. Using nonlinear regression, we successfully fit our model to data provided by the Government of Mexico, covering the period from February 2020 to June 2023. The statistical significance of the results was assessed through the standard error, 95 \% confidence intervals, and p-values. The goodness of fit was evaluated quantitatively using the R-squared statistic and the Akaike Information Criterion. The model is qualitatively validated through in silico experimentation. The proposed mathematical model effectively approximates the cumulative populations of susceptible individuals, infected individuals, recovered patients, and deaths attributed to COVID-19.
Keywords: COVID-19; In silico; Mathematical modeling; Nonlinear regression; SIRD model; Time-varying dynamical system.

# Time-variant SIRD Mathematical Model
In general, the purpose of mathematical modeling is to capture the essential characteristics of a real-world phenomenon, enabling both its interpretation and the formulation of predictive scenarios. In this context, and with the goal of understanding the dynamics of the COVID-19 pandemic in the Mexican population, we propose a SIRD-type model. This formulation is inspired by the frameworks presented in [5] and [6]. The model is described by the following system of four first-order, nonlinear, and time-dependent Ordinary Differential Equations (ODEs), which reflect the interactions among the susceptible, infected, recovered, and deceased populations over time:

(1)  dS/dt = -ρ1S - I(ρ2S - ρ3t),

(2)  dI/dt = +ρ4S + I(ρ5S - ρ6t),

(3)  dR/dt = +ρ7I(R - ρ8)^2,

(4)  dD/dt = +ρ9I(D - ρ10)^2,

where the state-variable S(t) represents the susceptible Mexican population, I(t) the cumulative Infected individuals, R(t) the Recovered population, and D(t) the cumulative Deaths caused by the SARS-CoV-2.

# References
[1] Gobierno de México. COVID-19 México. https://datos.covid-19.conacyt.mx/, 2023.

[2] Gobierno de México. Todo sobre el COVID-19. https://coronavirus.gob.mx, 2025. 401

[3] Secretaría de Salud México. Conferencia de Prensa: COVID19. https://www.youtube.com/channel/UCu2Uc7YeJmE9mvGG9OK-zbQ/videos, 2025.

[4] Centers for Disease Control Prevention. How COVID-19 spreads. https://www.cdc.gov/coronavirus/2019-ncov/prevent-getting-sick/how-covid-spreads.html, 2024.

[5] Brauer, F.; Castillo-Chavez, C.; Feng, Z.; et al. Mathematical models in epidemiology; Vol. 32, Springer, 2019. https://doi.org/10.100 4337/978-1-4939-9828-9.

[6] UCLA Life Science Course. Modelling the Spread of COVID-19. https://modelinginbiology.github.io/Epidemic-modeling-interactive-simulations, 2020.

[7] Motulsky, H. Intuitive biostatistics: a nonmathematical guide to statistical thinking; Oxford University Press, USA, 2014.

[8] MathWorks. fitnlm: Fit nonlinear regression model. https://www.mathworks.com/help/stats/fitnlm.html, 2025.
