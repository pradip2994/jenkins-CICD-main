**node-todo-cicd**

sudo apt install nodejs ,

sudo apt install npm ,

npm install ,

node app.js 

**Automated CICD Pipeline for Node Js web application using AWS, Github Integration and webhook, Docker,Docker-compose and Jenkins.**

Generate the SSH keys for integrating  Jenkins project with your git repository. Use ssh-keygen command to create public and private keys in EC2.
1) Configuring GitHub
  Go to your GitHub account settings.
  Go to “SSH and GPG” keys, Add the public key that we created using ssh-keygen for Authentication.
2)  For Installing GitHub Integration plugin in Jenkins
  1.In jenkins dashboard.
  2.Click on the “Manage Jenkins” button 
  3.Click on “Manage Plugins”
  4. Install “GitHub Integration” plugin
3) For GitHub-Webhook:
  1.Go to your GitHub repository and click on Settings.
  2.Click on Webhooks and then click on Add webhook.
  3. In the ‘Payload URL’ field, paste your Jenkins environment URL. At the end of this URL add /github-webhook/. In the ‘Content type’ select: ‘application/json’ and leave the ‘Secret’ field empty.
4) Configuring Jenkins:
  1. Create a jenkins job
  2. Create node-todo-app freestyle project
  3. In Configure, GitHub project URL paste project GitHub URL
  4.In Git, add credentials for jenkins
  5. Add the private key which we created using the ssh-keygen command in EC2.
  6. Click on the ‘Build Triggers’ tab and tick on the ‘GitHub hook trigger for GITScm polling’.
  7. Then save it.
  8.  Make the changes to the existing file in github repo or  Create the new file.
  9. See Output.

![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/7ad72692-b93d-4c02-b83a-053fc0d2fa2f)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/06ee70db-2fdb-41ad-84e3-2b53c4a3d25e)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/954cc886-5199-4f28-98be-3eb6242a5aa2)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/6d83d36e-0ed4-4242-a236-4331f2758caa)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/84ddcd7e-7fc5-47e0-8e1f-5a93c4040d52)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/6a5d7f5b-d153-459f-8416-5fb5c6d7e6d8)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/06665804-5c2d-406e-beb4-5aea2dbc7e80)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/c6d76680-da93-4dd6-964a-e0bf545d5dc7)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/8a24a387-fa11-4533-a6d0-8576347e52c9)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/de1b1e4b-d8ef-47b8-a72f-c90fec9a5469)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/a77e6e14-299b-44f6-8528-f4a670a89c98)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/3a8cb2f6-5851-4eb7-a85d-98983dbe2ccb)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/01f006e5-249c-4b77-89d7-28034c790489)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/da389f0e-3bae-48fd-87ee-5d132e92ba5e)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/03d413d9-15bc-41d0-a744-4c13d8d8c7ad)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/9c4cb53f-f729-4959-8832-e550d4346571)


**Created a Docker-integrated Jenkins declarative pipeline.**

1) Go to jenkins UI
2) Click on “ New items ”
3) Add name, click on “pipeline”
4) In ‘ General Section’ add Description
5) Tick ‘ Github project’ , add URL of github Repository.
6) In Pipeline section, Select ‘ Pipeline Script’
7) Write Script and Save
8) Now click on “ Build” , see the Stage View.


![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/ece0a902-5958-442b-8abe-87dc77d10c19)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/35539d07-8d2a-4bc7-817b-9675cae34067)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/5eeb498f-a4a5-426d-8363-836a4c6b503a)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/635a8e8a-258b-4689-b666-c140a9666d67)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/d53c6624-1b5d-45ca-b4b8-338782ec5d73)



**Created Jenkins agent and deployed Django web application through Jenkins Master server to Jenkins agent.**

1) Create 2 EC2 instances for master and agent
2) Generate SSH keys on “Jenkins-master” EC2 instance
3) Add public key from “Jenkins-master” instance to “Jenkins-agent” instance under location “.ssh/authorized_keys”
4) Create an agent by setting up a node on Jenkins
5) Click on “Nodes and Clouds”
6) Click on New Node.
7) Add details of your node, accordingly.
8) Launch Method: Launch agent via SSH.
  Host: <ip_address>
  Add credentials for jenkins
  Kind: SSH Username with Private key.
  ID: username
  Add the private key that we created in 'jenkins-master' and save.
9) Below we select Ubuntu for "Credentials".
10) Click on 'save' that will create a node.
11) You can see agent will be connected and online.


![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/2d84729b-6fa1-4c3d-8a96-e7127f04de3c)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/75c9012d-c746-4ce3-bbb6-51c9d71c13e2)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/12bf78ab-18be-4342-a146-90bbd8b6b422)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/a51435d8-208b-4110-a735-1a26041468ab)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/51db0ce7-6c96-44d0-a883-3e92c69eea05)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/84de340c-8ab4-44fd-8023-656964f790d5)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/07107521-4d6e-4309-9bd7-6f1b9617991f)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/b8ddc21d-58a5-41e7-97ce-0c8286d4f069)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/0664f253-ee8c-426a-827e-7a61e528e497)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/47ea14f1-b1d2-488e-b8c7-5160d08be670)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/c3f1cc8f-7bc0-456f-95bf-b0abb3fae3f2)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/e7c83c59-8efc-4f9c-9905-82d31faca732)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/2913d260-d11b-48f7-aa5e-56e3f31d2f70)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/77ce85f3-49a4-4884-80fa-84dabe34e88b)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/f792713c-2856-4a4b-a078-8ae7ae5e3baf)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/a60d95ab-857f-45bc-8128-c99f9d27dd83)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/e5fccce8-a81b-4578-9ea7-21aedb65536b)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/ff5476c9-a5e4-4ecb-9ab1-4eaf5e9e8d32)
![image](https://github.com/pradip2994/jenkins-CICD-main/assets/124191442/33d8a198-8923-4ad1-a1ba-addfa74dd3e0)


