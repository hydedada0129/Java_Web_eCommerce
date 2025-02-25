# Java_Web_eCommerce
OS:Ubuntu 20.04<br />
IDE:Eclipse 4.34.0<br />
Java --version <br />
  openjdk 11.0.25 2024-10-15<br />
  OpenJDK Runtime Environment (build 11.0.25+9-post-Ubuntu-1ubuntu120.04)<br />
  OpenJDK 64-Bit Server VM (build 11.0.25+9-post-Ubuntu-1ubuntu120.04, mixed mode, sharing)<br />
Tomcat 9.0 installation: <br />
Apache Tomcat 9.0 requires a Java Standard Edition Runtime<br />
Environment (JRE) version 8 or later.<br />

download from https://tomcat.apache.org/download-90.cgi<br />

choose tar.gz (pgp, sha512)<br />

Unpack the binary distribution<br />
  tar -xfv apache-tomcat-9.0.100.tar.gz<br />
  
Tomcat 9.0 installation document:RUNNING.txt<br />
Configure Environment Variables:<br />
Tomcat is a Java application and does not use environment variables directly.<br />
The CATALINA_HOME environment variable should be set to the location of the<br />
root directory of the "binary" distribution of Tomcat.<br />
The CATALINA_BASE environment variable specifies location of the root<br />
directory of the "active configuration" of Tomcat. It is optional. It<br />
defaults to be equal to CATALINA_HOME.<br />
Set JRE_HOME or JAVA_HOME (required)<br />
These variables are used to specify location of a Java Runtime<br />
Environment or of a Java Development Kit that is used to start Tomcat.<br />
The JRE_HOME variable is used to specify location of a JRE. The JAVA_HOME<br />
variable is used to specify location of a JDK.<br />
If both JRE_HOME and JAVA_HOME are specified, JRE_HOME is used.<br />

test tomcat:<br />
Start Up Tomcat:<br />
~/apache-tomcat-9.0.100/bin$ ./startup.sh<br />
http://localhost:8080/ <br />
copy above URL and paste into your browser. you will see <br />
"If you're seeing this, you've successfully installed Tomcat. Congratulations!"<br />
Shut Down Tomcat:<br />
~/apache-tomcat-9.0.100/bin$ ./shutdown.sh<br />

find Java installed path:<br />
sudo update-java-alternatives -l<br />
/usr/lib/jvm/java-1.11.0-openjdk-amd64<br />

add JAVA_HOME(Java JDK installed path)<br />
~$ vim .bashrc<br />
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64<br />

Setup Tomcat 9 in Eclipse:<br />
perspective -> Java EE -> reset<br />
Windoew->preferences->Server->Runtime environments->add->Apache->Apache Tomcat v9.0->Browse->select the installed path of your Tomcat 9 directory->finish->apply and close<br />

Launch Tomcat on Eclipse:<br />
Servers->click the link to create a new server->Apache->Apache Tomcat v9.0->finish<br />
under Servers->right click Tomcat v9.0 Server at localhost->start<br />

Create a new Dynamic Web Project:<br />
right click on Project Space->new->Dynamic web project->enter project name->next->next->finish<br />

Run dynamic web project on tomcat in eclipse:<br />
right click on the project name->run as->run on server->choose an existing server->check:Always use this server when running this project->finish(click Servers tab's Tomcat v9.0 <br />Server at localhost->TestWeb [Synchronized])<br />

Check dynamic web project's properties:<br />
resource->text file encoding->click inherited from container(UTF-8)<br />
Java compiler->make sure they are set correctly<br />
Java build path->libraries<br />
Server-><br />
Project Facets->click 'Java'->runtimes<br />
Deployment Assembly-><br />

Done!<br />





