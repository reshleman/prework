# Git

Git is a source content management (or SCM) tool that allows you to do revision
control. In short, it allows you to keep track of changes you make to your files
and easily share them with other developers. Revision control is essential to
managing and collaborating on code and Git is one of the most popular tools for
handling it.

We’ll be using Git for both the prework and class itself. We’ll be storing our
code using the online service [GitHub][github]. GitHub is a free platform for creating
Git repositories and sharing them with other developers.

To get started, you will need to install Git which you can download
from http://git-scm.com/downloads if you are using OSX. If you are using Ubuntu,
Git can be installed by running

    sudo apt-get install git-core

After you have installed Git, you should run the following commands to set up
your Git user:

    git config --global user.email “Your email address”
    git config --global user.name “Your Name”

This step is necessary because Git will need to record who made changes to the
files.

## GitHub

After installing Git you will need to create a GitHub account. If you don’t
already have an account, visit https://github.com/ and sign up.

![GitHub Sign Up][github_signup]

Make sure you select the free plan and leave “Help me setup an organization
next” unchecked.

![GitHub Free Plan][github_free_plan]

Once you’ve finished signing up, click the “New repository button”

![GitHub New Repository][github_new_repository]

Fill in the repository name with Metis Prework.

![GitHub New Repository Name][github_new_repository_name]

Make sure it’s public.

![GitHub Public Repo][github_public_repo]

Make sure “Initialize this respository with a README” is unchecked and click
“Create repository”

You’ll need to open “Terminal.app” on OSX or “Terminal” on Ubuntu to
perform the following steps. It is suggested you perform these steps in a
specific directory. In your terminal, run:

    cd ~
    mkdir metis_prework
    cd metis_prework

and then follow the instruction listed under:

![GitHub Create Repository Instructions][github_create_repository_instructions]

When using git you will typically type `git` followed by the command you want to
run. Let’s briefly review the commands GitHub had us run:

`init`: Sets up the current directory to be useable by Git. You will always need
to perform this first when you create your own git repository. If you are
“cloning” someone elses repository you will not need to run “init”.

`add`: “Stages” files. Running this command tells Git which files you want to
commit. Only committed models will be pushed to GitHub when we call push later.

`commit -m "first commit"`: Commits the files we’ve staged. We use the “-m” which
is called a flag followed by “first commit” to provide a message with the
commit. Messages are a good way of telling why you’ve made a change.

`remote add origin URL`: Sets up our repository to be able to push to GitHub.
We’ve called the remote repository “origin” which is located at the URL, but we
could have named this anything. You will only need to do this once.

`push -u origin master`: Sends our code to GitHub. Origin is the name of the
remote and master is the branch we want to push to. You can think of the master
branch as the “main” branch. While you can have additional branches let’s just
focus on master for now. Also you can ignore the “-u” flag for now.

[github]: https://github.com/
[github_signup]: images/github_signup.png
[github_free_plan]: images/github_free_plan.png
[github_new_repository]: images/github_new_repository.png
[github_new_repository_name]: images/github_new_repository_name.png
[github_public_repo]: images/github_public_repo.png
[github_create_repository_instructions]: images/github_create_repository_instructions.jpg
