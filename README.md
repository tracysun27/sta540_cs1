# STA 540L: Case Study 1 Reproduction (Tracy Sun)

- Code: sta540_cs1.Rmd
- Revised SAP: sta540_cs1_sap_edited.pdf
- 
The displayed results of the reproduction can also be found in the sta540_cs1.pdf file.

## Table 1
<img width="441" height="571" alt="Screenshot 2026-01-28 at 3 42 18 PM" src="https://github.com/user-attachments/assets/50b5d269-bf32-42a4-bd4e-227c5759b796" />

## Primary Analysis
<img width="519" height="367" alt="Screenshot 2026-01-28 at 3 41 26 PM" src="https://github.com/user-attachments/assets/c0abe35e-8b0e-42f1-a9d9-a4c25fc672d7" />

## Secondary Analysis
<img width="437" height="422" alt="Screenshot 2026-01-28 at 3 43 31 PM" src="https://github.com/user-attachments/assets/0837095c-967e-4916-9fd5-a2b8bf9dd538" />
<img width="436" height="375" alt="Screenshot 2026-01-28 at 3 43 46 PM" src="https://github.com/user-attachments/assets/a60a067a-efb5-4824-bd07-a06666bb1fce" />
<img width="436" height="375" alt="Screenshot 2026-01-28 at 3 43 55 PM" src="https://github.com/user-attachments/assets/01c43420-0869-4be8-a8cc-f86f60bd38e3" />
<img width="436" height="325" alt="Screenshot 2026-01-28 at 3 44 24 PM" src="https://github.com/user-attachments/assets/0bdffd11-db2b-4dd3-81ef-a6aa2b4d126d" />
<img width="436" height="548" alt="Screenshot 2026-01-28 at 3 44 37 PM" src="https://github.com/user-attachments/assets/a5a956c4-683d-4f5e-8a35-39bbf148258b" />
<img width="436" height="307" alt="Screenshot 2026-01-28 at 3 44 46 PM" src="https://github.com/user-attachments/assets/e558e620-625b-4fb4-a764-782388e8bc81" />

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
