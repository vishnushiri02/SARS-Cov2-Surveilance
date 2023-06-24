---
id: ikm1x970zyg0cc0u4ewttsk
title: GerstungLab
desc: 'Notes regarding the GerstungLa paper - SARS-CoV-2 England surveilance '
updated: 1687526948974
created: 1686831170884
---
## Pillar 2 SARS-CiV-2 data:
Pubilcally available SARS-CoV-2 test result data ![pillar2_example](assets/images/Pillar2_data_example.png). It is the number of positive cases grouped by specimen date.
## Surveillance sequencing:
Samples go throught amplicon sequencing protocol and lineage assignments were made using Pangolin.
## About the model
  ### Spatiotemporal genomic surveillance model:
  - Hierarchical Bayesian model - fit incidence data in a day and estimate the relative historical prevelance and transmission parameters <br>
_Following is my derivation of the solution of ODE_
$$$
x'(t)=(\vec{b}+r_0(t))*x(t)\\
\lmoustache dx/x(t)=\lmoustache (\vec{b}+r_0(t))\\
ln(x(t)) + const = \vec{b}t+const+\lmoustache r_0(t)dt\\
x(t)=e^{(\vec{b}t+const+\lmoustache r_0(t)dt)}\\
x(t)=e^{(\vec{b}t+const+v(t))} ; v(t) = e^{r_0(t)dt}\\
$$$
Relative proportions of lineages or lineage prevelance :
$$$
p(t)=\cfrac{x(t)}{\sum x(t)} \propto e^{const+\vec{b}t}\\
$$$
Total incidence factorizes into : 
$$$
\mu (t)=v(t) \sum e^{c+\vec{b}t}
$$$
v(t) contributes asame factor to each of the lineage since r<sub>0</sub> is lineage independent. <br>
p(t) :- Lineage [[Prevalence|Growth_Rate_Estimation.Glossary#incidence-vs-prevalence]]<br>
r<sub>0</sub>(t) : scalar time dependent logistic [[Growth rate|Growth_Rate_Estimation.Glossary#epidemic-growth-rate]]. This r<sub>0</sub> reflects lineage  independent transmission determenents. The lineages will differ only by the transmission intensity which I assume as the [[Reproduction Number|Growth_Rate_Estimation.Glossary#reproduction-number]]

P(t) being the lineage prevelance follows a logistic linear trajectory

## Incidence

- Let $\mu(t)$ be the expected daily number of positive pillar 2 test
- s is the population size in each LTLA(Lower Tier Local Authority)
- $\lambda(t)=log\mu (t)-log(s)$ :- logrithimic daily incidence per capita at time t



  