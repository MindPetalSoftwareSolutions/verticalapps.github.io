# Configuring your AWS Cloud9 instance for Java

1. [Java User Guide](https://docs.aws.amazon.com/cloud9/latest/user-guide/sample-java.html)
1. Create instance
1. Update Java

```
sudo yum -y update
sudo yum -y install java-1.8.0-openjdk-devel
sudo update-alternatives --config java
sudo update-alternatives --config javac
```
4. Install Maven
```
sudo wget http://repos.fedorapeople.org/repos/dchen/apache-maven/epel-apache-maven.repo -O /etc/yum.repos.d/epel-apache-maven.repo
sudo sed -i s/\$releasever/6/g /etc/yum.repos.d/epel-apache-maven.repo
sudo yum install -y apache-maven
```
5. Create Maven Project
```
mvn archetype:generate -DgroupId=com.verticalapps.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```
