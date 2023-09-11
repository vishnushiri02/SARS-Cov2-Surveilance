---
id: ttnshslislmgscwlukibhh5
title: R_packages
desc: 'This note delas with the R packages that employs the method mentioned in the parent note'
updated: 1694406236657
created: 1694342177084
---
## R_0 package
[Manual](https://cran.r-project.org/web/packages/R0/R0.pdf)

### Functions/ commands that are being used in the package

#### **check.incid**

This function is called internally by the estimation methods make the input incidence and dates data comatible to estimation methods.

   1. Takes in incidence object(vector/list) and vector of   dates or the start date and the size of the time step.
   2. Returns incidence and the dates in as double. 
   3. Incidence data should not contain negative or missing values.
   4. Incidence data and time vector should have the same length.

#### **est.GT**

1. Finding best fitting GT distribution for the given serial interval.
2. Serial interval is either provided as time lag between infector infectee pair. Or as two vectors one describing the date of onset of symptom onset in infector and the other is the date of symptom onset in infectee.
3. This function returns the name of the best fitting distribution along with the parameters like mean and sd.
4. It also return mean and sd of the descritized GT along with I assume few data point in the discritized distribtuion.

### **est.R0.AR**

1. Estimates the Reproduction number based on the attack rate alone (Initial proportion of the population considered susceptible has a default value of 1)
 2. Estimates is also done using population size and the incident cases - either given as a vector or a total count.
3. If Population size is given the confidence intervals are computed.

### **est.R0.EG

1. This function needs the epidemic curve data, generation time distribution, begin and end time of the computation. 
2. An argument reg.met which is in default poisson is used to fit the incidence rate data (epidemic curve) and estimate r.

### **est.R0.ML**

1. Needs the input of epidemic curve, Generation time distribution, range in which the maximum should be looked for. 
2.  If the generation time distribution is not known agrument unknown.GT is set true. Nevertheless the mean and sd of the GT should still be given. This values will be used as a starting value for the optimization routine.

### **est.R0.SB**
1. Epidemic curve, generation time distribution are fed in to the model.
2. Estimate of R at every sequential time step is the output.
   
### **Estimation of time dependent reproduction number:**

1. The incidence data is used to get the initial number of cases. Generation time interval is computed using generation.time. 
2. Agregating the initial data by a time unit is possible with method smoot.RT.

Apart from these methods there are also commands and options to simulate an epidemic - generates an epidemic curve with specified distribution and reproduction number. **sim.epid.indiv**,**sim.epid**

## EpiEstim vs R_0 package

1. EpiEstim - intstantaneous Reproduction number. While R_0 is for Basic Reproduction number
2. Epi_estim methods : differ only according to the inputs for the serial interval - parametric, non parametric, serial interval from the data. While R_0 packages differ on the method employed to find the Reproduction number.
3. EpiEstim uses estimate_R with arguments t_start,t_end in the config to specify the start and end time of each window. While the begin and end arguments in the  est.R0.(EG/ML/SB/TD) is used to say the start and end time of the estimation. 