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
