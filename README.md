# Github Workshop
Welcome to your first workshop of CS50! Here, you'll learn how to use Github, a version control system that allows for teams to concurrently work on the same code efficiently. Knowing how to use Github will be important both for this class and for a lot of future software development you'll do in the future. Let's get started!

## Getting Started
### What is Github?
GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects without always having to be in the same place.

This tutorial will teach you GitHub essentials like repositories, branches, commits, and pull requests. You’ll create your own Hello World repository and learn GitHub’s Pull Request workflow, a popular way to create and review code. The tutorial relies on using the command line interface, but all of these tasks can also be done without using the command line.

### Setup Instructions
To follow along this tutorial, you need to have **(1) a Github account** and **(2) Install Git on your computer/machine**. If you choose not to install Git on your machine, refer to the slides on how to use Git without the command line!

#### 1. Getting a Github Account
Navigating to www.github.com will lead you to the Github home page where you can sign up for an account. When signing up, choose the **free** personal plan option, which will let you create unlimited public repositories. Later in this guide, we walk you through how to activate your snazzy **student package**.

#### 2. Installing Git
For this step, it is easiest if you just refer to Github's default setup article: https://help.github.com/articles/set-up-git/

Follow the instructions for:
- Downloading/Installing the lastest version of Git,
- Setting your username globally in Git, and
- Setting your email globally in Git

After doing this step, you should be able to type "git" into your command line and get meaningful output. You're all set!

## The Tutorial
### 1. Repositories
A repository is usually used to organize a single project. Repositories can contain folders and files, images, videos, spreadsheets, and data sets – anything your project needs. Typically, these repositories, or repos, will be used to house all the code + necessary materials for your project.
#### Cloning This Repository
This workshop will revolve around you (and everyone else) playing with this repository. To get started, you'll need to **clone** this repository on your machine. Think about cloning a repository as downloading a copy of that repo onto your local machine that you can push to, pull from, and edit. To clone a repo:
1. Create an empty folder somewhere on your machine
2. Navigate to that folder using your command line/Terminal
3. Once inside that folder, type: *git clone https://github.com/CS50Stanford/GithubWorkshop.git*
4. That creates a folder titled "GithubWorkshop". Lastly, navigate into that folder: *cd GithubWorkshop* 

#### (Optional) Creating your own new repository
Cloning repos are nice, but say you want to start your own new project. Here's how you'd make your own repo:
1. In the upper right corner, next to your avatar or identicon, click the **+** and then select **New Repository**.
2. Name your repository.
3. Write a short description.
4. Select Initialize this repository with a README.
5. Click **Create Repository**

### 2. Branches
Branching is the way to work on different versions of a repository at one time. By default, every repository has one branch named *master* which is considered to be the definitive branch. We use other branches to experiment and make edits before *committing* them to master. In other words, think of the *master* branch as the branch that's meant to always be stable at any given time. Every other branch is used to experiment with creating new features, fixing bugs, etc... Once those features are fully implemented, you *merge* them into master to make them a part of the final product.

**Note:** You'll see that some teams don't use branches and instead just commit everything to master. This is typically considered bad practice since it means you have a higher risk of messing up the master branch, which is BAD and hence not recommended. If you choose to do this approach, be very careful!

#### Creating a Branch
Lets create your first branch off of master: 
```
git checkout -b YOUR_BRANCH_NAME
```

After doing that, you should get a message saying "Switched to a new branch 'YOUR_BRANCH_NAME'"! This means you've created your first branch! You can verify this by typing:

```
git branch
```

Which will list all branches related to your local machine, with an asterisk next to the branch you are currently on.

You can play around with jumping between branches by doing: 
```
git checkout master
```
which will switch you back to master, or *git checkout YOUR_BRANCH_NAME*, which will switch you back to your branch. Make sure to not include the -b! That will end up creating a new local branch!

#### What just happened?
When you create a branch in your project, you're creating an environment where you can try out new ideas. Changes you make on a branch don't affect the master branch, so you're free to experiment and commit changes here, safe in the knowledge that your branch won't be merged until it's ready to be reviewed by someone you're collaborating with.

As a note, this branch you just created won't actually persist in your actual Github directory until you make your first **push**.

#### Creating a new file
As a test, let's create a new file. 

1. Type: *vim yourfullname.txt* to create a text file.
2. In the file, type your name, year, major, CS50 Team, and two fun facts about yourself. Make them cool!
3. After you're done, save and exit by typing: *:wq*

*Note: The above 3 steps could've been done by also just creating a text file in whatever usual manner you create text files in. You don't have to use vim :)*

#### Committing your changes
Great! You've created a file, but this file only exists locally. How do we push it to your branch?

```git status```
