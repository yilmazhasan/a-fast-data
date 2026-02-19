# A Fast Data

Solution as a Custom GPT App for the _Data Self Service_ purpose.

## Introduction

The name, __FastData__, is derived from accessing the data faster than the usual ways. The usual way would be creating a ticket for a task, pinging a data analyst to build a dashboard or fetch the data and analyze them to review etc. This would require more than 3-4 steps.

With the helps of this automated process, a tech or even a non-tech user might navigate through the database and could fetch the relevant data in minutes by guiding the AI assistant to generate the correct SQL, in order to execute and fetch the data to analyze the meet the required needs.

## Audience

- Business and Sales teams
- HR teams
- Data teams
- Internal performance monitoring teams
- Any team that has data access which they need an analysis on

## Aims

To reduce the load on Data Analysts and to make the Business and Sales or any other team that strive for data analysis autonomously; _Data Self Service_ comes into hand.

- The primary purpose is to democratize the data for any team member who is part of a non-tech team.

- The secondary aim is to aid the data team members to be able to navigate through the various database tables in an automated way with the helps of such an AI assistant, LLMs.

## Technical details

The primary needs to establish such an app would be:
- MCP or a Web API Server
- JSON schema for the AI to know the available functions/tools
- A knowledge base e.g. faq, internal abbreviations, naming convention.

The secondary/optional needs would be:
- Using custom RAGs
- Using Rerankers for a better knowledge retrieval

## How it works?

The LLM is supposed to create the correct SQL and pass it as a string argument to the tool available via function/tool calling. The rest is straight-forward, as the API will receive the raw SQL, execute and then fetch the data to respond to the assistant.

## Context engineering
- The context needed is the usage details of the database such as type, version, custom syntaxes or internal naming conventions etc.

## Knowledge base

The knowledge might be anything that’s useful for AI to generate the correct SQL. The well structured knowledge for a optimized indexing is always better. Imagine that you look for a term in two dictionaries where one is sorted and the other is not, which and why you’d prefer is the same for AI.

## Cost and timing

The cost would dependend on the app architecture design.

The timing is mostly dependent on the MCP/API server speed. Moreover, the app might have a few back and forths because it works as a try and fail methodology. 


## The categorization / levels of the questions

|  Level  | Accuracy | # Table | # Join | Description |
|---------|----------|---------|----------|------------|
| Level 1 |    80%   |    1    |     -    | Requiring only one table |
| Level 2 |    60%   |  1-2    |    1-2   | Requiring at most two joins |
| Level 3 |    40%   |    2-4  |    2-4   | Requiring at least one join and three tables |


## Conclusion

Automating the process of Data retrieval/Analysis is a new challenge for Generative AI agents.

Automating would fasten the productivity but surely it has caveats such as correctness and precision.

The better schema structure the company have, the easier, faster and more correct results the app/agent yields. 

## Recommendation for builders

First in first, to be able to automate the process for the data self serve purposes, the app owner should at least have an intermediate level of knowledge about the available data and the schema. Thus, the developer must be able to write an intermediate level SQL query for a random data question.

If the builder doesn't have enough knowledge on the schema, the assistant that they are about to build couldn't produce trusted results for test cases.
