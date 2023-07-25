---
id: yzhnqpppxy0sf7yapgxvbjw
title: Growth_Rate_Estimation
desc: >-
  This note is the overall Reference document that is needed throughout this
  project
updated: 1691505922590
created: 1684496674975
---
# Existing methods to model the growth rate

|Sno|Model | Description | Name of the microorganism | Reference | Data Used | Notes|
|---|------|-------|------------|------|-------|------|
|1|1. Genomic Surveilance model <br> 2. Hierarchical Bayesian statistical model <br> 3.multivariate logistic regression model  | 1. Subset of 600,000 viral sample sequances were used to characterize the [[Epidemic Growth rate \|Growth_Rate_Estimation.Glossary#epidemic-growth-rate]] and geographical spread of different SARS CoV-2 lineages <br> 2. The model also calculates total and lineage-specific local incidences and time-dependent growth rates and approximate reproduction numbers R<sub>t</sub> by negative binomial spline fitting of the number of daily positive PCR tests|SARS CoV-2|[Vöhringer, H.S., et al. Genomic reconstruction of the SARS-CoV-2 epidemic in England. Nature 600, 506–511 (2021). ](https://doi.org/10.1038/s41586-021-04069-y)| Positive case data along with the sequences | 1. The effect of immunity is currently not modelled - this can have impact on the spread of a particular lineage.<br> 2. Stochastic growth events are not fully accounted so the estimated growth rate will not reflect viral tranmissibility<br> 3. In its current form, the model accounts for only a single introduction event per LTLA <br> 4. The modelled curves are smoothed over intervals of approximately 7 d.|
|2|1. Simple exponential Growth model <br> 2. Poisson likelihood framework is adopted for data fitting <br>  | R package _EpiEstim_ used to calculate the instatntaneous effective reproductive number of 12 African countries in order to show the potential of COVID-19 to spread across the region.|SARS CoV-2|[Musa, S.S., et al. Estimation of exponential growth rate and basic reproduction number of the coronavirus disease 2019 (COVID-19) in Africa. Infect Dis Poverty 9, 96 (2020).](https://doi.org/10.1186/s40249-020-00718-y)|1.Daily number of Covid-cases - time series data.<br>|1.Estimation for the early stages of the pandemic <br> 2. R<sub>0</sub> is also computed. <br> 3. SI that was used is from the estimates based on cases obtained in china|
|3|stochastic SHARUCD-type model—an extension of the well known simple SIR model| 1. The model is used to estimate the [[Effective Reproduction Number\|Growth_Rate_Estimation.Glossary#reffective-reproduction-number]] and momentary growth rates for hospital data.<br> 2. The collected total number of positive cases were categorised into hospital admissions, ICU admissions, recovered, deceased. These categorised data are used in the SEIR model - infected class partitioned into severe infections prone to hospitalization (H) and mild, sub-clinical or asymptomatic infections (A). For severe infections prone to hospitalization, we assume that individuals could either recover R, be admitted to the ICU facilities U or or eventually deceased into class D.| SARS CoV-2| [Aguiar, et al. "Reproduction ratio and growth rates: Measures for an unfolding pandemic." PLoS One 15.7 (2020): e0236620.](https://doi.org/10.1371/journal.pone.0236620)| Number of positive cases | The data is collected from March 4 2020 to May 9 2020. The frequency at which the data is collected is not known. The model is parameterised using the initial pandemic data.|
|4|Exponential growth model  |Estimation of the transmissibility of 2019-nCoV via the basic reproduction number, R<sub>0</sub>, based on the limited data in the early phase of the outbreak. R<sub>0</sub> is obtained using the estimated intrinsic growth rate.|SARS Cov-2|[Zhao, Shi, et al. "Preliminary estimation of the basic reproduction number of novel coronavirus (2019-nCoV) in China, from 2019 to 2020: A data-driven analysis in the early phase of the outbreak." International journal of infectious diseases 92 (2020): 214-217.](https://doi.org/10.1016/j.ijid.2020.01.050)| Positive test time series data|1. Non linear least square was used for data fitting and parameter estimation<br> 2.SI information from SARS and MERS, which share a similar pathogen as 2019-nCoV were used.|
|5|1.Smoothing splines are a quick method to estimate maximum growth <br> 2. Classsical logistic growth model written as analytical solution of the differential equation |Growthrates package of R aims to streamline estimation of growth rates from direct or indirect measures of population density (e.g. cell counts, optical density or fluorescence) determined in batch experiments or field observations | different species of bacteria, archaea, protists, and metazoa | [Estimation of Growth Rates with Package growthrates, Part 1: Introduction Thomas Petzoldt](https://cran.r-project.org/web/packages/growthrates/vignettes/Introduction.html)| 1. Concentration <br> 2. time <br> 3. value of the indirect measure.| 1.Nonlinear fitting of parametric growth models like the logistic or the Gompertz growth model. Parametric model fitting is done by using package FME (Flexible Modelling Environment) of Soetaert and Petzoldt (2010). In addition to growth models given in closed form (i.e. empirical regression equations or analytical solutions of differential equations) it is also possible to use numerically integrated systems of differential equation. Such models are then solved with package `deSolve’ (Soetaert, Petzoldt, and Setzer 2010).<br> 2. Fitting of linear models to the period of exponential growth using the ``growth rates made easy method’’ of Hall et al. (2014) , <br>3. Nonparametric growthrate estimation by using smoothers. R contains several powerful smoothing methods, that can leveraged for this purpose. The currently implemented method uses function smooth.spline, similar to the package grofit (Kahm et al. 2010).| 
|6| 1. Target cell limited model <br> 2. mixed effects model| 1. The study aims to estimate reproduction number and growth/expansion rate at the early pathogenesis of HIV -1 infection. For this purpose samples from already HIV-1 infected persons are not considered for the study <br> 2. In the context of host viral dynamics, R0 is a measure of whether a virus can establish infection. It specifically measures how many cells a single infected cell will infect when there is no target cell limitation.  | HIV-1 | [Ribeiro, Ruy M et al. “Estimation of the initial viral growth rate and basic reproductive number during acute HIV-1 infection.” Journal of virology vol. 84,12 (2010): 6096-102.](https://doi.org/10.1128/JVI.00127-10)|HIV viral load data from the plasma of 51 donors. The data seems to be collected 10 times with an interval for each sample| 1. The time of infection for the sample collected is not known which is the t<sub>0</sub>. The work arbitarily defines the time of origin as as the time that the subject’s viral load first reached the limit of detection, 50 cp/ml, and call it t<sub>50</sub>. <br> 2. Linear mixed effects model is used for estimating the expansion rate|
|7|1. Exponential growth model <br> 2. Polynomial growth model|The study aims to analyse the growth pattern of Ebola virus disease epidemic in different spatial scales  (regional, national, and subnational) in western Africa.<br> 3. The growth trend in the regional endemics followed a polynomial exponenetial function. | Ebola Virus|[Chowell, Gerardo et al. “The Western Africa ebola virus disease epidemic exhibits both global exponential and local polynomial growth rates.” PLoS currents vol. 7 ecurrents.outbreaks.8b55f4bad99ac5c5db3663e916803261. 21 Jan. 2015.](https://doi.org/10.1371%2Fcurrents.outbreaks.8b55f4bad99ac5c5db3663e916803261)|Weekly time series  of reported Ebola virus disease case numbers.| The local data was first plotted on the semi-logrithamic scale. Exponential growth is evident if a straight line fits well several consecutive disease generations of the epidemic curve, whereas a strong curvature in semi-logarithmic scale would be indicative of sub-exponential growth and a straight line fitted to the square-root transformed epidemic curve would be indicative of quadratic polynomial growth.|
|8|[[Risk model\|Growth_Rate_Estimation.Glossary#risk-model]]| 1. The study aims to develop a mathematical model to explain the cubic growth of AIDS and apply it in the homosexual population <br> 2. The risk-based model builds on the fact that the amount of 'risky' behaviour is not distributed equally among the population. It also assumes that the people with similar risk behaviour tend to primarly interact among themselves (biased mixing) rather than equally with others(homogenous mixing), finally the model incroporates the epidemologic data on the progression from initial HIV infection to AIDS. | HIV-AIDS|[Colgate, S A et al. “Risk behavior-based model of the cubic growth of acquired immunodeficiency syndrome in the United States.” Proceedings of the National Academy of Sciences of the United States of America vol. 86,12 (1989): 4793-7.](https://doi.org/10.1073/pnas.86.12.4793)||1. Homogenous mixing is assumed<br> 2. study assumes that the risk behaviour is distributed.<br> 3. Risk behaviour - New partner Rate and frequency of sexual contact.  |
|9|  Emprical model | Development of improved maximal growth rate estimator and prediction of maximal growth rates from over 200,000 genomes, metagenome assembled genomes, and single-cell amplified genomes to survey growth potential across the range of prokaryotic diversity|Prokaryotic organisms|[Weissman, Jake L., Shengwei Hou, and Jed A. Fuhrman. "Estimating maximal microbial growth rates from cultures, metagenomes, and single cells via codon usage patterns." Proceedings of the National Academy of Sciences 118.12 (2021): e2016810118.](https://doi.org/10.1073/pnas.201681011)|1. Growth rate of species listed in the original Vieira-Silva and Rocha dataset.<br> 2. All complete genomwe assenblies from RefSeq |The implementation is provided in an R package called **gRodon**|



# General Growth Rate models


## Exponential

$$
x(t) = x_0e^rt
$$

x<sub>0</sub> - Initial value <br> r - growth rate

## Logistic 
c(t) is assumed to satisfy the following equation: <br>
 $$
 c'(t) = rc(t)[1 - \frac{c(t)}{K}] 
 $$
 <br> This equation has an explicit solution: <br>  
 $$
 c(t)= K/{1+[(K/c_0)-1]e^{-rt})}  
 $$
  c(t) - expected cumulative cases <br> K - final size of the epidemic which c(t) approches

## Richards
c(t) in Richards satisfies <br>
$$
 c'(t) = r c(t) \biggl[1- \biggl(\frac{c(t)}{K} \biggr)^a \biggr] 
 $$
 which has solution : <br>  

$$ 
c(t) = \frac{K}{ ( 1+ [(K/c_0)^a-1 )\exp\{ -r_0t/[1-(c_0/K)^a]\} )^{1/a}} 
$$

## Delayed Logistics

While Logistic model is used to describe the cumulative incidence, this model is used to model the cumulative death

$$
d(t) = \int_0^t c_{{}_{\rm Log}}(s)e^{-m(t-s)}\,ds 
$$

- where c<sub>Log</sub>(t) is the solution to the logistic model
- m is the rate of delay that is exponenetially distributed.

*__In Logistic, Richards, Delayed Logistics the interval incidence is obtained by differencing cumulative expressions __*
$$
x(t) = c(t + \Delta t)-c(t)
$$
*_where c(t) is cumulative incidence, and x(t) is interval incidence (typically daily or weekly)._* [1]
## SEIR model (phenomenological model)

# References
[1]: <https://doi.org/10.1007/s11538-013-9918-2>


