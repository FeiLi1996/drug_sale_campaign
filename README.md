# drug_sale_campaign

## About project

When a new drug hits the market, not every clinician is aware of the drug treatment because there are too much information on the web these days. One way to promote a new drug awareness is through campaigns. This could be advertisements on certain medical related websites or targeted messages in certain medical software applications like a prescribing application. 

This project focuses on evaluating a campaign effectiveness to promote a new drug called 'FEELA-GOOD' . FEELA-GOOD is a medication that relieves pain and makes you feel good. This is a special drug because it has no side effects except maybe emptying your cash wallet.We are all aware of the danger of opioids in pain management. Opioids are great for relieving pain but there are high risk of addiction and overdose that might lead to death. According to CDC, in 2021, over 75% of the approximately 107,000 drug overdose fatalities were attributed to opioids.This translates to a staggering 80,000+ lives lost to opioid overdoses in the same year, equating to an average of 220 individuals per day. It's crucial to recognize that these figures are likely conservative estimates, and the opioid crisis is likely to escalate, as evidenced by numerous tragic overdose incidents reported in the news.

## About the Data set

This  synthetic dataset gives information about the doctors'  prescription behavior and whether the doctor has seen the promotional message or not. There are only 6 columns. We will use the data to analyze if the messaging had any positive lift in 'FEELA-GOOD' prescriptions. There will be visuals to view data in different segments.Finally a T-test will be used to see if the campaign effect is statistically significant.


* Attribute Information
  +	rx_id 
      +	__Meaning__: The unique ID for the prescription
      +	__Variable Type__: character
      +	__Possible values__:  any number from 1 to infinity
  +	doctor_id 
      +	__Meaning__: The unique ID of a  doctor 
      +	__Variable Type__: character
      +	__Possible values__:  any number from 1 to infinity
  +	drug_name 
      +	__Meaning__: Name of the drug. Could be brand or generic name.
      +	__Variable Type__: character
      +	__Possible values__:  'OXYCODONE' , 'APIXABAN', 'FEELA-GOOD',etc
  +	is_pain_drug 
      +	__Meaning__: Is the drug used for pain or not. 1 if yes. 0 if no.
      +	__Variable Type__: integer
      +	__Possible values__:  1 or 0     

  +	is_target_drug 
      +	__Meaning__: Is the drug being prescribed the drug of interest? 1 if yes. 0 if no.
      +	__Variable Type__: integer
      +	__Possible values__:  1 or 0

  +	has_seen_msg 
      +	__Meaning__: Did the doctor see the campaign message?  1 if yes. 0 if no.
      +	__Variable Type__: integer
      +	__Possible values__:   1 or 0


## Group Comparison graph 1
![Alt text](pain_prescription_proportion_between_groups.PNG)


- Insight: Seems like both groups have similar tendency to prescribe pain drugs. This is important attribute.This could be a confounding variable if it wasn't balance. We would need to do things to balance this covariate like propensity score weighting/matching.
## Group Comparison graph 2
![Alt text](target_drug_proportion_between_groups.PNG)

- insight: Seems like the treatment group prescribed more of the campaign drug. Maybe the promotion was effective???
## Group Comparison table with attributes
![Alt text](attributes_at_group_level.PNG)

- insight: Seems like treatment group has much higher proportion of their prescriptions being related to the campaign

## Conclusion
- The campaign had a positive relative lift of 94%[(43.1-22.2)/(22.2)] for Feela-Good drug. This was statistically significant with a p-value < 0.001. The A/B testing shows that the campaign intervention was very effective in promoting the new drug. We should roll out more campaigns to doctors that share similiar attributes to the test/control group.