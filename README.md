wwc2019 logo
Women’s World Cup 2019 Graph Example
Description: Explore the data behind the Women’s World Cup with our World Cup Graph

model
Figure 1. Model
example
Figure 2. Example
Example Query:
MATCH (t:Tournament {year: $year})<-[:PARTICIPATED_IN]-(team)
RETURN team.name as team
Setup
This is for Neo4j version: 3.5,4.0

Required plugins: apoc

Rendered guide available via: :play https://guides.neo4j.com/sandbox/womens-worldcup/index.html

Unrendered guide: documentation/wwc2019.neo4j-browser-guide

Load graph data via the following:

Data files: import/*.json
Import flat files (csv, json, etc) using Cypher’s LOAD CSV, APOC library, or other methods.

Dump file: data/wwc2019-40.dump
Drop the file into the Files section of a project in Neo4j Desktop. Then choose the option to Create new DBMS from dump option from the file options.

Use the neo4j-admin tool to load data from the command line with the command below.

bin/neo4j-admin load --from data/wwc2019-40.dump [--database "database"]
Upload the dump file to Neo4j Aura via https://console.neo4j.io/#import-instructions

Data load script: scripts/wwc2019.cypher
bin/cypher-shell -u neo4j -p "password" -f scripts/wwc2019.cypher [-d "database"]
Or import in Neo4j Browser by dragging or pasting the content of scripts/wwc2019.cypher.

Code Examples
JavaScript

Java

C#

Python

Go
