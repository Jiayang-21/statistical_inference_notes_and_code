How to interpret confidence interval (CI)?


- First, this is a **frequentist** concept
    - Thus, this applies in the long run
- In the long run, 95% of (future) confidence intervals will contain the true parameter value.
- A visual to help, the simulated study has zero effect. Only 5% of CIs does not contain the true effect size, which is zero.
- <img width="833" alt="image" src="https://user-images.githubusercontent.com/58786087/226150316-cb339cf3-d12c-4696-a812-2dceefea453c.png">
- If 95% of CI does not include 0 —> automatically implies  p-value < 0.05

How to not interpret CI?


- Though this is how people tend to interpret it, it is **incorrect**!
- <img width="826" alt="image" src="https://user-images.githubusercontent.com/58786087/226150326-5772487a-bdc5-4c32-9a34-1c9d2ebec21e.png">
- - But! if we run a simulation, it turns out that a single CI captures the true value **84.3% of the time**. This is also known as a **captured percentage.**


So, how is CI calculated?


-<img width="838" alt="image" src="https://user-images.githubusercontent.com/58786087/226150353-392dd735-1a1b-46b4-b165-537288599a5d.png">
- Should be obvious that larger N is good for having a smaller CI
- <img width="892" alt="image" src="https://user-images.githubusercontent.com/58786087/226150361-c3b93f12-0544-4f84-b265-4c73c689b64d.png">



How to reduce CI?



- The width of the confidence interval depends on the sample size, the confidence interval level, and the standard error



What is Standard error ? What are the implications?


- The standard error (SE) estimates the variability between sample means that would be obtained after taking several measurements from the same population. It is easy to confuse it with the standard deviation, which is the degree to which individuals within the sample differ from the sample mean


Ok, what is credible interval, again?



- In Bayesian stats, we have a similar thing as the CI, but more intuitive.
- A credible interval is a quantified belief that quantifies 95% of the values we find most plausible.
- E.g., blue is the prior, grey is the observed data, black is the posterior, 95% credible interval contains the values we found most plausible
- <img width="842" alt="image" src="https://user-images.githubusercontent.com/58786087/226150412-cda1d3ab-dfee-4b7b-a212-b81ebfedce73.png">



What is the benefit of having more sample size?


- Less variation in data —> higher power (less Type 2 error) & more accurate estimate
    - Why doesn’t it help with Type 1 errors?
        - Type 1 error rate is directly determined by the chosen significance level (alpha) of the test, which is usually set at 0.05 or 0.01. The significance level is the probability of rejecting a true null hypothesis. This means that regardless of the sample size, the probability of committing a Type 1 error remains the same because it is determined by the chosen alpha level.
     
    

How to calculate statistical power?



- Statistical power is a function of the effect size, the alpha level, and the sample size.
- <img width="834" alt="image" src="https://user-images.githubusercontent.com/58786087/226150430-32c4da83-b5dc-47ef-b339-c5269674a0f7.png">


What is P-curve analysis, and why is it useful?


- Since we know that if there is an effect, the P-value should be right-skewed (having more lower P-values than the barely significant values) and that it will be flat otherwise, if there is no effect, thus, if we do a meta-analysis and plot the distribution of the P-values for a set of studies, and get a better sense of wether is a true effect. (AND you want to build your research on the studies that show the right skewed )


  

