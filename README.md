# Devin Ingersoll 

## Current
- I am a senior at Northwest Missouri State University. 
- I finishing up my Cyber Security Bachelor's of Science Degree.

## Background
- I have obtained the CompTIA Network+ certification
- I obtained my Associate of Arts Degree at Metropolitan Community College of Kansas City.
- Some hobbies of mine include: 
  - Messing around with Linux computers 
  - Video Games 
  - Cooking

## Plans
- I hope to get a job working as a Penetration Tester

## Notes 
### Bash
#### tr
- transforms specified character(s) into new ones
- ex: tr ' ' '\12' 
- this changes spaces into return characters (\12)
#### curl 
- this command downloads webpages (full source) 
- can be > outputed into files for data manipulation
#### sort
- this command sorts a file or standard input (>) 
- -n flag means sort by numeric
- -r flag means sort in reverse
#### uniq 
- this command removes all duplicate lines in a file or stdin (>) 
- -c flag adds numbers before each entry of how many times a string was duplicated
#### cat 
- this command prints out a file to stdout 
- can be used to send full files to stdin (>) 

### Powershell
#### Kafka
- first to start the kafka server: (window will stay open) 
~~~powershell
.\bin\windows\kafka-server-start.bat .\config\server.properties
~~~
- after that, start zookerper: (window will stay open)
~~~powershell
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
~~~
- Changed the server.properties file to change to another port (just for testing)
~~~powershell
vim .\config\server.properties
#changed this line's port from 9092 to 3989
listeners=PLAINTEXT://:3989 
~~~
- After changing this file you need to start the topic server using the configured port (topic can be anything) 
~~~powershell
.\bin\windows\kafka-topics.bat --zookeeper localhost:3989 --replication-factor 1 --partitions 1 --create --topic TOPIC 
~~~
- now that the port is open you can test if it's running with these two commands 
~~~powershell
.\bin\windows\kafka-console-producer.bat --broker-list localhost:3989 --topic TOPIC
> you can put in test input here
______________________________Another Powershell Window_________________
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:3989 --topic TOPIC --from-beginning    
text you type in the producer will show up here
~~~
- You can list each different topic by:
~~~powershell
.\bin\windows\kafka-topics.bat --zookeeper localhost:3989 --list
~~~


## Links
- [Linkedin](https://www.linkedin.com/in/devin-ingersoll/)  
- [Shell data project](https://github.com/deviningers/shell-big-date)
