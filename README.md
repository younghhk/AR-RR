
[![Cancer Research Software Hub](https://img.shields.io/badge/Back_to-Hub-blue)](https://github.com/younghhk/NCI)

# Absolute Risk and Relative Risk


##  Definitions (NCI)
* [Absolute Risk](https://www.cancer.gov/search/results?swKeyword=absolute+risk): The probability that an individual will develop a disease over a specified time period. 
* [Relative Risk](https://www.cancer.gov/publications/dictionaries/cancer-terms/def/relative-risk): A ratio comparing the risk in an exposed group to the risk in an unexposed group. 

Absolute and relative risk quantify different aspects of disease occurrence and often serve different analytic goals.

## Why Absolute Risk Matters
Absolute risk (additive scale) is essential in settings where the number of preventable events is directly relevant:
* Which subgroups gain the most in absolute terms?
* How many cases can be prevented by intervening on an exposure?
* What is the public-health benefit across time?

## Why Relative Risk Matters
Relative risks (multiplicative scale) are central for:

* characterizing the strength of an association
* understanding biological or etiologic interaction
* evaluating effect modification on a proportional scale
* estimating model coefficients in regression frameworks

##  Additive vs Multiplicative Interaction

*(Modern Epidemiology, Table 26-1)*

**Ten-year lung cancer risk**

| Smoking status | No Asbestos | Asbestos |
| -------------- | ----------- | -------- |
| Never smoker   | 0.0011      | 0.0067   |
| Ever smoker    | 0.0095      | 0.0450   |



**Baseline risks (no asbestos)**

* Never-smoker: 0.0011
* Ever-smoker: 0.0095

Smokers begin with a much higher baseline risk.



**Additive scale (risk differences)**

* Never-smokers:
  0.0067 − 0.0011 = 0.0056

* Smokers:
  0.0450 − 0.0095 = 0.0355

Absolute increase is far larger in smokers.
→ Additive scale says asbestos removal helps smokers more.



**Multiplicative scale (risk ratios)**

* Never-smokers:
  0.0067 / 0.0011 ≈ 6.1

* Smokers:
  0.0450 / 0.0095 ≈ 4.7

Proportional increase is larger in never-smokers.
→ Multiplicative scale suggests asbestos is "more harmful" for never-smokers.


This example shows a positive additive interaction but a negative multiplicative interaction.

<!--
More examples: 
* **H. pylori × NSAID use (peptic ulcer disease)**
Slight positive additive interaction; negative multiplicative interaction.

* **Factor V Leiden × Oral contraceptives (venous thrombosis)**
Near-null multiplicative interaction; clear positive additive interaction.-->


##  Points to Consider When Reporting Absolute Risk

* Relative risks can exaggerate or minimize effects unless the baseline risk is shown.

* Absolute risks differ by age, sex, comorbidity, genetics, and background incidence. One value does not apply universally.

* Absolute risk must specify a time horizon (1-year, 5-year, lifetime, etc.). Without this, interpretation is ambiguous.


<!--* Example: ``We assume a 5-year absolute risk of 6 percent in adults aged 55–75, based on SEER incidence rates."-->
  
## A Related Topic: Absolute Risk Prediction (Gail Model)

The breast cancer risk model developed by Gail and colleagues is a well-known example of how absolute risk can be estimated in practice. The model begins with relative risks obtained from epidemiologic studies, then combines them with population baseline incidence and competing mortality to produce individualized absolute risk estimates such as 5-year or lifetime risk.

The absolute risk of breast cancer for a woman age $a$ over the next $\tau$ years in the Gail model is:

`P(a, τ) = ∫ from a to a+τ  [ h1(t) × r(t) × exp{ -∫ h1(u) r(u) du } × S2(t)/S2(a) ] dt`

Where:

`h1(t)` = baseline breast cancer hazard at age `t`

`r(t)` = relative risk multiplier based on risk factors

`S2(t)/S2(a)` = probability of surviving competing causes from age `a` to `t`



In compact form:

`Absolute risk = Baseline hazard × Relative risk × Competing-risk survival`


**Reference**: Gail MH, Brinton LA, Byar DP, et al. Projecting individualized probabilities of developing breast cancer for white females who are being examined annually. J Natl Cancer Inst. 1989;81:1879–1886. 		PMID: 2593165: 		 [DOI: 10.1093/jnci/81.24.1879](https://doi.org/10.1093/jnci/81.24.1879)

---
## Reference
* Lash TL, VanderWeele TJ, Haneuse S, Rothman KJ, editors. Modern Epidemiology. 4th ed. Wolters Kluwer; 2021. (Examples and interpretation principles referenced in this document derive from this text.)
