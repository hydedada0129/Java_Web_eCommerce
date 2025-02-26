# Java_Web_eCommerce
# my laptop:
OS:Ubuntu 20.04<br />
IDE:Eclipse 4.34.0<br />
openjdk 11.0.25 2024-10-15<br />
OpenJDK Runtime Environment (build 11.0.25+9-post-Ubuntu-1ubuntu120.04)<br />
OpenJDK 64-Bit Server VM (build 11.0.25+9-post-Ubuntu-1ubuntu120.04, mixed mode, sharing)<br />
# Tomcat 9.0 installation: <br />
Apache Tomcat 9.0 requires a Java Standard Edition Runtime<br />
Environment (JRE) version 8 or later.<br />

### download
download from https://tomcat.apache.org/download-90.cgi<br />
choose tar.gz (pgp, sha512)<br />
Unpack the binary distribution<br />
  tar -xfv apache-tomcat-9.0.100.tar.gz<br />
Tomcat 9.0 installation document:RUNNING.txt<br />

### test tomcat:<br />
Start Up Tomcat:<br />
~/apache-tomcat-9.0.100/bin$ ./startup.sh<br />
http://localhost:8080/ <br />
copy above URL and paste into your browser. you will see <br />
"If you're seeing this, you've successfully installed Tomcat. Congratulations!"<br />
Shut Down Tomcat:<br />
~/apache-tomcat-9.0.100/bin$ ./shutdown.sh<br />

### find Java installed path:<br />
sudo update-java-alternatives -l<br />
/usr/lib/jvm/java-1.11.0-openjdk-amd64<br />
add JAVA_HOME(Java JDK installed path)<br />
~$ vim .bashrc<br />
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64<br />

# Setup Tomcat 9 in Eclipse:<br />
perspective -> Java EE -> reset<br />
Windoew->preferences->Server->Runtime environments->add->Apache->Apache Tomcat v9.0->Browse->select the installed path of your Tomcat 9 directory->finish->apply and close<br />

### Launch Tomcat on Eclipse:<br />
Servers->click the link to create a new server->Apache->Apache Tomcat v9.0->finish<br />
under Servers->right click Tomcat v9.0 Server at localhost->start<br />

### Create a new Dynamic Web Project:<br />
right click on Project Space->new->Dynamic web project->enter project name->next->next->finish<br />

### Run dynamic web project on tomcat in eclipse:<br />
right click on the project name->run as->run on server->choose an existing server->check:Always use this server when running this project->finish(click Servers tab's Tomcat v9.0 <br />Server at localhost->TestWeb [Synchronized])<br />

### Check dynamic web project's properties:<br />
resource->text file encoding->click inherited from container(UTF-8)<br />
Java compiler->make sure they are set correctly<br />
Java build path->libraries<br />
Server-><br />
Project Facets->click 'Java'->runtimes<br />
Deployment Assembly-><br />

Done!<br />





