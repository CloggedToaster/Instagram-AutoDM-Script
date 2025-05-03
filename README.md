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
    $ git config --list | grep user.*
    ```

4. Clone the repository (which downloads a local copy of the project to your computer):
    ```
    git clone https://github.com/CloggedToaster/Instagram-AutoDM-Script.git
    cd Instagram-AutoDM-Script
    ```


5. You will need to download all dependencies:

## Regular Development Workflow

1. Switch to the main branch and pull the latest changes:
    ```
    git switch main
    git pull
    ```

2. Create a new feature branch:
    ```
    git checkout -b "<Insert_name_of_feature_branch_here>"
    ```

3. Make changes and stage them for commit:
    #### To stage **specific** files
    ```
    git add <file_to_track>
    ```

    #### To stage **all** changes
    ```
    git add --all
    ```

4. Commit your changes with a descriptive message:
    ```
    git commit -m "Message describing the changes you made in the commit"
    ```

5. Push your feature branch to the remote repository:
    #### **Note: If it's your first time pushing, follow the recommended command if prompted**
    ```
    git push
    ```

## Do When You Are Ready To Merge Changes

1. Create a Pull Request (PR) on GitHub and assign a team member for review.

2. After approval, ensure your feature branch is up to date with main using rebase:
    ```
    git switch main
    git pull
    git switch "<Insert_name_of_feature_branch_here>"
    git rebase main
    ```

3. Resolve any conflicts, if needed, during rebase.

4. Once in sync, merge the PR into the main branch in Github (should be a big green merge button)

5. Once you merge you should update your local main branch
    ```
    git switch main
    git pull
    ```

## Misc. Tips

1. If you aren't sure of the current status of your local branch, you can type `git status` in a terminal and it will output the current status of the branch.

2. If you aren't sure which branch you are on, you can type `git branch` and it will output a list of branches and highlight green which you are on. (In order for this to stop outputting branches press `q`)

3. To switch between branches you can type `git switch <branch name>`