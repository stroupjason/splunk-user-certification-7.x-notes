# 1) TYPES OF INPUTS

# 2) UPLOAD INPUT

# 3) MONITOR INPUT

# 4) FORWADERS

# 5) Quiz

# TYPES OF INPUT - GETTING DATA IN

1. Upload - The upload option while logged in as an adminstrator allows the user to upload local files to a splunk enterprise index that only gets indexed once and never gets updated
2. Monitor - this option allows the user to monitor the files directories, http events, network ports, or data gathering sripts located on splunk enterprise instances
   - note: if you're in a windows env you would see local window host monitoring events as well - e.g. RMM, event logs, file system changes, active directory, network info on local machines
3. Forward - (most common) this option lets you receive data from forwarders. Again as a reminder, forwarders are installed on local machines to gather data and forward it to indexers on a receiving port

# UPLOAD INPUT

- splunk uses source types to categorize data so that it is indexed properly
- source type is used in many management functions
- if the data is recognized than it will assign it a pre-trianed source type e.g. "csv"
- when saving a source type the app context setting is important becuase it will tell splunk which app to apply it to i.e. "system"
- When setting the input you have additional parameters for the data, 3 options specifically for the host field value:
  1. constant value
  2. regex on path
  3. segment path
- set the host field value to "splunkServer1"
- for the index option you can select which one or create a new one

### Main Index

- allowing users to search one idex for all your data
- There are some instances and circumstances where you'd want seperate indexes. Having seperate indexes can help you search be more efficient e.g. `index=web_data_index fail*`

  1. Web Data Index
     - e.g. from the query above is `web_data_index`
     - limits the data amoutn splunk searches
     - returns events only from that index
     - multiple undexes allow limiting access by user role
  2. Main Index
  3. Security Index
     - this allows admin to control who sees what data

  - seperate indexes allow for custom retention policies

  - save the data to default
  - now hit start searching! (looks really similar to kibana elastic search)

# MONITOR INPUT

- this option is used when you have files and ports (similar to upload with a few differences):

1. Files and Dir
   - upload file
2. HTTP Event Collector
   - configure tokens that clients can use to send data over HTTP or HTTPS
3. TCP/UDP
   - configure splunk platform to listen on a network port
4. Scripts
   - get data from any API, service, or db with a custom script

- When selecting a file or dir you have the option to continuously monitor or index once if you're looking for events contuniously on a server then select the first option
- can whitelist or blacklist files in the dir

# FORWARDERS

- out of scope for this course - see documentation for more details: https://docs.splunk.com/Documentation/Splunk/latest/Data/Usingforwardingagents

# 5) Quiz

1. In most production environments, **\_\_\_** will be used as the source of data input.

- forwarders

2. The monitor input option will allow you to continuously monitor files. T/F

- True

3. Splunk knows where to break the event, where the time stamp is located and how to automatically create field value pairs using these.
   [X ] Source types
   [ ] File names
   [ ] Line breaks

4. Files indexed using the the upload input option get indexed **\_**.
   [ ] Every hour
   [ ] On every search
   [ ] Each time Splunk restarts
   [X ] Once

5. Splunk uses **\_\_\_\_** to categorize the type of data being indexed.

- source types

![Module 4 Quiz Results](https://raw.githubusercontent.com/stroupjason/splunk-user-certification-7.x-notes/master/img/quiz-4-results-2020-07-01.png)
