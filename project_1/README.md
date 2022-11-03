### Problem Statement

The new format for the SAT was released in March 2016. Since then, levels of participation in multiple states have changed with varying legislative decisions. This project aims to explore trends in SAT and ACT participation for the years 2017-2019 and identify states with low SAT participation. Combined with outside research, this project also aims to identify factors for the low participation and provide reccomendations for the college board to increase participation.

### Outside Research

1) It is shown that only 36% of Americans believe that standardised tests are still neccessary. Of this 36%, 56% were Republicans, 26% were Democrats. 

2) Many colleges are now going test optional and no longer require SAT or ACT for admission because it places unfair cost and burden on low-income and minority students.

3) Minority race in the U.S. seem to favor the Democratic party than Republican party. And urban counties favor the Democratic party while rural counties favor the Republican party

4) Colleges do not have preference over any standardized test.

5) Research has repeatedly proved that students from wealthy families score higher on the SAT and ACT, compared to students from low-income families. And according to a 2015 analysis by Inside Higher Ed, the lowest average scores for each part of the SAT came from students with less than \\$20,000 in family income. The highest scores came from those with more than \\$200,000 in family income. 

### Data Cleaning

1) Checked for missing values
2) Checked for NaN values
3) Converted Dtypes
4) Ammended wrong values/ incorrect data
5) Dropped unnecessary columns
6) Renaming columns
7) Merging dataframes

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|act_2017|U.S. states which the data is collected from | 
|act_participation_2017|float|act_2017| ACT participation rate in 2017 (Min: 0, Max: 1)
|act_composite_2017|float|act_2017|Mean ACT composite score of 2017 (Min: 1, Max: 36)
|act_participation_2018|float|act_2018| ACT participation rate in 2018 (Min: 0, Max: 1)
|act_composite_2018|float|act_2018|Mean ACT composite score of 2018 (Min: 1, Max: 36)
|act_participation_2019|float|act_2019| ACT participation rate in 2019 (Min: 0, Max: 1)
|act_composite_2019|float|act_2019| Mean ACT composite score of 2019 (Min: 1, Max: 36)
|sat_participation_2017|float|sat_2017| SAT participation rate in 2017 (Min: 0, Max: 1)
|sat_total_2017|float|sat_2017| Mean SAT total score of 2017 (Min: 400, Max: 1600)
|sat_participation_2018|float|sat_2018| SAT participation rate in 2018 (Min: 0, Max: 1)
|sat_total_2018|float|sat_2018|Mean SAT total score of 2017 (Min: 400, Max: 1600)
|sat_participation_2019|float|sat_2019| SAT participation rate in 2019 (Min: 0, Max: 1)
|sat_total_2019|float|sat_2019| Mean SAT total score of 2017 (Min: 400, Max: 1600)
|us_abbrev_states|object|https://gist.github.com/rogerallen/1583593 | Abbreviations of U.S. states 
|political_party|object|https://www.nytimes.com/elections/2016/results/president | Political party of the state (Republican or Democratic)


### Exploratory Data Analysis

1. Democratic states has more 100% participation in SAT while Republican states has more 100% participation in SAT
2. The lower the participation, the higher the test score. 
3. High SAT total comes from rural areas like North and South Dakota, Kansas and Iowa.
4. Discovered well-scoring states generally have lower participation in the SAT test. This is due to a sampling bias where students who bother to take SAT test in Republican states which favors the ACT test would most likely be higher-achieving students and likely come from well-to-do families therefore bringing up the mean total score of SAT for their state.
5. Nevada and Hawaii democratic states, doing better in SAT compared to ACT. 
6.  Minnesota and Missouri falling ACT participation but low SAT participation
7. In 2019, North Carolina and South Carolina with more than 50% SAT participation and more than 78% ACT participation. 
8. In 2019, Alaska has less than 50% participation on both test

### Reccomendation and Conclusion

###### Key factor for decrease in SAT participation
I have discovered within this analysis that the test-optional policy has been contributing to the decrease in participation rate
as states have the choice now to not participate in any standardised tests at all. 

After doing some research, I found out that one of the few reasons for the test-optional policy is that it is **inaccessible for low-income families and minorities**. This causes this group of demographic to be under represented in colleges. Therefore, colleges are also in favor of test-optional policies to become more accessible to everyone.

According to the chloropeth map in part 3, we can see that SAT participation is low in the middle part of the U.S. which also happens to be the more rural states of the U.S. This makes us wonder, why are rural states more in favor towards ACT. It could be because states still believe that taking the SAT is expensive.

With reference to one of the key findings from EDA, it is true that the high SAT scores comes from rural states. This statistic is only possible due to higher-achieving students who are likely to come from well-to-do families who are attemping to apply to out of state colleges in urban cities. **Proving that SAT are more in favor towards the rich**.

Also, students who come from well-to-do families tend to understand the importance of education while students who come from low-income families might not understand the importance. In addition, low-income families might face financial problems with school fees or college tuition which deters their children from aiming to an out of state college. All in all, as states become test-optional, these students would not feel inclined to participate in standardised testing like the SAT further lowering participation rates. 

###### Reccomendation
In order to combat the root issue of standardised test being inaccessible, the college board can start to work with high schools to help students better understand the importance of college. Once these students understand the importance of college, these students would be more motivated to partake in standardised test to secure a placement in college.

Together with existing efforts like SAT day which allows students to take the SAT for free and free online resources such as Khan Academy. These efforts would then help make SAT accessible to all.
Which would help us achieve an increase in participation.

The college board can also take this chance to show students that the SAT is no longer that test that is full of trick questions and has been reformatted to test students on college readiness. Once these students realised that the SAT is no longer made to be 'stressful', sentiments on the SAT will get better which will attract more students to take the SAT which would also increase participation in SAT.

###### States to target
1. Nevada and Hawaii democratic states, doing better in SAT compared to ACT. College board can try to use test scores to encourage these states to try to increase participation as students are doing better in SAT than ACT.

2. Minnesota and Missouri falling ACT participation but low SAT participation. This shows that there are decreasing interest in ACT in these states. Therefore college board can take the opportunity to market SAT in these states. 

3. In 2019, North Carolina and South Carolina with more than 50% SAT participation and more than 78% ACT participation. This shows that these states are still interested in standardised tests and college board can further increase their market share in these states

4. In 2019, Alaska has less than 50% participation on both test. Alaska is also a rural state, as discussed above, when accessiblity increases, there is a better chance for SAT to target this state.

### Citations

Source 1: https://www.insidehighered.com/admissions/article/2021/06/01/states-and-state-systems-move-away-required-testing-admissions

Source 2:
https://christianacademiamagazine.com/test-optional-movement-should-we-require-sat-or-act-or-neither/

Source 3: https://today.yougov.com/topics/society/articles-reports/2018/06/21/standardized-tests-college-admission

Source 4: https://www.pewresearch.org/politics/2018/03/20/1-trends-in-party-affiliation-among-demographic-groups/

Source 5: https://www.collegeraptor.com/getting-in/articles/act-sat/preference-act-sat-state-infographic/

Source 6: https://edition.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html

Source 7: https://gist.github.com/rogerallen/1583593

Source 8: https://www.nytimes.com/elections/2016/results/president 



