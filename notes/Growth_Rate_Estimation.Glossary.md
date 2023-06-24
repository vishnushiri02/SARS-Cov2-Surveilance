---
id: rfr63bef0sa84zpwv9fw1w0
title: Glossary
desc: >-
  This document contains the important terms and definitions that are used in
  the project
updated: 1687524865330
created: 1684497049640
---

# **Epidemiological Terms**

## **Reproduction Number**: 
  
  The number reflects the infectious potential of a disease

### **R<sub>0</sub>(Basic Reproduction Number)**:

The average number of secondary cases generated
by an average infected person throughout their infectious period in a wholly susceptible population - **_when the population is fully susceptible_**

![Importance of R0](./assets/images/Importance%20of%20R0.png)

      
### **R(Effective Reproduction Number)**: 

Number of secondary infections generated from a population consisting of both **_naïve/susceptible and exposed/immune individuals_** and therefore will always be less than R0.
- #### **Backward looking R**:

     
  R<sub>t</sub> estimated for the cases infected at the time of an intervention like lockdown. This is regarding the primary infection that cased the secondary infections which are currently prevailing when the intervention is introduced (takes pre intervention scenario into account)

- #### **Forward looking R**: 
  The infections that were prevailing at the time of introduction of intervention were considered as primary infection and the average number of secondary infections caused by these primary infections are taken as forward looking R. This is lower than the backward looking R as the consequence of the intervention.
  
  
[[Importance of Reproduction number | Growth_Rate_Estimation.SARS_Cov2_notes#importance-of-reproduction-number]].

## **Epidemic Growth rate**: 

  Represents the rate at which number of new infections arises.It can be either positive or negative. It is dependent on the reproduction number and timescale between infections $r = (R0-1)/Ƭ$. If R<sub>0</sub> is greater than 1 then there is an exponential growth rate. When R<sub>0</sub> < 1 the infection cannot be established in the population and dies out.
  [[Relationship between Generation time/ Serial interval, epidemic growth and Reproduction number|Growth_Rate_Estimation.SARS_Cov2_notes#relationship-between-generation-time-serial-interval-epidemic-growth-and-reproduction-number]]

## **Seropositives**: 
  Showing a significant level of serum antibodies, or other immunologic marker in the serum, indicating previous exposure to the infectious agent being tested.

## **Generation Time**:     
  The generation time, Ƭ, for an infectious disease is the time between **_infection_** events in an infector-infectee pair of individuals. 
  It can be used to derieve the speed of the spread.
  Measuring Generation time is challenging because it is unobserved. Hence is usually replaced with serial time.
  However, ignoring the difference between the serial interval and generation time can lead to biased estimates of R
  At this early stage the instantaneous r of the exponentially growing epidemic curve, is approximately given by $r = (R0-1)/Ƭ$
  
## **Serial interval:** 
  Serial intervals describe the average time between symptoms of infection in the primary infection to when the person he or she infects develops symptoms.
  It is easier to measure than
   the generation time as symptom onset is easier to identify through contact tracing studies than time of infection acquisition.
## **The doubling time of the epidemic:**
The number of days or time units which leads to a doubling in cases. The doubling time dt in the early stages is therefore: dt = ln(2)/r.
To give a simple example, the doubling times of cases in the UK in the rapid growth phase of the epidemic in March 2020 before 'lock down', was of the order of 3 to 4 days30. Taking a value of 3.5, this gives an r estimate of 0.2 per day.
The doubling time is useful only at the start of epidemic.
When the epidemic is in the decline stage halving time is used. It is the time required for the number of cases to halve and hence how rapidly or slowly the remaining cases will decline to eradication

## ** 20/80 rule:**

Defines that in many cases 80% of the transmission results from 20% of the infected in any one generation of infection spread.

## **Viral fitness:**
The capacity of a virus (a serotype, clade, or variant) to become dominant in the field, relative to other serotypes, clades, or variants of the same virus has been defined as epidemiologic fitness 
![viral_fitness](assets/images/viral_fitness.png)

[viral_fitness_reference](https://doi.org/10.1016/j.coviro.2012.07.007)

## **Incidence vs Prevalence:**
Prevalence differs from incidence in that prevalence includes all cases, both new and preexisting, in the population at the specified time, whereas incidence is limited to new cases only<br>
Prevelance is calculated as:
$$$
Prevalance = \cfrac{Number of cases}{total population}
$$$
Incidence is calculated as:
$$$
Incidence = \cfrac{Newcases}{total population}
$$$


## **Cumulative Incidence:**
Cumulative incidence is the proportion of a population at risk that develops the outcome of interest over a specified time period.

## **Virus epidemiological fitness:**
Quantification of epidemiologic fitness is based largely on observational data and examines changes in distribution, prevalence, and composition of viral genotypes over time to infer their relative fitness.

## **CUB(codon usage biases):**

Synonymous codons are codons that encode for the same amino acid. Despite that, synonymous codons are generally used at different frequencies. This phenomenon can be seen in most genes and organisms, and it is called codon usage bias (CUB).

## **Risk model:**

A risk model is a statistical procedure for assigning to an individual a probability of developing a future adverse outcome in a given time period. The assignment is made by combining his or her values for a set of risk-determining covariates with incidence and mortality data and published estimates of the covariates’ effects on the outcome.[2]

[1]: <https://sphweb.bumc.bu.edu/otlt/MPH-Modules/PH717-QuantCore/PH717-Module3-Frequency-Association/PH717-Module3-Frequency-Association4.html#:~:text=Cumulative%20Incidence%20Versus%20Incidence%20Rate,-There%20are%20two&text=Cumulative%20incidence%20is%20the%20proportion,%22%20(person%2Dtime)>

[2]: <Whittemore AS. Evaluating health risk models. Stat Med. 2010 Oct 15;29(23):2438-52. doi: 10.1002/sim.3991. PMID: 20623821; PMCID: PMC2990501>