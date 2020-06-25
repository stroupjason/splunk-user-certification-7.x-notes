# Notes for Module 2

- What is Splunk?
- Module 2 Quiz

# 5 main functions of splunk enterprise

1. Index Data
2. Search & Investigate
3. Add knowledge
4. Monitor & Alert
5. Report & Analyze

- "Available, accessible, and usable" to everyone in the org

### Index Data

- collects data from any source
- i.e. like a factory on a conveyor belt
  - the data is processed and labeled into single events
  - time stamps i.e. are "normalized" (like a JSON object)

### Search & Investigate

    - you can search events that contain values across multiple data sources e.g.
        - user login, item viewed, server error, 404 error, https request errors etc
    - this allows you to analyze and run statistics use the splunk search language

### Add knowledge

    - this allows to add how you interpret your data - add labels essentially
        - add "enrichment" normalize it so you can store this in a report for later use

### Monitor & Alert

    - proactively monitor the infrastructure in real time to identify issues, problems and attacks before they impact any customers or services e.g. server error
    - can create alerts to monitor for specific conditions and respond to issues automatically with a variety of actions

### Report & Analyze

    - data vizualation
    - allowing all functions across the org and "empowering them" to see and receive the information they need, "organized into a single pane of glass"

# Components

- There are 3 main components:

1. Indexers
2. Search Heads
3. Forwarders

### 1. Indexers

- process incoming machine data and storing those results as events
- these events are logged and stored in dir by classification "age" so the folder has a "timestamp" with the events
- allows you to narrow down a search - similar to kibana elastic search

### 2. Search Heads

- allows users to search the splunk data
- e.g. `sourcetype=access_combined action=purchase status=200`
- this search then distrubutes the request to the indexers which perfoms the search on the data (db)
- provides a lot of tools e.g. dashboards, reports and vizualizations

### Forwarders

- splunk enterprise instances
- they consume data and forward it to the indexes for processing
- requires minimal resources
- little impact on performance
- resides usually on your local machine where the data originated
- e.g. - linux web server - you would install a forwarder on that server and it would sent data to the indexer
- in most splunk deployments, forwarders serve as the primary way data is supplied for indexing

# How it Scales

- multiple ways, single instance to a full distributed infrastructure

1. Single-Instance Deployment

   - hanldes all the functions of splunk:
     - Inputs
     - Parsing
     - Indexing
     - Searching
   - Why would You want to use a single instance?
     - Proof of concept
     - personal use
     - learning
     - might serve the needs of small deparment-sized environments

2. Production Environment
   - You would have to split the functionality of inputs, parsing, indexing, and searching up across multiple specialized instance and adding forwarders to send data to indexers and then adding multiple serach heads and indexers to increase indexing and search capacity
   - serach heads and indexer can also be clustered
     - this makes sure that the data is always available and searchable

Elapsed time: 28min 13s

# Module 2 Quiz

1. A single-instance deployment of Splunk Enterprise handles:

- Input
- Searching
- Parsing
- Indexing

2. In most Splunk deployments, **\_\_\_\_** serve as the primary way data is supplied for indexing

- Forwarders

3. Search requests are processed by the \***\*\_\_\_\*\***.

- Indexers

4. What are the three main processing components of Splunk?

- Search Heads
- Forwarders
- Indexers

5. Which function is not a part of a single instance deployment?
   [X] Clustering
   [ ] Indexing
   [ ] parsing
   [ ] Searching
