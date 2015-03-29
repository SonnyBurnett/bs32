# bs32
(c) Taco Bakker

Simple build server for continuous integration demo.
Installation:
install Vagrant, Git and VirtualBox
clone this repository
cd to the directory with the Vagrantfile
type: vagrant up

***

With this extremely simple setup you can do the following:

Edit (with vim) a HelloWorld java servlet and change the text or the color
The java code is located at: /home/vagrant/demo/src/main/java

Push your code to git. A script is available to help you with this
If asked:  password = "admin"

Find out the ip address of your VM: with ifconfig

Go to your browser and type in the ip address followed by:
htttp://172.28.128.3:8080/jenkins    Note (change 172.28.128.3 for your local ip)

Also type in:
htttp://172.28.128.3:8480/HelloWorld

Jenkins will automatically be triggered by git, and will start building a new version
of the HelloWorld app
Check git:
htttp://172.28.128.3:8180/gitblit

After Jenkins is done you can refesh the HelloWorld app screen.
Jenkins has replaced the old version of the HelloWorld app with the new one. 
Note that this app is running in Tomcat. 

Your artifacts have been stored in Artifactory:
htttp://172.28.128.3:8380/artifactory

The quality of your java code has been checked by SonarQube:
htttp://172.28.128.3:9000

If you rather use Nexus than Artifactory:
htttp://172.28.128.3:8280/nexus

I have kept things very basic to demonstrate some principles of continuous integration. 
Please play with this and improve the setup to your own needs.
Have fun!