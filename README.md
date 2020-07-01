# Jenkins-Setup



Get the LTS war 2.73 or above from https://jenkins.io/download  
run it using 
java - jar <downloaded_filename>

It will create Jenkins home as a hidden folder in the current user home directory 

First time it gives setup wizard it will generate random unlock password & suggest plug-ins. You can add an admin user use job import plug in to get jobs on other Jenkins but disable those until u set up required tools under Jenkins tools->Configure tools required for your builds such as maven, allure etc...

Then comes the job of troubleshooting your jobs & making builds successful
