# GitHub-Actions-Zero-to-Hero
Repository to kick start your journey with GitHub Actions

1) No need of any plugins
2) We have to create a folder in the repository like .github/workflows 
3) in the workflows we can write our github-actions file which is in yml like first-actions.yml (pipeline)
4) in the ymal file, ``` on ``` is used to actions like push, commit .. whenever there is a action in the repo
5) can we use any no. of actions on ``` on ``` like push,commit, issues, pill it will work like either of the actions should be done in the repo side.
6) Bydefault you have to execute the piepline
7) No limitation we can keep any no. of actions files.
8) As soon as we commit, it will checkout the code and it has to create a python evn for us (python-example is used here) be'coz we don't not configure any server
9) In jenkins we have servers pre-configured like docker containers or worker nodes
10) If we can using 3 jobs then it is like we are using 3 jenkins pieplines
11) Under steps : users : it is not configured it is plugin (checkout@v3)
12) Ref link ``` https://docs.github.com/en/actions/quickstart ```

# Github Runners
--
1) **SELF HOSTED RUNNERS** : Runner is a place where our job gets run. (In jenkins we called it as Agent node - where our app'n gets run on jenkins)
2) **GITHUB HOSTED RUNNERS** : When we run or build a CI project on github, github have the runner. we dont have any ownership to the runner.
3) When it comes to enterpirse or private project, Runner provided by github is not expected to run for our application wch needs more cpu or ram like that, then we will go with self hosted runners (Security, private repo's, runner not matching with the requirements) -- SELF HOSTED RUNNERS
4) Use only Http and HTTPS ports -- in inbound and out bound rules --- EC2 instances.

# SETUP Self hosted Runners
NOTE: In the workflow folder we have created a first-actions.yml file where we have option to switch between github hosted runner and self hosted runners
![image](https://github.com/pavankumar0077/GitHub-Actions-Zero-to-Hero/assets/40380941/502f9e7a-04e0-4825-a573-e9233b275173)
Here runs-on == if we mention ubuntu then it will take ubuntu and run on it. If we select runs-on == self-hosted then it will selected the runner that we have created

1) Go to github repo settings
2) Actions --> Runners
3) Click on Add new runner
4) ![image](https://github.com/pavankumar0077/GitHub-Actions-Zero-to-Hero/assets/40380941/afe1be4a-3c50-4382-ac14-3a0f506c75d5)
5) We have download option where we have instruction or commands to run, Follow as menioned.
6) ![image](https://github.com/pavankumar0077/GitHub-Actions-Zero-to-Hero/assets/40380941/79d4b791-a202-4459-9c66-638c7d820c7e)
7) In the github we will see the green mark that means runner done with the job.



# -------

## Comparing with Jenkins 
1) If it is public project then GITHUB ACTIONS are high preffered (Open source)
2) Because we will entire servers for free microsoft provides free servers
3) If the project is private project it is recommmended to use JENKINS it has a lot of options or features like docker, plugins and etc

### Advantages of GitHub Actions over Jenkins

- Hosting: Jenkins is self-hosted, meaning it requires its own server to run, while GitHub Actions is hosted by GitHub and runs directly in your GitHub repository.

- User interface: Jenkins has a complex and sophisticated user interface, while GitHub Actions has a more streamlined and user-friendly interface that is better suited for simple to moderate automation tasks.

- Cost: Jenkins can be expensive to run and maintain, especially for organizations with large and complex automation needs. GitHub Actions, on the other hand, is free for open-source projects and has a tiered pricing model for private repositories, making it more accessible to smaller organizations and individual developers.

### Advantages of Jenkins over GitHub Actions

- Integration: Jenkins can integrate with a wide range of tools and services, but GitHub Actions is tightly integrated with the GitHub platform, making it easier to automate tasks related to your GitHub workflow.

In conclusion, Jenkins is better suited for complex and large-scale automation tasks, while GitHub Actions is a more cost-effective and user-friendly solution for simple to moderate automation needs.

# Interview Questions
1) Why Github actions, we have tools like jenkins or aws cloud build ? Why you have chosen Github Actions ?
A) 1.1) We are using public project so that code is in github, it makes easy for CI-CD process
   1.2) Our project is already in github and we manage everything in github for ex not jsut the cicd we also do our agile - scurm in projects option present in github, we use confluence pages as gihutb wiki, we also use the security and we use insights as well.

2) How do you secure the sensitive information in GITHUB ?
A) In Repo settings we use the SECRETS AND VARIABLES OPTION

3) How do you write a Github CI File.
A) in the repo, we create .github/workflow folder --> in that we write our ci files with the extension .yml


