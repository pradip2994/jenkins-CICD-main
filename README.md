#node-todo-cicd

sudo apt install nodejs ,

sudo apt install npm ,

npm install ,

node app.js 


# Created a Docker-integrated Jenkins declarative pipeline.

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



# Created Jenkins agent and deployed Django web application through Jenkins Master server to Jenkins agent.

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


