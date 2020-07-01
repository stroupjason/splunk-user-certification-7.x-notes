# Search and Reporting App

### 1) Search App

### 2) Using Search

### 3) Events

### 4) Search Everything

### 5) Module 5 Lab

### 6) Module 5 Quiz

### 1) Search App provides a default app for searching and analyzing data and helps create the following:

1. knowledge objects
2. reports
3. dashboards
4. more

- There are 7 main components to the search:

1. splunk bar (nav bar)
2. app bar - navigate the app
3. global search - ie search string
4. time picker
5. how to search panel
6. what to search panel - shows results that are indexed on the server
   - when clicking on the "data summary" button you get a full breakdown report of the indexed data by hosts, sources, and sourcetypes
7. search history menu

### 2) Using the Search Bar

- limiting a search by time is key to fster results and is a best practice

1. Patterns tab allows you to get a better understanding of what's happening with your data
2. if none of the above fields or searches work for you, then pivots, quick reports and search command docs will be displayed

- NOTE: Commands that create statistics and visualizations are called transforming commands.
- NOTE: by default, a search job will remain active for 10min, after that time you will need to run the results again
- NOTE: a shared search job will remain active for 7 days (shared with everyone)

- There are 4 types of file formats, raw, csv, xml or json

- there are 3 search modes to select from: 1) fast mode (2) smart mode (3) verbose mode

1. fast mode

   - cuts down on the information that's returned
   - field discovery is disabled in fast mode - only returns info on default fields - min required to get you your results returned

2. verbose

   -

3. smart mode
   - will toggle behavior and results based on the information you're quering

- note: selecting or zooming into events uses your original search job

### 3) Events

- you can use returned events to expand searches and interact with data
- showing newest events first
- remember that events are set based on your local time zone set in your account
- if you take your cursor and highlight a text, you have the option to add that field to your query and or exclude and launch a search with your input
- selecting info button - you'll see all the extracted events - you can run and advanced query by de-selecting or selecting your desired field events. This is out of this course's scope and is discussed in fundamentals II: https://www.splunk.com/en_us/training/courses/splunk-fundamentals-2.html

### 4) Search Everything

- you can use a wildcard `*`
- AND OR NOT ie. failed NOT password - this will yield a query where the events failed but not the password (passed)
- if no boolean is written AND is applied i.e. `failed password` === `failed AND password`
- bollean operation have an order of evaluation:
  1. NOT
  2. OR
  3. AND `
  4. NOTE: parenthesis are used to control the order of the evaluation i.e. `failed NOT (success OR accepted)` - evaluates success or accepted prior to quering failed
  5. exact phrases with quotes

### 5) Module 5 Quiz

1. What is the order of evaluation for Boolean operations in Splunk?
2. AND
3. NOT
4. OR

5. failed password === failed AND password. T/F

- True

3. Commands that create statistics and visualizations are called ******\_\_\_****** commands.

- transforming

4. Events are always returned in chronological order. T/F

- False (reverse chronological order)

5. When a search is sent to splunk, it becomes a **\_**.
   [ ] File on the host system
   [ X] Search job
   [ ] Event
   [ ] Task for Jimmy the Splunk elf

![Module 5 Quiz Results])()
