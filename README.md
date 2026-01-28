# STA 540L: Case Study 1 Reproduction (Tracy Sun)

- Code: sta540_cs1.Rmd
- Revised SAP: sta540_cs1_sap_edited.pdf

The displayed results of the reproduction can also be found in the sta540_cs1.pdf file.

## Study Overview
### Background/Motivation
HIV is a sexually transmitted infection that attacks the human immune system, and results in AIDS at the most advanced stage of infection. Once they get HIV, a patient cannot be cured. Therefore, prevention and treatment efforts for HIV are very important. In the 1980s-1990s, the HIV pandemic swept the globe, and in particular devastated queer communities due to many gay men passing away from the disease. Men who have sex with other men, referred to as MSM in the study, are at particular risk of HIV if they have anal sex without protection. PrEP, the prevention method discussed in this study which is meant to be taken as a daily pill, has been shown to be very effective at reducing the risk of infection. Young MSM who are part of minority groups (Black/Latinx) are a group that are at risk but do not often know of or use PrEP. They also may engage in other behaviors that could put them at higher risk of HIV, such as binge drinking or drug usage. Because of this, spreading awareness for HIV prevention and examining its relationship to other risk factors is particularly important.

### Primary objective
To determine the difference in effectiveness between several different forms of internet outreach, in particular social media platforms (Facebook and Instagram), dating apps used by MSM (Grindr and Jack'd), and search engines (Google and Bing), in encouraging MSM who are at higher risk of HIV to engage in HIV prevention efforts. This is determined by the rate/number of HIV self-test kits that participants in the study order. 

### Secondary objective
To determine if there is a relationship between the primary outcome (number of self-test kits ordered) and the following variables:
- Reported substance use, including alcohol, stimulants (prescribed and otherwise), opioids, cannabis, and sedatives.
- Stage of health behavior change for HIV testing (assigned as Precontemplation, Contemplation, Determination, Action, Maintenance)
- Attitudes toward HIV testing and treatment 
- Stigma towards HIV and those with HIV
- Medical mistrust
- Opinions about PrEP measures 
  
## Table 1
<img width="447" height="555" alt="Screenshot 2026-01-28 at 4 09 23 PM" src="https://github.com/user-attachments/assets/be89f29b-27e4-46bb-bf09-2b9a893f6206" />

## Primary Analysis
<img width="559" height="414" alt="Screenshot 2026-01-28 at 4 09 37 PM" src="https://github.com/user-attachments/assets/a267f8a0-e1f7-4bdc-a344-9b1d878d7c7e" />

## Secondary Analysis
<img width="638" height="418" alt="Screenshot 2026-01-28 at 4 09 51 PM" src="https://github.com/user-attachments/assets/54c9017e-3b41-468f-9874-95c516ec4705" />
<img width="638" height="262" alt="Screenshot 2026-01-28 at 4 10 06 PM" src="https://github.com/user-attachments/assets/9af513fc-ab7f-4c0e-94b3-0e0c9310722e" />
<img width="638" height="324" alt="Screenshot 2026-01-28 at 4 10 16 PM" src="https://github.com/user-attachments/assets/9a842be3-9ec4-40f4-b8c4-018736c81275" />
<img width="492" height="560" alt="Screenshot 2026-01-28 at 4 10 30 PM" src="https://github.com/user-attachments/assets/da84856d-12d4-482f-80f2-f5c176cf14a7" />
<img width="544" height="560" alt="Screenshot 2026-01-28 at 4 10 40 PM" src="https://github.com/user-attachments/assets/5d30b8c2-4ac9-4e2b-ab8a-0b722ba69607" />
<img width="529" height="655" alt="Screenshot 2026-01-28 at 4 10 52 PM" src="https://github.com/user-attachments/assets/4bb01438-d246-4abe-802b-6e080e028fa3" />

## Additional Figures
<img width="1303" height="432" alt="Screenshot 2026-01-28 at 3 45 08 PM" src="https://github.com/user-attachments/assets/1fc23ff6-adce-4f17-b3f1-974c76e2208c" />
<img width="1252" height="625" alt="Screenshot 2026-01-28 at 3 45 33 PM" src="https://github.com/user-attachments/assets/062d6b8c-f1d3-4acc-a3bf-e4fe545cd2f6" />
<img width="1311" height="654" alt="Screenshot 2026-01-28 at 3 46 01 PM" src="https://github.com/user-attachments/assets/d7e78993-b652-4537-bdbc-e6d7a34327b9" />

## Reflection

### Primary Analysis
Table 1 can be almost perfectly replicated, with a few small differences and notes:

- The race section's counts and percentages are out of 250 instead of 254, as there are 4 participants whose race was left as NA so they were excluded. 
- There was one individual who took the HIV test but also marked a reason not to take it, so they were excluded from the "reasons not to take HIV test" section. 
- The IQR for the age in years, as well as the median and IQR for months since last HIV test are slightly different from the original Table 1. 

As for the contrast significance testing, the p-values obtained are slightly different from the original, although the conclusions on significance are the same, with all the platforms in Wave 1 not being significantly different from each other at the 0.05 level, and all the platforms in Wave 2 being significantly different from each other (mainly due to Jack'd having a lot more test kits ordered than any other platform). However, due to Bing having exactly zero test kits ordered, with the original model, the p-values for both of Wave 2's contrasts that involve Bing are highly non-significant. This may be due to slight differences in how R and SAS calculate the test statistics. However, by adding a small pseudocount of 0.5 to Bing's test kit number to stabilize the estimate, the p-values flip from being insignificant to a similar significance as the paper, with the contrasts for Bing vs Instagram being slightly less significant than Bing vs Jack'd or Jack'd vs Instagram. 

### Secondary Analysis
The secondary analysis, depicted in Appendix 3, is also able to be almost perfectly replicated. The only difference is that for the first table on alcohol/substance use, I was unable to find and account for the 5 rows for the sedative and prescribed stimulants category that were listed as missing, so my counts and p-values were slightly off.

Also, the figures S1-S3 don't have the same counts as in the paper.

## References
Manuscript of the original paper and its appendices, which were followed to reproduce the results, can be found here:
https://pmc.ncbi.nlm.nih.gov/articles/PMC9591705/

https://bookdown.org/yihui/rmarkdown-cookbook/text-width.html

https://www.rdocumentation.org/packages/stats/versions/3.6.2/topics/wilcox.test

ChatGPT was used to generate some sections of this code as well as for some editing and debugging. 
