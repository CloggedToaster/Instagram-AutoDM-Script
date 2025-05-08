# Instagram-AutoDM-Script Workflow


## Initial Setup
### Pre-Visual Studio Code
1. Download and use [VSCode](https://code.visualstudio.com/download) for development.

2. You will need to [download git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) (and if you are using windows make sure you include the git credentials manager).

### Inside Visual Studio Code
1. Open a folder (CTRL+K CTRL+O) of the location where you would like your project to be saved.

2. Open the Terminal by following the menu choices: Terminal > New Terminal (CTRL + SHIFT + `)

3. Before you start using Git, you will need to configure your user name and email:
    ```
    git config --global user.name "Your Name"
    git config --global user.email "your.email@example.com"
    ```
    In order to verify if you entered these correctly you can run:

    ```
    git config --list | grep user.*
    ```

4. Clone the repository (which downloads a local copy of the project to your computer):
    ```
    git clone https://github.com/CloggedToaster/Instagram-AutoDM-Script.git
    cd Instagram-AutoDM-Script
    ```


5. You will need to download all dependencies

## Development Quick Start:
###
1. #### Checkout and create a branch.

    Terminal Input:
    ```
    git checkout -b <Branch_Name>
    git push origin <Branch_Name>
    ```
    This will create a new branch locally then push it to the remote repository.
2. #### Code!

    Make all relevant code changes, test and make sure everything works!

3. #### Add all files to your current branch.

    Terminal Input:
    ```
    git add --all
    ```
    This will stage all files in the present working directory for commitment to the remote repository
4. #### Commit all changes.

    Terminal Input:
    ```
    git commit -m "<Commit Message>"
    ```
    This will stage the commit for pushing to the remote repository.
5. #### Push all commits.
   **Note: If it's your first time pushing, follow the recommended command if prompted.**

   Terminal Input:
   ``` 
   git push origin <Branch_Name>
   ```
   This will push the local committed changes to the remote repository.

6. #### Create a Pull Request (PR) in Github.
    <p align="center">
        <img src="images/README%20images/PullRequestCreate1.gif" alt="Pull Request Create Step 1">
        <em>Starting a Pull Request and Selecting the Branch</em>
    </p>
    </br>

    <p align="center">
        <img src="images/README%20images/PullRequestCreate2.gif" alt="Pull Request Create Step 2">
        <em>Viewing Code Changes, Adding a Description, and Assigning Reviewers </em>
    </p>

7. #### Rebase main upon Pull Request Approval 
   **Note: This will only be necessary when multiple people are working on multiple features and things are update while you're working on your branch**
   
    Terminal Input:
    ```
    git switch main
    git pull
    git switch <Insert_name_of_feature_branch_here>
    git rebase main
    ```
    This will switch to your local 'main' branch and pull all changes. This will then switch to the branch you've been working on and graft it's changes on top of the newly updated main branch. (Manual input may and often will be required!)
   
8. #### Merge with main in Github.
    Once you've rebased and your branches are in-sync, merge the Pull Request (PR) into the 'main' branch in Github (There should be a big green merge button.)
    
    <p align="center">
        <img src="images/README%20images/PullRequestCreate3.gif" alt="Pull Request Create Step 3">
        <em>Merging a Pull Request</em>
    </p>
    
    

3.  #### Update local main branch
    
    Terminal Input:
    ```
    git switch main
    git pull
    ```
    This will switch your current branch to the local 'main' branch and then this will pull from the 'main' branch on the remote repository.

## Misc. Tips

1. If you aren't sure of the current status of your local branch, you can type `git status` in a terminal and it will output the current status of the branch.

2. If you aren't sure which branch you are on, you can type `git branch` and it will output a list of branches and highlight green which you are on. (In order for this to stop outputting branches press `q`)

3. To switch between branches you can type `git switch <branch name>`