# Jenkins-Setup



Get the LTS war 2.73 or above from https://jenkins.io/download  
run it using 
java - jar <downloaded_filename>

It will create Jenkins home as a hidden folder in the current user home directory 

First time it gives setup wizard it will generate random unlock password & suggest plug-ins. You can add an admin user use job import plug in to get jobs on other Jenkins but disable those until u set up required tools under Jenkins tools->Configure tools required for your builds such as maven, allure etc...

Then comes the job of troubleshooting your jobs & making builds successful

## Optional
Configure Jenkins to use HTTPS and the JKS keystore
Copy your Jenkins *.jks keystore file to your Jenkins server.  You can put the keystore file into your JENKINS_HOME folder for convenience.

Edit the jenkins.xml file (installed into %PROGRAMFILES{x86)%/Jenkins/jenkins.xml by default on Windows) and change the following arguments being passed to java when launching jenkins:

--httpPort=-1  (to stop Jenkins from listening over plain HTTP)
--httpsPort=443  (or 8443 or whatever SSL port you want Jenkins to listen on)
--httpsKeyStore="%JENKINS_HOME%\jenkins.example.com.jks"
--httpsKeyStorePassword="<cleartext-password-to-keystore>"
Private key and JKS keystore passwords
When creating the JKS keystore, the destination keystore password (e.g. JKS) must match the source keystore password (e.g. the password for the .pfx).
  
![Thread Lifecycle](https://github.com/praveen-cimplicity/Jenkins-Setup/blob/master/Thread_Lifecycle.jpg)
