# FSRIO
Data automation for USDA FSRIO to parse and scrape data from multiple sources for their food safety Research Projects Database

Dependencies:  
1. Maven 3.0 or higher  
2. JDK 1.8  

Before running, please ensure that the configuration file (process.cfg) is set up properly, specifically that the MySQL host, database and username, output and log folders have been specified correctly.  

There are default values for all other options, but ensure that the values are what you want them to be.  

## Building and Running from Scratch

This is the maven build of the project. To install and run:

1. Clone the directoy to your  local drive.
2. cd into FSRIO/jbt
3. Compile using "mvn compile"



For running upload:
	mvn exec:java -Dexec.mainClass="com.jbt.Run" -Dexec.args="process.cfg password upload"

For running scraping: 
 	mvn exec:java -Dexec.mainClass="com.jbt.Run" -Dexec.args="process.cfg password scrape"



## Using prebuilt jar file

To build mvn executable, run the following in /fsrio/jbt: mvn install  
The jar file will be places in /fsrio/jbt/target. Make sure to move it to /fsrio/jbt.  


To avoid compiling, the executable jar can be used to run the program as follows:  
1. Clone the directoy to your  local drive.  
2. cd into FSRIO/jbt  


For running upload:
	java -jar fsrio.jar "process.cfg" "password" "upload"

For running scraping: 
 	java -jar fsrio.jar "process.cfg" "password" "scrape"

## How to open the output tab-delimited files in Excel  
1. Open Excel, go to "Data" tab.  
2. Click "From Text".  
3. Choose the appropriate file.  
4. Click next, then select tab as the delimiter.
5. Click Finish.
