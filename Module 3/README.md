# Installing Splunk on your machine

https://docs.splunk.com/Documentation/Splunk

- Linux
- Windows
- OSX
- Splunk Cloud
- Apps and Roles

* RECOMMENDED: DO NOT INSTALL SPLUNK AS THE ROOT USER

### Linux

- wget

### Windows

- have an option to use a GUI or cmd
- wget is also available
- custom settings options: change location, what account type, local or domain account (remote log in)
- set administrative password
- short cut options

### OSX

- (https://www.splunk.com/en_us/download/get-started-with-your-free-trial.html#tabs/macos)

* two options:

  1. .tgz file
     - archive of the splunk directory installing anywhere you want on your system
     - this way you can match your production environment (not needed for this tutorial)
  2. dmg file (recommended installation for training/ learning)
     - disk image file
  3. wget cmd download as well

* Commands in the command line

./splunk start
./splunk stop
./splunk restart
./splunk help

![splunk enterpise local host interface]()

### Splunk Cloud

- subscriptions services
- removing infrastructure rquirements on your cloud
- trial will index 5GB per day, but only for 15days
- (not recommended for this course)

### Apps and Roles

#### Apps

- apps in the splunk enterprise interface are preconfigured env that sit on top of each enterprise instance
- extends pre built knowledge and capabilites
- e.g. lik workspaces built to solve a specific use-case
- the apps you see are defined by a user with an administrator role
- https://splunkbase.splunk.com/
  - there are DevOps, IT Operations, Security, Business Analystics, IoT, Utilities and more

#### Roles

- determines what a user is able to see, do and interact with
- 3 are 3 main types of roles:
  1. Administrator
     - can install apps and create knowledge objects for all users
  2. Power
     - can create and share knowledge objects for suers of an app and do realtime searches
  3. User
     - can only see their own knowledge objects and those shared with them

The coursework will be done with the "power" user role

THer are 100s of apps that you can pull down

# Module 3 Lab

[insert hosted pdf here](Module 3/SplunkFundamentals1_module3.pdf)

# Module 3 Quiz

1. This role will only see their own knowledge objects and those that have been shared with them. [] Power [] Admin [X] User

2. What are the three main default roles in Splunk Enterprise?
   [X] Power [X] Admin [X] User [] Manager [] King

3. The password for a newly installed Splunk instance is:
   [] Randomly generated.
   [] Your email address.
   [X] Created when you install Splunk Enterprise.
   [] Available from the splunk.com website.

4. You can launch and manage apps from the home app. T/F
   True

5. ****\_**** define what users can do in Splunk.
   [] Tokens
   [] Disk permissions
   [X] Roles

Elapsed time: 4min
