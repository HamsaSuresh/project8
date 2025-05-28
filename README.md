Program 4

package com.example;

public class App { public static void main(String[] args) { System.out.println("Hello, Maven"); System.out.println("This is the simple realworld example....");

    int a = 5;
    int b = 10;
    System.out.println("Sum of " + a + " and " + b + " is " + sum(a, b));
}

public static int sum(int x, int y) {
    return x + y;
}
}

maven:- mvn clean install mvn exec:java -Dexec.mainClass="com.example.App"

gradle:-

gradle init

plugins { id 'java' }

group = 'com.example' version = '1.0-SNAPSHOT'

repositories { mavenCentral() }

dependencies { testImplementation 'junit:junit:4.12' }

task run(type: JavaExec) { main = 'com.example.App' classpath = sourceSets.main.runtimeClasspath }

gradlew build

gradlew run

Program 7

sudo adduser [username]
When prompted, define a strong account password.
sudo usermod -aG sudo [username]
sudo su [username]
ssh-keygen
hostname -i
ssh-copy-id [username]@[remote-host]
sudo apt update
sudo apt install ansible -y
ansible --version
sudo mkdir -p /etc/ansible
sudo nano /etc/ansible/hosts
[local] localhost ansible_connection=local
Ctrl+S, Ctrl+X
ansible-inventory --list -y
sudo ansible all -m ping
project 8: Exercise Project Solution: Step 1: Open GIT bash Step 2: Create a directory with the following steps mkdir maventest1 cd maventest1 Step 3: Create project

mvn archetype:generate -DgroupId=com.yourname -DartifactId=repo_name-DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin "repo link"
git push -u origin main (error)
git pull origin main --rebase
git add
git push -u origin main 13. Go to pom.xml
