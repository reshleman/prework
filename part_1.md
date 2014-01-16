# Part 1

## Your Editor

One of the first things you should decide on for development is a text editor.
Your editor provides you with lots of benefits that will dramatically speed up
your ability to write code. It’s important to chose an editor that offers a good
feature set. Unless you already have an editor with which you are proficient, we
suggest using [Sublime Text][sublime_text]. You may not use Text Editor on
Ubuntu or TextEdit.app on OSX. Spending a lot of time in your editor is a good
way to become proficient. Feel free to read the [documentation on Sublime
Text][sublime_text_documentation] to increase your understanding of the editor.

## Your Terminal

The terminal provides you with quick access to things normally provided by your
file manager, like Finder.app, and will allow us to manage both directories
(folders) and files.

On OSX, you can find your terminal at `Applications > Utilities > Terminal`.

On Ubuntu, you can find your terminal at `Applications > Accessories > Terminal`.

It might be worth pinning it to your dock, as you will be using it frequently
over the course of this class.

When you run a terminal program, you’ll typically be provided with a prompt
followed by a cursor where you can type different commands. Here are some of the
commands you should familiarize yourself with:

`pwd`: “print working directory” displays the name of the current directory
terminal is running under. Try it out by opening a terminal and typing:

    pwd

`mkdir`: “make directory” creates a new directory under the current directory. Try
it out by creating a directory named “test”:

    mkdir test

`ls`: “list” displays the names of all the files and directories under the current
directory. Try it out by typing:

    ls

You should see our `test` directory as well as any other files and directories
that were in your current directory.

`cd`: “change directory” allows you to change the current directory. Try it out by
typing:

    cd test

followed by:

    pwd

You should now be inside the test directory. Now let’s go back up a directory by
typing:

    cd ..

The `..` is used to specify the directory above the current directory. `..` is
also known as a relative path. A relative path is any path that you reference
without putting a `/` at the beginning of the directory name. When you add the
`/` at the beginning of a directory name you’re telling your terminal to use an
absolute path. An absolute path starts from the “root” directory. The “root”
directory is the top most directory that will contain every other file and
directory inside of it or one of it’s directories. You’ll typically find that
you’ll use relative paths far more often than absolute paths.

`mv`: “move” will change the name of a file or directory. Try it out by typing:

    mv test testing

followed by:

    ls

You should see that the `test` directory has been renamed to `testing`

`rm`: “remove” will delete a file or directory. Try it out by typing:

    rm testing

Whoops, you should see `rm: testing: is a directory`. In order to delete
directories we need to tell `rm` to delete recursively. In other words, for
directories it needs to make sure to delete everything inside the directory.
While our directory is currently empty we’ll still need to delete recursively.
We can do this by using the `-r` flag. Flags are usually prefixed with a `-` and
they change the way a program will run. In this case the `-r` flag allows `rm`
to remove a directory.

    rm -r testing

Then if you type:

    ls

You’ll see that the testing directory has been removed.

## Git

Git is a source content management (or SCM) tool that allows you to do revision
control. In short, it allows you to keep track of changes you make to your files
and easily share them among other developers. Revision control is essential to
managing and collaborating on code and git is one of the most popular tools for
handling it.

We’ll be using Git for both the pre-work and class itself. We’ll be storing our
code using the online service [GitHub][github]. GitHub is a free platform for creating
git repositories and sharing them with other developers.

To get started, you will need to install the Git program which you can download
from http://git-scm.com/downloads if you are using OSX. If you are using Ubuntu,
Git can be installed by running

    sudo apt-get install git-core

After you have Git installed you should run the following commands to set up
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

![GitHub Create Repository][github_create_repository]

You’ll need to open “Terminal.app” on OSX or “Command Prompt” on Windows to
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

## Moving on

If you feel comfortable with everything you learned in Part 1, please move on to
[Part 2][part_2].

[sublime_text]: http://www.sublimetext.com/
[sublime_text_documentation]: https://tutsplus.com/course/improve-workflow-in-sublime-text-2/
[github]: https://github.com/
[github_signup]: images/github_signup.png
[github_free_plan]: images/github_free_plan.png
[github_new_repository]: images/github_new_repository.png
[github_new_repository_name]: images/github_new_repository_name.png
[github_public_repo]: images/github_public_repo.png
[github_create_repository]: images/github_create_repository.png
[part_2]: part_2.md
