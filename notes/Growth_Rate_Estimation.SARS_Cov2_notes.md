---
id: dm29gl6lytt8sj0b96z6pg8
title: SARS_Cov2_notes
desc: This scratchpad contains vatious notes
updated: 1691505975483
created: 1684740753208
---

## **Facts on SARS-CoV2:**

- The SARS-CoV-2 virus accumulates approximately 24 point muta- tions per year, or 0.3 mutations per viral generation [3]

## ** Factors to consider when modelling the epidemiology of SARS Cov2 **:

   - Asymptomatic insdividuals - who may or may not be infectious to others
    - Pre-symptomatic infectious period
    -  Impact of partial or full (‘lock down’) isolation 
    -  known unknown’ is the duration of immunity post recovery
    -  it is not clear if those reinfected are again infectious to others or exhibit symptoms of infection that result in measurable morbidity
    - ‘unknown unknowns’ (meaning unmeasured parameters and unknown pathways of infection, transmission and disease [1]


## ** Importance of Reproduction Number:**

[[Reproduction Number:|Growth_Rate_Estimation.Glossary#reproduction-number]]

  - R<sub>0</sub> and R<sub>t</sub> are important measure of the progression of an epidemic
  - It is used for the policy formulation.
  - The value of R matters – not just whether it is greater or less than 1 – but because the value of R when greater than unity tells you what proportion of new infections you need to prevent in order to go from increasing incidence to stable or decreasing incidence.
  - In addition, the magnitude of R<sub>0</sub> [[(Basic Reproduction Number):|Growth_Rate_Estimation.Glossary#r0basic-reproduction-number]] also provides information on what level of herd immunity will drive the value of R to less than unity such that the infection cannot persist.
  - This gives the target for vaccination programmes of what fraction of the community to immunise. As a rough approximation, the expression p=1-1/R<sub>0</sub> gives the critical proportion (or percentage) p that must be immune if transmission is to be halted. For a value of 2.5 as recorded in Wuhan in the early stages of the epidemic, this critical proportion is 0.6 or 60%. That is : 1 primary infection causes 2.5 secondary infections. So 1/2.5 primary infection causes 1 secondary infection. So to get a 1 as secondary infection there must be only 1/2.5 primary infection which means 1-1/2.5 should be immunised which is 60%.[1]
  
## **Dynamics of Serial/Generation interval**

[[Generation Time|Growth_Rate_Estimation.Glossary#generation-time]]

[[Serial interval|Growth_Rate_Estimation.Glossary#serial-interval]]



 - Serial interval in the case of COVID-19 has less relevance given that many infections especially in the young do not seem to generate marked
    and easily identifiable symptoms.
  
  - The interventions that are put into places will affect the dynamics of both serial interval and generation time.
    1. shorter generation times early in the epidemic,
  and longer ones as the epidemic is declining
    2. For a highly variable incubation period there may be negative serial intervals, which may
    be misinterpreted as the wrong direction of transmission.If the wrong direction of transmission is assumed, contact tracing efforts may stop prematurely and miss new infections that then may lead to further uncontrolled transmission events.[1]

## **Relationship between Generation time/ Serial interval, epidemic growth and Reproduction number**



       r = (R0-1)/Ƭ 

  To explain the relationship between R and time an comparison is provided by HIV, which has an R<sub>0</sub> of around 2 in some populations, and influenza, which has an R<sub>0</sub> around 1.329, the most important being the reproduction number R, but the timescale from one infection to the next is days for influenza but months or years for HIV.[1]

  [[Epidemic Growth rate|Growth_Rate_Estimation.Glossary#epidemic-growth-rate]]

  ## **Using Epidemic growthrate**

  Epidemic growth rate is a measure of the speed of epidemic growth, conveying information about the time scale of disease spread. In contrast, R<sub>0</sub>is a pure number with no associated time scale; epidemics with the same R<sub>0</sub>
 can occur over vastly different time periods, ranging from days to years. Knowing the epidemic time frame can be critical for selection of disease control strategies. Secondly, r itself is independent of potentially uncertain knowledge about the generation interval distribution, and thus may be useful in comparing the severity of disease epidemics.[2]
  Epidemic growth rate r itself can only be directly measured providing case reporting, hospital admissions, recorded deaths due to COVID-19 or serological data.
  but when the main source
 of data is deaths other information is required such as the probability distribution of times from infection to death
 and the fraction who die from infection.[1]
  
  
  
<!--References-->
  [1]: <./assets/Reference%20literature/set-covid-19-R-estimates.pdf> 
  [2]: <https://doi.org/10.1007/s11538-013-9918-2>
  [3]: <https://doi.org/10.1038/s41586-021-04069-y>

  
  

