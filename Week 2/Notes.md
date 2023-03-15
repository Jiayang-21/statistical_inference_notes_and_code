

What is the likelihood?

- It gives  the function of a parameter given the data
    - Eg, you flip a coin 10 times, observed 8 heads, the likelihood of theta (Greek letter of hypothesis) look like: P(theta = 0.7) = 0.23, P(theta = 0.8) = 0.3, etc.
        - Theta = 0.8 is the most likely true population parameter



What is likelihood ratio?

- Likelihood under H0 and H1, one over another
    - For eg above, the P(theta = 0.8)/P(theta = 0.5) = 6.87.
    - Royall said “ratios of 8 and 32 are moderately strong and strong evidence”
- It is **relative evidence ,** meaning that A >> B doesn’t mean A is true, it only means A is more likely to be true than B


Difference between probability and likelihood?

- The equation for P involves both information about the data (x, n) and information about the parameter (θ). To compute a probability, we view θ as fixed (for instance, for a fair coin, we plug in θ=.5) and then estimate the probability of different outcomes (x, n). The resulting function is the probability mass function. To compute likelihood, we instead view our data as fixed (e.g., observing 5 heads out of 10 coin tosses), and we view P as a function of theta,
estimating the value that maximizes the likelihood of our particular sample.


What is the Bayesian statistics

- We **quantify** a **prior** first and use data to **update** our belief to lead to a **new posterior** belief.



What is the formula of posterior odds?
<img width="573" alt="image" src="https://user-images.githubusercontent.com/58786087/225404914-ca4c3f78-c897-48bb-b3f0-408e789d38e9.png">


What is bayes factor?

- A Bayes factor is the relative evidence (likelihood term above) for one model compared to another.


How to interpret Bayes factor?

- A Bayes factor between 1 and 3 is considered ‘not worth more than a bare mention’, larger than 3 (or smaller than 1/3) is considered ‘substantial’, and larger than 10 (or smaller than 1/10) is considered ‘strong’. These labels refer to the increase in how much you believe a specific hypothesis, not in the posterior belief in that hypothesis. If you think extra-sensory perception is extremely implausible, a single study with a BF = 14 will increase your belief, but you will now think extra-sensory perception is pretty much extremely implausible


What is bayesian estiamation?

- Instead of testing two models (prior vs posterior ) you can also use the posterior to estimate the plausible values


What is credible interval


- In Bayesian approaches, probability distributions represent our degree of belief. When calculating a credible interval, one is saying ‘I believe it is 95% probable (given my prior and the data) that the true parameter falls within this credible interval’. A 95% credible interval is simply the area of the posterior distribution between the 0.025 and 0.975 quantiles.


        







