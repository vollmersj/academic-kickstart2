---
title: Accelerating Markov Chain Monte Carlo
summary: Speeding up MCMC for scalable Bayesian Inference.
tags:
- MCMC
date: "2017-06-16T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
#  caption: Photo by rawpixel on Unsplash
  focal_point: Center

links:
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

In recent years there has been an explosion of complex data-sets in areas as diverse as Bioinformatics, Epidemiology, Finance as well as from Industrial Monitoring Processes. Realistically, the complex dynamics characterising the data generating process can only be expressed as a high-dimensional stochastic model, rendering exact Bayesian inference and classical Monte Carlo methods insufficient.  The only computationally feasible and accurate way to perform statistical inference is with Markov Chain Monte Carlo (MCMC), typically employing methods based on Metropolis-Hastings schemes. 

A key feature of these methods is that they are asymptotically un-biased, i.e. the posterior distribution can be approximated arbitrarily well, provided sufficient samples are generated. While this property is advantageous, this comes at a cost: typically such methods exhibit large variance meaning that many samples must be generated to obtain an approximation to within a given error tolerance. This has motivated practitioners to investigate approximate inference methods, where the property of asymptotic unbiasedness is relaxed, thus permitting a small amount of bias at the cost of a huge reduction in variance. 

Another class of approximate inference algorithms is the Stochastic Gradient Langevin Dynamics (SGLD) algorithm, originally proposed for approximating expectations with respect to an unnormalised density. In contrast to the discretised Langevin dynamics, the SGLD uses an unbiased estimate of the gradient of the log target based on a small subset of the data, thus mitigating computational cost by requiring a reduced number of data point evaluations per sample generated. 

There has been much recent activity on the use of piecewise deterministic markov processes (PDMP’s) as a method for sampling. While still in their infancy, these novel methods appear to be advantageous over state of the art MCMC methodology.  PDMP based methods for sampling demonstrate many highly desirable properties:  they are non-reversible but remain asymptotically un-biased, and moreover, for tall-data problems sub-sampling can be introduced while preserving the invariant measure.



