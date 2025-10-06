# Connect a GitHub Repo with AWS

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-devops-github)

**Author:** Łukasz Brodziak  
**Email:** lukasz.brodziak@gmail.com

---

## Connect a GitHub Repo with AWS

![Image](http://learn.nextwork.org/surprised_maroon_fierce_chinese_gooseberry/uploads/aws-devops-github_dd9d254e)

---

## Introducing Today's Project!

In this project, I will demonstrate how to create a GitHub repo and push code changes to it. This repository will be then used in next steps of CI/CD pipeline.

### Key tools and concepts

Services I used were git and GitHub. Key concepts I learnt include creating new repository on GitHub, initializing local git repo on EC2, pushing code to remote.

### Project reflection

This project took me approximately 30 minutes 

I did this project because I needed the code on github repository to use it in CI/CD pipeline that will be created in later steps.

This project is part two of a series of DevOps projects where I'm building a CI/CD pipeline! 

---

## Git and GitHub

Git is often called a version control system since it tracks changes by taking snapshots of what files look like at specific moments, and each snapshot is considered a 'version'. I installed Git using the command sudo dnf install git -y


GitHub is a place for engineers to store and share their code and projects online. It's called GitHub because it uses Git to manage your projects' version history. I'm using GitHub in this project to store app files to be used in next projects.

![Image](http://learn.nextwork.org/surprised_maroon_fierce_chinese_gooseberry/uploads/aws-devops-github_efaadbf7)

---

## My local repository

A Git repository is a folder that contain all project files and their entire version history.

Git init is a command that sets up the directory as a local Git repository which means changes are now tracked for version control. After running git init, the response from the terminal was "Initialized empty Git repository in /home/ec2-user/nextwork-web-project/.git/"

A branch in Git is an "alternate" version of the code in the same repository. This allows developers to add changes and new features without affecting the main branch and thus possibly breaking the working production code.

![Image](http://learn.nextwork.org/surprised_maroon_fierce_chinese_gooseberry/uploads/aws-devops-github_7bf21bae)

---

## To push local changes to GitHub, I ran three commands

### git add

The first command I ran was "git add". This command is used to add new and changed files to staging area. In the command I ran I use . (dot) as an argument which added all files to staging are. Another usage is by passing particular filename to be added. A staging area is a place where all changed files are stashed by git for review before pushing them to remote.

### git commit

The second command I ran was git commit -m "Message". Using '-m' means te we are adding a comment about what was changed in this commit.

### git push

The third command I ran was git push -u origin master Using '-u' means that we are setting an upstream for local branch, which makes Git push to this branch by default.

---

## Authentication

Git needs to double check that you have the right to push any changes to the remote origin your local repo is connected with. To do this, Git is now authenticating your identity by asking for your GitHub credentials.

### Local Git identity

Git needs author information for commits to track who made what change. If you don't set it manually, Git uses the system's default username, which might not accurately represent your identity in your project's version history.

Running git log showed me that jsp file has been updated with new content

![Image](http://learn.nextwork.org/surprised_maroon_fierce_chinese_gooseberry/uploads/aws-devops-github_9a27ee3b)

---

## GitHub tokens

GitHub authentication failed when I entered my password because GitHub phased out password authentication to connect with repositories over HTTPS - there are too many security risks and passwords can get intercepted over the internet 

A GitHub token is a unique string of characters that looks like a random password.  I'm using one in this project because it is a better practice than using password.

I could set up a GitHub token by going into Profile -> Settings->Developer settings -> Personal Access Tokens -> Tokens (classic). 

![Image](http://learn.nextwork.org/surprised_maroon_fierce_chinese_gooseberry/uploads/aws-devops-github_fa11169d)

---

## Making changes again

I wanted to see Git working in action, so I updated the index.jsp file. I couldn't see the changes in my GitHub repo initially because changes were only done locally.

I finally saw the changes in my GitHub repo after I commited them and pushed them form local repo to remote.

![Image](http://learn.nextwork.org/surprised_maroon_fierce_chinese_gooseberry/uploads/aws-devops-github_6becb2bc)

---

## Setting up a READMe file

As a finishing touch to my GitHub repository, I added a README file, which is a file containing projects documentation. I added a README file by runing touch command to create it in local repo and then pushed the file to github.

My README is written in Markdown because this is the language used for formatting md files. Special characters can help you format text in Markdown, such as ** for making text bold, or # which creates a large header (H1 in HTML).

My README file has 6 sections that outline general information about the code, technologies used in the project, instructions on how to install and setup the project, contact information

![Image](http://learn.nextwork.org/surprised_maroon_fierce_chinese_gooseberry/uploads/aws-devops-github_c94976902)

---

---
