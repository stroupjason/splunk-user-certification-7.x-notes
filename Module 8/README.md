# The Splunch Search Language (SPL)

### 1) Search Syntax

### 2) Vivual Pipline

### 3) Limits Explained

### 4) Fields Command

### 5) Table Command

### 6) Rename Command

### 7) Dedup Command

### 8) Sort Command

### 1) Search Syntax

    1) Serach Terms
    2) Commands
    3) Functions
    4) Arguments
    5) Clauses - how you want data grouped or defined

    i.e. `sourtype=acc* status=200 | stats list(product_name) as "Games Sold" | top "Games Sold"`

     *pipes are used to pass the current component to the next component

### 2) Vivual Pipline

- color coded command an command arguemts and function displayed in cordinating colors
- can move a pipe or a line to another line
- you can set a theme as well
  - setting in advanced editor

### 3) Limits Explained

- left to right search terms piped into searhch commands is one of the most important features/concepts in splunk language
- when you search your splunk index, splunk reads the result from yoru disk and makesa copy in memory , removing events tahat were not in search results
- once an item is removed for the search result the command is no longer available to subsequent search commands

### 4) Fields Command

- what are some commands that help us work with our data in a more useful way?
  - useful to limit fields displayed and can make searching faster
- field inclusion happens before field extraction and can improve performance

### 5) Table Command

- similar to fields where that specified fields are kept in your results the only difference here is that table command retains the information in a tabular format
- to rearrange columns all you have to do is rearrange the order of the commands in the SPL query

### 6) Rename Command

- used to rename fields
- once renamed the orignal name for your field is no longer available to susequen search commands
- you will need to use the new field names to be used further down the pipeline
- note: need to wrap the name in a quotes if it is a phrase - if not SPL will not see it as an available field

### 7) Dedup Command

- removes duplicate events with duplicate events
-

### 8) Sort Command

- display resutls in ascending or descending order
- string data is sorted alphanumerically
- numeric data is sorted numerically
- by default - a given field is sorted by ascending order

- a `-` with show descending order
- when there's a pace between your field the operator and the function then it will effect all field name in the query

- limit argument (pagination)

# Module 8 Quiz

1. Finish the rename command to change the name of the status field to HTTP Status.
   [ ] status to "HTTP Status"
   [ ] as "HTTP Status"
   [ ] status as HTTP Status
   [X ] status as "HTTP Status"

2) Which command removes results with duplicate field values?
   Select your answer.

[ X] Dedup
[ ] Distinct
[ ] Join
[ ] Limit

3. What command would you use to remove the status field from the returned events? (`sourcetype=a* status=404 | _______ status`)
   Select your answer.

[ ] fields
[ ] not
[ ] table
[ X] fields -

4. What is missing from this search? `sourcetype=a* | rename ip as "User IP" | table User IP`
   Select your answer.

[ ] Search terms
[ X] Quotation marks around User IP.
[ ] A table command.
[ ] A pipe.

5. Would the ip column be removed in the results of this search? Why or why not?
   Select your answer.

[ ] Yes, because a pipe was used between search commands
[ ] No, because table columns can not be removed.
[ ] Yes, because the negative sign was used.
[X ] No, because the name was changed.

![Module 8 Quiz Results]()
