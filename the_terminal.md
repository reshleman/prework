# The Terminal

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

you’ll see that the testing directory has been removed.
