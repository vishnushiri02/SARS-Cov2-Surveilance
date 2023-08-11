---
id: nwkot08jbh3bx24z3zcf9sg
title: Implementation of gerstung lab paper
desc: 'Understanding and reusing the code'
updated: 1691675689004
created: 1689585165705
traitIds:
  - meetingNote
---


## Attendees

<!-- Meeting attendees. If you prefix users with an '@', you can then optionally click Ctrl+Enter to create a note for that user. -->

- Dr. Daniela Börningen
- Vishnushiri

## Work done so far

<!-- What has been done so far -->

Comprehension of the model used in the gerstung lab paper. Statistical distributions that were used were also intuitively understood. Distributions like negative binomial, Dirichlet multinomial; Concepts like spline function, convolution, multinomial and multivariate were all read and understood.

### Gerstung Lab paper

[[Doubts and answers|Growth_Rate_Estimation.GerstungLab#doubts-and-answers]]


<!-- Any doubts to be cleared -->

## Next Step

<!-- What should  I work on till the next meeting-->
- We are not going to implement the Gerstung lab paper
- See if gerstung lab program works for their data set, modulate the parameters and see what happens
- Look into more approaches that handle epidemic data and choose what can be reimplemented.

## Tasks

<!-- You can add any follow up items here. If they require more detail, you can use `Create Task Note` to create each follow up item as a separate note. -->

- [ ] Run the program with their data and then try repeating with german data

> There are lots of dependency issues between numpyro,jaxlib and genomic surveillance. The package needs old version of numpyro and jaxlib which are giving tough time. pip is able to install jaxlib version 0.1.75 onwards with cuda but genomic surveillance needs package 0.1.62

- [ ] Read given papers and about the R package
  