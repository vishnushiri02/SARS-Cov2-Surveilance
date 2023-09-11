---
id: v1jffnk3ktk5mbx8jpgx53v
title: Wallinga_Lipsitch
desc: 'This note contains description of the method described in the paper'
updated: 1694333360302
created: 1694262461882
---

## Motivation of the paper

1. Observed r can be related to reproduction number : $R=1+rT_c$; Where $T_c$ is mean generation time. This is not the only expression there are many expressions that relate growth rate and reproductive number and each equation would result in a different estimate of reproduction number. Hence it is important to know which equation can be used for inferring reproductive number from the observed growth rate.
2. [[Eurler lotka equation|Growth_Rate_Estimation.Glossary#eurler-lotka-equation]] is used as a start point  to examine the relationship between reproductive number and observed change in the number of cases.
   
## Deriving the Lotka-euler equation:
1. This derivation is made on the assumption regarding human population (demographical and not epidemiological).
2. Resent time is denoted as t=0, past time is denoted by negative number and future is represented using positive number. 
3. It is assumed that the population would displays exponential growth at a fixed growth rate and the age distribution of the population would not change over time.
4. The equation is based on  two concepts - to get the total number of births in the year t.
5. First : The sum of number of children born to mothers of all age at time t gives the birth at that time.
6. second : The number of births to mothers of age a at time t is equal to the number of births at time t-a (the number of mothers, including those who have not survived) multiplied by the expected number of offspring per year for mothers of age a(simce time is involved we can call it  rate). Summing this over all possible mother's age at time t (first concept) gives the total number of births in the year t.
7. $b(t)= \int_{a=0}^\infin b(t-a)n(a)da$ where b(t) is the birth rate of population at time t, n(a) rate of production of **female** offspring by a mother at age a. n9a) includes the fraction of individuals surviving at age a l(a) and the birth rate for mothers of age a m(a). n(a)=l(a)m(a)
8. Since the population is growing exponentially, the rate can be given as  [[Exponential Function |Growth_Rate_Estimation.Glossary#exponential-function-and-e-eulers-number]]. The number of births at given time t is given as $b(t)=b(t-a)e^{ra}$ number of births at time t-a multiplied by the exponential growth rate $e^{ra}$. So combining the two equations $b(t)=\int_{a=0}^\infin b(t)e^{-ra}n(a)da$ cancelling b(t) on both the sudes we get 
   $1=\int_{a=0}^\infin b(t)e^{-ra}l(a)m(a)da$

## A moment generating function expression for the reproductive number R
1. It is seen that n(a) gives the rate of production of female offspring by a mother of age a. Integrating n(a) for the total lifespan gives the total number of female offspring produced by the mother over her lifespan. $\R=\int_0^\infin n(a)da$.
2. Normalising the rate $\frac{n(a)}{\int_0^\infin n(a)da}=\frac{n(a)}{R}=g(a)$ g(a) is the normalised rate distribution. If age is considered as the time since infection g(a) can be said as the probability distribution of the generation time. The equation can be rewriten as $\frac{1}{R}=\int_{a=0}^\infin e^{-ra}g(a)da$
3. 