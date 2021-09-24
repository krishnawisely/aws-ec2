# AWS EC2
### Machine login with CMD
#### Step 1:
Login
> ``` ssh -i /path/my-key-pair.pem ec2-user@your public DNS name  ```
#### Step 2:
- Check java version
  > ``` java -version ```
- Remove jdk from your machine
  > ``` sudo yum remove java-1.7.0-openjdk ```
- Install jdk new version
  > ``` sudo yum install java-1.8.0-openjdk-devel ```
- Install jdk 11
- > ``` sudo amazon-linux-extras install java-openjdk11 ```
#### Step 3:
- Download ApacheTomcat in machine
  > ``` wget http://mirrors.estointernet.in/apache/tomcat/tomcat-9/v9.0.27/bin/apache-tomcat-9.0.27.tar.gz ```
- Unzip ApacheTomcat
  > ``` tar -zxvf apache-tomcat-9.0.27.tar.gz ```
- Change directory to the bin
  > ``` cd apache-tomcat-9.0.27/bin ```
- Finally start server
  > ``` sh startup.sh ```
#### Step 4:
- Add user role in tomcat-users.xml
  > ``` cd conf/ ```
- Open with editor
  > ```vi tomcat-users.xml ```
- Add following details
  > ``` 
  > <role rolename="manager-gui"/>
  > <user username="krishna" password="krishna" roles="manager-gui"/>
  > ```
- Change directory using following command
  > ``` cd webapps/manager/META-INF/ ```
- Open context.xml with editor
  > ``` vi context.xml ```
- Then command line following details in 
  > Command <Valve> and <Manager> tages.
