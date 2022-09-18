Coding Task V3
Use this Data source to feed data in mongo - https://www.ecdc.europa.eu/en/publications-data/data-covid-19-vaccination-eu-eea

`A. Question`
Design a REST API endpoint that provides the report of a country by a given range in
weeks.
Request Description:

`GET` /vaccine-summary

Query Parameters:

```txt
    `c`, country code to get report for
    `dateFrom`, yyyy-Www, eg. 2020-W10 (Including)
    `dateTo`, yyyy-Www, eg, 2020-W20 (Excluding)
    `rangeSize`, number, eg, the period for which to calculate metrics
    `sort`, either by `NumberDosesReceived`[descending] or `weekStart` [ascending]
```

`B. Sample responses`
These are just examples to provide guidance (It will just contain total number of doses in
given date range)

`Example 1: Match`
Request
GET /vaccine-summary?c=AT&dateFrom=2020-W10&dateTo=2020-W53&range=5

Response
{
    "summary": [
        {
            "weekStart": "2020-W10",
            "weekEnd": "2020-W15",
            "NumberDosesReceived": 1000
        },
        {
            "weekStart": "2020-W15",
            "weekEnd": "2020-W20"
            "NumberDosesReceived": 2000 
        } ,
        ... till end of range (dateTo)
    ]
}

`Example 2: No match`
Request
GET /vaccine-summary?c=AT&dateFrom=2017-W00&dateTo=2018-W02&range=5
Response
{
    "summary": []
}


`C. Tech Requirements`
    1. Nodejs
    2. Typescript
    3. MongoDB (use appropriate aggregation, when possible)
    4. Docker and docker-compose (optional)
    5. Tests: Chai and Mocha (Or Jest)
    6. Input validation (Optional)
    7. Code linter

`D. Submission requirements`
    1. No Typescript = No Submission (Please don’t waste your time)
    2. Design and implement your solution as you would do for real production code
    3. Clean and well-structured solution
    4. Use Mongo mock and add integration test cases
    5. Commit early and often. We want to be able to check your progress
    6. Please complete your working solution within 7 days of receiving this challenge, and
    be sure to notify us when it is ready for review.
    7. Please submit your code in any way you like: Github or bitbucket with instructions on
    how to run the code and any assumptions you made.
    8. Bonus (Feel free to add this feature in your code/test to stand out): Add
    rate-limit feature in API, eg, for the given IP address, to only allow 5 calls per minute