- the fields that are extracted at index time are the most powerful:

1. index
2. source
3. host
4. sourcetype

- these searches will not need to be extracted every time

- inclusions vs exclusion

### Using Time

- date set picker
- real time searcher
- limit the results between the time selected
- Advanced time search
- @ symbol used to round down i.e. `-30m@h`
- `sourcetype=access_combined earliest=-2h latest=-1h`

### Indexes

- filter events early in searches
- splunk admins may often use multiple indexes to segregate data
  - ie. web data and security data indexes
  - limit access for security purposes for some users
- can search multiple indexes at the same time

### Module 7 Quiz

1. What is the most efficient way to filter events in Splunk?
   [X ] By time.
   [ ] Using booleans.
   [ ] With an asterisk.

2. This symbol is used in the "Advanced" section of the time range picker to round down to nearest unit of specified time.

[ ] %
[ ] &
[ ] \*
[X ] @
[ ] ^

3. Time to search can only be set by the time range picker. T/F
   False

4. Having separate indexes allows:
   Select all that apply.

[ X ] Ability to limit access.
[ X ] Faster Searches.
[ X ] Multiple retention policies

5. As a general practice, exclusion is better than inclusion in a Splunk search. T/F
   False

![Module 7 Quiz Results]()
