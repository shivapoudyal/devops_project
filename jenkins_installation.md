******************************* Intall JAVA & Set home_path ***************************

sudo apt install default-jre            
sudo apt install openjdk-11-jre-headless
sudo apt install openjdk-8-jre-headless

******************************* Setting the JAVA_HOME Environment Variable ************************
 
 sudo update-alternatives --config java

********Copy the path from your preferred installation and then open /etc/environment using nano or your favorite text editor ********
sudo nano /etc/environment

********** put your copied desired java path into enviroment file, for eg- **********

JAVA_HOME="/usr/lib/jvm/java-8-oracle"

*************************************** Save and exit the file, and reload it *********************************
source /etc/environment

***********************You can now test whether the environment variable has been set by executing the following command ********************

echo $JAVA_HOME


************************************* JENKINS INSTALLATION (Jenkins Debian Packages) **************************************

wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -

******************************* Then add this entry in your /etc/apt/sources.list (jenkins package) *****************************

deb https://pkg.jenkins.io/debian-stable binary/

******************************** Now, Update the package & Install Jenkins ***********************************
 
 sudo apt-get update
 sudo apt-get install jenkins
 
 Jenkins, is installed, it runs to 8080 port,
 
******************************** Add JDK in JENKINS ***********************************

go to ->manage jenkins->Global Tool Configuration->add jdk (jdk name = JAVA_HOME, JAVA HOME = jdk path)


