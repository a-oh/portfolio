
## Background

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([_source_](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([_source_](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):

-   [SAT](https://collegereadiness.collegeboard.org/sat)
-   [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([_source_](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([_read more about this here_](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

However, despite this recent trend to opt-out of standardized tests for college admissions, more states are opting-in to mandate either SAT or ACT to Juniors or Seniors in high school, with the help of test agencies offering free testing days and study materials. ([_source_](https://collegereadiness.collegeboard.org/sat/k12-educators/sat-school-day/about)). By doing so, the state officials are not only eliminating additional assessment tests for students to stress over by replacing them with SAT or ACT, but also hoping to encourage those who are not planning on attending college to reconsider. In this analysis, I want to investigate whether the increase in SAT participation leads to higher education attainment for states.

-   [`sat_2017.csv`](http://localhost:8890/notebooks/dsi/project/project_1/data/sat_2017.csv): 2017 SAT Scores by State
-   [`sat_2018.csv`](http://localhost:8890/notebooks/dsi/project/project_1/data/sat_2018.csv): 2018 SAT Scores by State
-   [`sat_2019.csv`](http://localhost:8890/notebooks/dsi/project/project_1/data/sat_2019.csv): 2019 SAT Scores by State
-   [`table-1.csv`](http://localhost:8890/notebooks/dsi/project/project_1/data/table-1.csv): List of US States and Territories by Education Attainment ([_table source_](https://en.wikipedia.org/wiki/List_of_U.S._states_and_territories_by_educational_attainment#cite_note-datasource-1)) ([_original source - Bureau, U.S. Census. "2013-2017 American Community Survey 5-Year Estimates"_](https://archive.vn/20190517072954/https://factfinder.census.gov/faces/tableservices/jsf/pages/productview.xhtml?pid=ACS_17_5YR_S1501))




## Data Dictionary

|Feature                           |Type   |Dataset     |Description                                                                                                                                    |
|----------------------------------|-------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
|state                             |object |SAT-HigherEd|State in the US and District of Columbia                                                                                                       |
|2017_participation_rate           |float64|SAT-HigherEd|The percent SAT participation rate among high school seniors in 2017 (units percent to decimals 0.38 means 38%)                                |
|2017_ebrw                         |Int64  |SAT-HigherEd|The average score of the Evidence-Based Reading and Writing section in 2017 (out of 800)                                                       |
|2017_math                         |Int64  |SAT-HigherEd|The average score of the Mathematics section in 2017 (out of 800)                                                                              |
|2017_total                        |Int64  |SAT-HigherEd|The average of the total SAT score in 2017 (out of 1600)                                                                                       |
|2018_participation_rate           |float64|SAT-HigherEd|The percent SAT participation rate among high school seniors in 2018 (units percent to decimals 0.38 means 38%)                                |
|2018_ebrw                         |Int64  |SAT-HigherEd|The average score of the Evidence-Based Reading and Writing section in 2018 (out of 800)                                                       |
|2018_math                         |Int64  |SAT-HigherEd|The average score of the Mathematics section in 20178(out of 800)                                                                              |
|2018_total                        |Int64  |SAT-HigherEd|The average of the total SAT score in 2018 (out of 1600)                                                                                       |
|2019_participation_rate           |float64|SAT-HigherEd|The percent SAT participation rate among high school seniors in 2019 (units percent to decimals 0.38 means 38%)                                |
|2019_ebrw                         |Int64  |SAT-HigherEd|The average score of the Evidence-Based Reading and Writing section in 2019 (out of 800)                                                       |
|2019_math                         |Int64  |SAT-HigherEd|The average score of the Mathematics section in 2019 (out of 800)                                                                              |
|2019_total                        |Int64  |SAT-HigherEd|The average of the total SAT score in 2019 (out of 1600)                                                                                       |
|2013-2017_hs_graduate             |float64|SAT-HigherEd|The percentage of the total population who are high school graduates (units percent to decimals 0.38 means 38%)                                |
|2013_2017_bachelors_graduate      |float64|SAT-HigherEd|The percentage of the total population with Bachelor’s degree or higher (units percent to decimals 0.38 means 38%)                             |
|2013-2017_advanced_degree_graduate|float64|SAT-HigherEd|The percentage of the total population with an advanced degree (units percent to decimals 0.38 means 38%)                                      |





## Analysis and Conclusion

 - Top 10 states with the highest percentage of college graduates had high SAT participation rates.
	 - 9/10 states placed above 75th percentile in the SAT participation rate in 2017
	 - 7/10 states placed above 75th percentile in the SAT participation rate in 2018
	 - 6/10 states placed above 75th percentile in the SAT participation rate in 2019
	 - 3 states (District of Columbia, Conneticut, and New Hampshire) placed placed above 75th percentile in the SAT participation rate in all three years
 - Overall, there seems to be a weak positive correlation
 - Caveats
	 - the dataset is somewhat limited (changes to SAT implemented in 2016)
	 - correlation does not equal causation - closer look at the states with highest improvement in SAT participation rate would reveal whether this leads to an increased % of college graduates in the states 5-10 years later
	 - no information on how much it costs for states to engage students in participating in SAT or ACT - may not return the best result per dollar spent compared to a more targeted spending for low-income counties
	 - if more colleges abandon SAT, the incentive for students to take the standardized test diminishes 


