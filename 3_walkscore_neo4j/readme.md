# Walkscore computation using Neo4j graph algorithms

## Assemble Data Sets:

### Yelp data for amenities:

Use the Yelp Import tool to import data: https://github.com/johnymontana/yelp-graph-algorithms/tree/3.4 

* Download the JSON version of the https://www.yelp.co.uk/dataset/download[Yelp Dataset Challenge^] and extract it into the `dataset` directory

* Run the following command to create Neo4j Import Tool CSV files:

```
python json_to_csv.py
```

* Run the following command to extract cities, areas, and countries:

```
python lat_long_expansion.py
```

* Navigate to the Neo4j home directory and run the following command:

```
sh /path/to/import.sh

Neo4j version: 3.3.4
Importing the contents of these files into /path/to/data/databases/yelp.db:
```

* Update the neo4j.conf file to contain this line:

```
dbms.active_database=yelp.db
```

* Restart Neo4j and we're good to go