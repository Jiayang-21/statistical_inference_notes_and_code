# statistical_inference_notes_and_code

Repo for my learnings of the MOOC "Improving your statistical inferences" (https://www.coursera.org/learn/statistical-inferences)


## Main contribution:

#### 1. Utilized Cornell notes structure and converted learnings into a Q & A format.
#### 2. Convert the R-code used for simulations and analyses into Python code. 

##### For example, below shows the week 3 (Error Control) file:

#### Code:

<img width="933" alt="image" src="https://user-images.githubusercontent.com/58786087/225491983-6985d229-5cf9-4355-916d-612188422797.png">
.
.
.
<img width="733" alt="image" src="https://user-images.githubusercontent.com/58786087/225492018-b41d03b0-33f3-4af2-8ac5-72690dd1010b.png">


#### Notes: 


How to prevent type 1 errors (in multiple testing)?


- Bonferroni correction (Dunn correction)
    - Simple: new alpha = original alpha/# of test
    - Conservative
- Holm correction:
    - Order P value, inverse rank, multiply the new rank with p-value to get the corrected p-value
    - A little less conservative
    <img width="561" alt="image" src="https://user-images.githubusercontent.com/58786087/225490389-3eab337d-277e-4ad5-ae5d-34570862c646.png">



What is optional stopping?

- Collecting data until p<0.05.
    - This may sound valid. But it will inflates the type 1 error
    - This could **always** lead to a significant results
    - However, with controlled error rate, this can be a very effective way to collect data
    - Work-around: **Sequential analysis** to control error rate (Pocok correction).
        - efficient: US army actually stopped this publication during the war so that enemies don’t know this
        - Very similar to Bonferroni, but if you look twice, you will have a slightly higher threshold than, let’s say 0.025, if alpha is 0.05.
            - <img width="535" alt="image" src="https://user-images.githubusercontent.com/58786087/225490474-90c6eb66-a9f4-40b7-80a4-840cc741b4e0.png">

        
        
        - 5 looks with out correction
            - <img width="503" alt="image" src="https://user-images.githubusercontent.com/58786087/225490521-48151723-f2c8-4353-9049-a1ed2e5da937.png">
                        
            
        - Pocock corrected sequential analyses
            - Still kind of weird, but much better controlled
            - <img width="501" alt="image" src="https://user-images.githubusercontent.com/58786087/225490553-fc4ad498-136e-45dd-ae81-f5550da617ba.png">

            

What is false discovery rate control?

- A more recent approach by Benjamini & Hochberg
    - Good for when you have many many many things to test together, eg, gene analysis
    - How-to: [A Guide to the Benjamini-Hochberg Procedure - Statology](https://www.statology.org/benjamini-hochberg-procedure/)
        - Uses: rank of p-values, # of tests, and a chosen false discovery rate


Let’s say you had a significant result, if you repeat it, what is the chance that you will observe a significant result again?

- May be tempting to say 95%, but that is completely wrong. The probability will be the power. So you will need to do a power analysis
    - Power is a function of sample size and effect size
        -<img width="581" alt="image" src="https://user-images.githubusercontent.com/58786087/225490645-ae657c7e-d793-4031-b843-1ad0009b14b3.png">


How to increase power besides increasing sample size?

- Decreasing measurement error: reducing the variability
    - Eg, IQ test, you don’t just ask 1 question, instead, you ask a lot
- Using within designs (Also named dependent groups or repeated measures design)
    - all participants take part in every condition. It’s the opposite of a between-subjects design, where each participant experiences only one condition.
    - More powerful bc **Individual variation is removed**
    - All longitudinal studies use within-subjects designs
    - Cons: time-related effects, as it is hard to control the effects of time on the outcomes of the study, eg, a lockdown
- Increasing variability in the response options
    - Eg, using 1-10 scale is easier to find differences than a 1-3 scale
- Use one-sided tests (When you have a directional prediction)
    - <img width="581" alt="image" src="https://user-images.githubusercontent.com/58786087/225490737-0d8dd71a-a7c1-4c4c-b860-74b6ad43af3c.png">

    
    
What is p-hacking?

- The practice of manipulating data to achieve statistical significance. It is when researchers make choices after seeing their data to help them get a significant result. This includes choices or tweaks like dropping outlying data points or changing the way you analyze data.
    - Selecting only the data that supports the hypothesis and ignoring the rest
    - Running multiple tests on the same data until a significant result is found.
    - Removing outliers from the data.
    - Changing the analysis method until a significant result is found.
    

What is pre-registration? 


- Pre-registering a study protocol with a detailed analysis plan helps to reduce the risk of data dredging, p-hacking, or other practices that may inflate Type 1 errors.
    - Distinguish confirmatory research from exploratory analyses
    - Coming up with hypothesis after seeing data reverses the empirical cycle.
        - During exploration, you can perform hypothesis test, but you cannot test a hypothesis.
- To pre-register
    - justify sample size (stopping rule)
    - specify IV (independent variable) and DV (dependent) for test : what are you going to measure?
    - Describe the analysis plan (alpha, how to clean data, eg, what is outlier?)


When does a significant p-value indicate a true effect?
    - Useful tool: [Experience Statistics (shinyapps.org)](http://shinyapps.org/apps/PPV/)





## Repo for the course: https://github.com/Lakens/statistical_inferences
