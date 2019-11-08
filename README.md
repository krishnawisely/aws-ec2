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
- Then finally install jdk new version
  > ``` sudo yum install java-1.8.0-openjdk-devel ```
