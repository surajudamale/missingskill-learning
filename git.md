# **GIT**

#### Introduction to GIT

- Git is a free and open source distributed version control system designed to handle small as well as large projects with speed and efficiency.
- Git was created by Linus Torvalds in 2005.
- Git is easy to learn and very fast to perform.
- It also has excellent support for branching, merging and rewriting repositories.
- Git is free and very fast.
- Git basically developed for Linux Project Requirement.
- Git is Distributed source control System.

---

#### Why GIT ?

- In Gits collections of version control files lept together in a repository, The repository also contains files, History, config managed by GIT
- There are three states of Gits
  - Wotking Directory
  - Staging area – pre-commit holding area
  - Commit – Git Repository (History)
- Remote Repository (Github)
- Master Branch

---

#### Version Control System

##### Version Control system fall into two catagories.

- **1. Centralized**

  - In Centralized system all team members are connect with Central System to share a same code with each other.
  - Subversion and Team Foundation Server are the example of Centralized Version control system.
  - The problem with the Centralized version control System is the single point of failure, If the Server goes offlin ewe cannot colaburate until serrver comes back online

- **2. Distributed**
  - In distributed system you dont have problems like centralized have. In this Every team member has a copy of the project with its histiory in his own machine. So we can save snapshos of our project locally on our machine.
  - If the server is offline we can synchronize our work directly with other, GIT and Mercurial are the example for Distributed version control System.
  - Git is the most popular version control System, because its Free, Open Source, Super Fast, Scalable, Cheap Branching/Merging.
  - Git is everywhere almost 90% people are using Git for better Software development.

---

#### Steps of using GIT

- Git is a distributed version control system.
- Open an account ongitlab.
- I used linux system. So i dont want to donload git bash which is basically used to operate git on windows.

**Git Commands**

- At the command line, first verify that you have GIT installed.
- On all operating System
  ```
  git --version
  ```
- The command that sets the auther name and the email address with yor commits.

  ```
  git config --global user.name "suraj udamale"
  git config --global user.email "surajudamale08@gmail.com"
  ```

- To create an empty Repository type this command.

  ```
  git init
  ```

  - This will create a hidden folder, **_.git_** which is basically needed for Git to work.

- The command that has been used to obtain a repository from Git Repository.
  ```
  git clone <HTTPS URL>
  ```
- Next step is , check what files or folders you want to add to yor Git repository.
  ```
  git status
  ```
- Review the resulting the list of files, you can tell git which of the files you want to add into your Gin repository.
  ```
  git add <file/directory name> ...
  ```
  for adding all files use this command.
  ```
  git add .
  ```
- This will 'stage' all your files to be added to Git, preparing them to be commited in your first commit.
- The commit will record the file permanently in the version history.

  ```
  git commit -m "First commit"
  ```

  this will commit all the files that have been added, along with the commit message.

- Then we can see the list of version history fro the current branch, what is gets coomited on which brach
- In these there is auther name and email with date and time gets specified with the clatest or recorded commits

  ```
  git log
  ```

- Final Step is now push these file into the Git Repository.
- These commands sends the commited changes to the master to the remote repository.

  ```
  git push origin master
  ```

  It will ask about username and password for complete the process.

- The command that has been used to fetch and merge the changes on the remote repository to local directory.
  ```
  git pull <Repo URL>
  ```

#### ssh-Keygen

- To make our usability smooth we uses a kwy for **_push/pull_** code it doesn't ask for username and password again and again. We create a key in Local Repository.
  ```
  ssh-keygen
  cd .ssh
  cat id_rsa.pub
  ```
  Copy that bulky code into the Git ssh key....

#### Create Branches on GitHub

- Creating and checking out new branches
  - To create new branch while staying on the current branch use :
    ```
    gir branch <branch name>
    ```
  - Generally, the branch name must not contain spaces and must be relevent to the project.
  - To switch to an Existing branch.
    ```
    git checkout <branch name>
    ```
    Revert back to the tree
  - To create new branch and switch it to :
    ```
    git checkout -b <branch name>
    ```
  - To merge the branches use :
    ```
    git merge <2nd branch>
    ```
  - To delete the specific branch use :
    ```
    git branch -d <branch name>
    ```

#### Listing Branches

| Goal                               | Command                          |
| ---------------------------------- | -------------------------------- |
| List local branch                  | git branch                       |
| List of remote branches            | git branch -r                    |
| List of merged branches            | git branch --merged              |
| List of unmerged branches          | git branch --no-marged           |
| List of branches containing commit | git branch --contains [<commit>] |

#### How to pull the branches when there is changes in Remote Repository

- First we checkout to one branch we want to merge.
  ```
  git checkout<1st branch name>
  ```
- Then merge the other branch
  ```
  git merge <2nd branch name>
  ```
- Then push the main branch into the Remote Repository
  ```
  git push origin <1st Branch name>
  ```
- Then all the merge branches are merged to the master branch were all project will be done.
