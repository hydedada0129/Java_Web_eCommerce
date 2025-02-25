# Java_Web_eCommerce
OS:Ubuntu 20.04
IDE:Eclipse 4.34.0
Java --version 
  openjdk 11.0.25 2024-10-15
  OpenJDK Runtime Environment (build 11.0.25+9-post-Ubuntu-1ubuntu120.04)
  OpenJDK 64-Bit Server VM (build 11.0.25+9-post-Ubuntu-1ubuntu120.04, mixed mode, sharing)


Tomcat 9.0 installation: 
Apache Tomcat 9.0 requires a Java Standard Edition Runtime
Environment (JRE) version 8 or later.

download from https://tomcat.apache.org/download-90.cgi
choose tar.gz (pgp, sha512)

Unpack the binary distribution
  tar -xfv apache-tomcat-9.0.100.tar.gz
  
Tomcat 9.0 installation document:RUNNING.txt
Configure Environment Variables:
Tomcat is a Java application and does not use environment variables directly.
The CATALINA_HOME environment variable should be set to the location of the
root directory of the "binary" distribution of Tomcat.
The CATALINA_BASE environment variable specifies location of the root
directory of the "active configuration" of Tomcat. It is optional. It
defaults to be equal to CATALINA_HOME.
Set JRE_HOME or JAVA_HOME (required)
These variables are used to specify location of a Java Runtime
Environment or of a Java Development Kit that is used to start Tomcat.
The JRE_HOME variable is used to specify location of a JRE. The JAVA_HOME
variable is used to specify location of a JDK.
If both JRE_HOME and JAVA_HOME are specified, JRE_HOME is used.

test tomcat:
Start Up Tomcat:
~/apache-tomcat-9.0.100/bin$ ./startup.sh
http://localhost:8080/ 
copy above URL and paste into your browser. you will see 
"If you're seeing this, you've successfully installed Tomcat. Congratulations!"
Shut Down Tomcat:
~/apache-tomcat-9.0.100/bin$ ./shutdown.sh

find Java installed path:
sudo update-java-alternatives -l
/usr/lib/jvm/java-1.11.0-openjdk-amd64

add JAVA_HOME(Java JDK installed path)
~$ vim .bashrc
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64

Setup Tomcat 9 in Eclipse:
perspective -> Java EE -> reset
Windoew->preferences->Server->Runtime environments->add->Apache->Apache Tomcat v9.0->Browse->select the installed path of your Tomcat 9 directory->finish->apply and close

Launch Tomcat on Eclipse:
Servers->click the link to create a new server->Apache->Apache Tomcat v9.0->finish
under Servers->right click Tomcat v9.0 Server at localhost->start

Create a new Dynamic Web Project:
right click on Project Space->new->Dynamic web project->enter project name->next->next->finish

Run dynamic web project on tomcat in eclipse:
right click on the project name->run as->run on server->choose an existing server->check:Always use this server when running this project->finish(click Servers tab's Tomcat v9.0 Server at localhost->TestWeb [Synchronized])





