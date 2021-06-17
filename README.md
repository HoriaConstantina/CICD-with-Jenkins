### CI/CD with Jenkins


![cicdJenkins](https://user-images.githubusercontent.com/56413816/122414606-2d230c80-cf7f-11eb-9899-496388794378.png)







You have your application available on your local host You SSH into your GitHub repository GitHub has a Webhook which listens for changes to the repository. Jenkin automates the CI/CD process. Anytime changes are made/ code is devloped these get pushed to GitHub and passed through Jenkins. Steps 1-5 are part of the CI-Continuous Integration process i.e source code is built and pushed. Then we have the Agent Node which will run all the automated tests on this code. Because there may be many testers testing code we do this on the agent node. Then we push this to Master Node, where we will use scp to transfer the data from the local host to the remote host in AWS. i.e we want to push it to the cloud. Steps 6-8 are part of CD-Continuous delivery- we are putting things in the pre-production environment after it has been tested. The we will push from the pre-production environment to the live environment on the cloud in aws. Is reffered to as CD- continuous deployment.



## How to set up Jenkins
- Generate new ssh key in you localhost/laptop and name it yournamejenkins
- copy public ssh key in into github the .pub file yournamejenkins.pub
- copy provate ssh key int o Jenkins - yournamejenkins.pub
- add git-hub url into repository URL after select Git underneath source code managment
- add https git-hub repo url in the git project
- exchange the branch to main
- execute shell
- cd app
- npm install
- npm test
- save and trigger the build
