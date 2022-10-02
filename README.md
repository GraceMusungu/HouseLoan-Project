/* HouseLoan-Project */

/* select the data we want to start with */
SELECT "CODE_GENDER", "NAME_TYPE_SUITE", "NAME_HOUSING_TYPE", "AMT_INCOME_TOTAL", "NAME_EDUCATION_TYPE", "CNT_FAM_MEMBERS", "OCCUPATION_TYPE" FROM loan
WHERE "OCCUPATION_TYPE" is NOT NULL

/* let's check which gender is taking more financial loans than the other. if such a company
wanted to market their product, it would help to know where to target more */

SELECT "CODE_GENDER", COUNT(*) 
FROM loan 
GROUP BY "CODE_GENDER";

/* getting the minimum amount income total who took the loan */
SELECT MIN("AMT_INCOME_TOTAL")
FROM loan 

/* getting the average of the credit amouny */
SELECT AVG("AMT_CREDIT")
FROM loan


