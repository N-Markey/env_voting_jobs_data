# Congressional Environmental Voting and Jobs Data, 1989-2016
The csv file jobs_voting_final.csv contains data on Congressional environmental voting and district fossil fuel jobs between the 101st (1989-1990) and 114th (2015-2016) Congresses. Each row corresponds to one member in one session of Congress. The columns are as follows:

* **congress** (integer): the session of Congress
* **state_abbrev** (character): the two-letter postal abbreviation for the state which the member represents
* **district_code** (integer): the number of the member's district
* **district_id** (character): the member's state and district, formatted "ST-XX", where "ST" is the two-letter abbreviation for the member's state and "XX" is the two-digit representation of the member's district number
* **party code** (integer): code representing member's party, as used by Voteview. Documentation [here](https://voteview.com/articles/data_help_parties). Note that, for our modeling purposes, we filter the data to only include Democrats (party code 100) and Republicans (party code 200).
* **icpsr** (integer): unique identifier for each lawmaker provided by the Inter-University Consortium for Political and Social Research. Useful for joining to other Congressional data.
* **bioname** (character): member name, as formatted by Voteview. According to [Voteview](https://voteview.com/articles/data_help_members), "For most members, agrees with the Biographical Directory of Congress."
* **nominate_dim1** (numeric): the member's first-dimension DW-NOMINATE score
* **nominate_dim1** (numeric): the member's second-dimension DW-NOMINATE score
* **nokken_poole_dim1** (numeric): the member's first-dimension DW-NOMINATE Nokken-Poole score for this session of Congress
* **nokken_poole_dim2** (numeric): the member's second-dimension DW-NOMINATE Nokken-Poole score for this session of Congress
* **lcv_pooled_score** (numeric): member's League of Conservation Voters score for this session of Congress. Created by averaging annual LCV scores for the two years of the Congress, weighting by number of relevant votes in each year.
* **est_jobs** (numeric): estimated number of fossil fuel extraction jobs in the member's district. Created using census County Business Patterns data on industry-specific employment by county.

Thorough background on the variables and the methodology involved in creating this dataset is contained in section II of Final_Report.pdf
