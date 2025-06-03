Program 4

package com.example;

public class App {
    public static void main(String[] args) {
        System.out.println("Hello, Maven");
        System.out.println("This is the simple realworld example....");

        int a = 5;
        int b = 10;
        System.out.println("Sum of " + a + " and " + b + " is " + sum(a, b));
    }

    public static int sum(int x, int y) {
        return x + y;
    }
}

maven:- mvn clean install 
mvn exec:java -Dexec.mainClass="com.example.App"

gradle:-

gradle init

plugins {
    id 'java'
}

group = 'com.example'
version = '1.0-SNAPSHOT'

repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'junit:junit:4.12'
}

task run(type: JavaExec) {
    main = 'com.example.App'
    classpath = sourceSets.main.runtimeClasspath
}

gradlew build

gradlew run

Program 7
STEP 1: Configure Ansible Control Node
1. Create an administrator-level user for the control node. Use the adduser command:
sudo adduser [username]
2. When prompted, define a strong account password.
3. Use the following usermod command to assign superuser privileges to the account:
sudo usermod -aG sudo [username]
4. Switch to the newly created user on the control node:
sudo su [username]
STEP 2: Set up an SSH Key pair
1. Enter the command below using the Ansible control node command line:
   ssh-keygen
3. When prompted, provide a passphrase. While adding a strong passphrase is recommended, pressing Enter allows the user to skip the passphrase creation. The system generates the public/private key pair and prints the randomart image.
STEP 3: Configure an Ansible Host
1. Use the following ssh-copy-id command on the control node to copy the public key to a host:
ssh-copy-id [username]@[remote-host]
hostname -i
2. Type yes and hit Enter when asked whether to continue connecting to an authenticated host.
3. Enter the remote host account password.
STEP4 : Install Ansible
1. Ensure the package index is up to date
sudo apt update
2. Install Ansible on Ubuntu with the following command:
sudo apt install ansible -y
STEP 5: Verify the Installation
ansible --version
STEP 6: Set up the Inventory File
1. Create the ansible subdirectory in the etc directory:
sudo mkdir -p /etc/ansible
2. Use a text editor such as Nano to create a file named hosts:
sudo nano /etc/ansible/hosts
3. Add localhost that the control node will manage. Use the following format:
[local] localhost ansible_connection=local
Ctrl+S, Ctrl+X
4. Save the file and exit.
5. Enter the command below to check the items in the inventory:
ansible-inventory --list -y
STEP 7: Test the Connection To ensure the Ansible control node can connect to the local hosts and run commands, use the following ansible command to ping the hosts from the control node:
sudo ansible all -m ping

project 8: Exercise Project Solution: S
tep 1: Open GIT bash
Step 2: Create a directory with the following steps
mkdir maventest1
cd maventest1
Step 3: Create project
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

program 10
STEP1:On creating organization goto Organization settings goto Policy
And Allow Public Projects active
STEP2: GOTO GITBASH
TYPE COMMANDS AS IN BELOW
mkdir maventest1
cd maventest1
STEP3: to create simple hellow world maven project type command as in bmvn
archetype:generate \
-DgroupId=com.yourname \
-DartifactId=repo_name \
-DarchetypeArtifactId=maven-archetype-quickstart \
-DinteractiveMode=false
STEP4: to add files from local to github Follow the procedure
a) First create a repository in github as maventestazure
b) Then come to gitbash and type
git init
git add .
git commit -m “project created”
git branch -M main
git remote add origin https://github.com/amitdalvik/xyz.git
git push -u origin main
STEP5: Now goto Azure Devops Organization create Public Project
STEP6: SELECT PIPELINE and then click on create pipeline
STEP7: After creating Pipeline select type of repo as Github
STEP8: It asks for minimum signin verification after that ur screen be as in below select required repository there to run maven project 
STEP9: It again verifies signin verification of microsoft account You be able to see starter pipeline select for Maven
finally u will be able to see task running
The commits will also be visible in github

program 9
STEP1:Go to Google chrome and type azure for students
STEP2: Click on Start Free after that u get screen as in below
STEP3:Provide your email id at place of create account
STEP4:After password is set provide your First name Last name
STEP5: Verification code be mailed to the mentioned once kindly type it
STEP6:After code is verified as u got in the mail referred
U be given an option to solve puzzlegame
STEP7:This step is the important once where u fill your Academic Details properly where u provide College email id as in provided by your Individual colleges later the verification code again comes.After proper college email is given u get verification mail with link to mail u have provided
TO MAKE UR ACCOUNT SECURE IT AGAIN HAVE PUZZLE
Go To search and type Azure Devops
Click on Get started with Azure
After the click u get the screen of Get free need not to do anything just click on Signin 
Type Azure Devops
STEP8:Select Azure Devops Organization
STEP9:
After u opting for Azure Devops Organizations u get a screen as in below now
select My Azure DevOps Organizations
You will be able to see Organization is Created
Finally After Creating a New Organization
U can create Project of ur choice as per requiremen
