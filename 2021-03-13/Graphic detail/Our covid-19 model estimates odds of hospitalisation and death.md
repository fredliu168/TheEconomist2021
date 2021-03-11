###### One size fits few
# Our covid-19 model estimates odds of hospitalisation and death 
##### Death rates depend mostly on age, whereas comorbidities sharply raise chances of hospitalisation in young people 
> Mar 13th 2021 





EVER SINCE the covid-19 pandemic began, calibrating disease-related risk has become a fixture of everyday life. Few places are fully safe. Is it wise to go to the supermarket? What about taking a taxi with the windows down while wearing a mask?

The answers depend not just on how likely an activity is to cause transmission, but also on how bad a bout with covid-19 would be for the individual involved. In rich countries the case-fatality rate (CFR) for people who test positive is just under 2% (the true death rate, including undiagnosed cases, is lower). Yet covid-19’s lethality varies so much that most people do not face a low-single-digit CFR. Few children show symptoms, whereas the elderly—especially those with other illnesses (“comorbidities”)—die at alarming rates. Officials have emphasised universal recommendations like masks and social distancing, leaving individuals to choose risk tolerances within those guidelines.


Such assessments can be complex. Although older people account for most deaths from covid-19, the mechanism behind this pattern is unclear. Are the elderly at risk purely because of their age? Or is it instead because they often have comorbidities that weaken defences against covid-19—and if so, which ones? There is no consensus about the relative importance of these factors. In America the list of comorbidities that enable younger people to get vaccines varies widely between states.

Making granular estimates of covid-19’s risks requires lots of data. The sample needs to have plenty of rare examples, such as gravely ill teenagers and sprightly 90-year-olds. It also needs accurate proportions of specific demography-comorbidity pairings, such as men in their 30s with covid-19, pancreatitis and asthma.

Such a dataset now exists, though it has notable flaws. A group of American hospitals, doctors, insurers, pharmacies and data vendors have pooled data about their patients to create the Covid-19 Research Database, an archive of over 5bn medical records. In partnership with A3.AI, a research group that has spliced each patient’s records together, the project’s administrators have granted access to The Economist.

The archive records the age, sex and presence of 29 comorbidities among 104m people in America, of whom 466,000 were diagnosed with covid-19 in May-December 2020. It also lists which ones died in 2020, and, for people who tested positive, their date of diagnosis and whether they were hospitalised during their illness. Although the population in the dataset is sicker than average, this bias can be offset by adjusting the sample using official data on cases and deaths by age, sex and time period.



The data illuminate patterns that doctors have already seen in coronavirus wards, but are not yet conventional wisdom. Covid-19 spreads mostly through the air, and is often considered a respiratory ailment. However, complications in severe cases are often cardiovascular, including heart inflammation and irregular blood clotting. The archive bolsters growing evidence that covid-19 attacks the body broadly, and is most exacerbated by comorbidities that cause inflammation or that affect the circulatory system, such as kidney, liver or heart problems. In contrast, respiratory conditions like asthma matter less—though severe ones, such as lung cancer or pulmonary fibrosis, are big risk factors too.

How much danger such conditions pose to covid-19 patients depends on the outcome you measure. Most risk analysis focuses on deaths. On this metric, raw age is a stronger predictor than listed comorbidities; sex is important as well. After correcting for biases in the data, 8.5% of men and 4.9% of women in their 70s with no known conditions besides covid-19 died. The figures for people aged 25-34 with covid-19, heart disease and hyperlipidemia (eg, high cholesterol) were 0.8% for men and 0.7% for women. This means that you might want to wait until your tennis-playing, adventure-travelling grandparents are vaccinated before visiting them. It also means that governments have been right to vaccinate older people first, even unusually fit ones—and that men might need lower age cut-offs than women do.

However, covid-19 can cause people great harm even if it does not kill them. And when it comes to predicting hospital stays, comorbidities play a greater role. Of the 25- to 34-year-olds with heart trouble, hyperlipidemia and covid-19, a quarter of men and a fifth of women were hospitalised—roughly the same shares as those of people in their 70s without other listed conditions. People aged 25-34 without known illnesses besides covid-19, in contrast, had just 1.6% (for men) and 1.0% (for women) chances of hospitalisation. Although most younger patients beat covid-19 eventually, those with relevant comorbidities often cannot do so at home.



Covid-19’s interactions with demography and comorbidities are too complex for simple rules of thumb. To calculate risks for all possible combinations of these factors, we have built a statistical model using a machine-learning algorithm called “gradient-boosted trees”. For any group of un-vaccinated people of a given age, sex and mix of comorbidities, the model estimates the shares that, within 30 days of a positive test for covid-19 in America in late 2020, would have died or been hospitalised. You can explore its output  and learn how we built it .

Our model cannot estimate risk reliably for individuals. The archive used to build it has several limitations. It only includes people with health insurance, and does not list patients’ location, ethnicity or date of death. Most octogenarians’ ages appear as “80+”. Anyone who has filed a medical claim since 2014 citing a comorbidity is listed with that condition, regardless of its recency or severity—preventing distinctions between cancers in remission and malignant tumours. Not everyone without known illnesses is healthy: some have ailments not on the 29-condition menu. And our correction for the data’s overrepresentation of sick people could yield an underestimate of the impact of comorbidities.

Moreover, the model’s assumptions may not hold up beyond its training data. It assumes that people are infected with one of the strains of SARS-CoV-2 common in America in late 2020; that their quality of treatment and odds of getting tested are similar to the American averages at that time; and that they demographically and immunologically resemble people in the data who share their listed attributes. In fact, new viral variants are spreading fast; most health care is either better or worse than the American average; treatments keep improving; and differences in genetics and past viral exposure can affect CFRs.

Yet despite these limitations, the model is probably more accurate than most publicly available alternatives. It accounts for interactions between comorbidities rather than taking each one in isolation, and estimates chances of both hospitalisation and death. Its output represents a group average, from which any given individual will differ. But by narrowing that group to people of the same age, sex and mix of comorbidities, it provides a more relevant starting point than a one-size-fits all average.■

Sources: Covid-19 Research Database; AnalyticsIQ; A3.AI; CDC;

