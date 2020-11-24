# IPL_DATABE

## HOW TO RUN THE QUERIES
* Step-1 : Start the docker 
```
$ docker start container_id
```
* where the container_id is the id of the container you have created in docker.
Eg: 
    docker start learn_sql
* Step-2 : Dump the dumpipl.sql file into MySQL
```
$ mysql -h 127.0.0.1 -u root --port=5005 -p  < dumpipl.sql
```
Here 5005 is the port number on which the mysql is runnig.
After entering the command you will get something like:

* Enter password:

* then enter the password of the docker container.

* This command may take a while .

Step-3 : run the python file ipl.py using the command :-
```
$ python3 ipl.py
```
Step-4 : After runnig the python file you get something like this :

* Username: 
* Password:

* On these enter the root (which is usually the case) in the Username and enter the password of MySQL in the password.

* If u have entered correct credentials it shows up a message "Connected".

* Now you are able to use the interface to run the queries.

## Details about the DATABASE

1. We have developed quite a friendly USER INTERFACE to let the user run queries. We have options like functionalites which include queries like selection , projection , aggregate , Search. We have analyzed data to  obtain results. We have modification functionalities : INSERT , DELETE , UPDATE. 

2. The Average_runs attribute of the relation BATSMAN is derived from the Matches_played attribute in PLAYER table and Number_of_runs attribute in the BATSMAN relation.  We are taking user input for Averae_runs attribute we have calculated by using the above mentioned attributes.

3. We have queries like "Maximum runs scored in the IPL season" , "Maximum wickets taken in the IPL season" and "Determing the type of pitch" in the analysis part. We have used joins across tables to get the required information . We have used tables : PLAYER , BATSMAN , BOWLER , VENUE , MATCHES etc. We are determing the type of pitch(Batting pitch / Bowling pitch) by the average runs scored in that particular venue. If the average is less than 150 then it is a bowling pitch otherwise it is a batting pitch. 

4. We are calculating the average runs by a team by using join between the relations TEAM , MATCHES.

5. After updating insertion of every match we are updating the matches played in the corresponding teams and updating the scores of the players participated in the match. 
