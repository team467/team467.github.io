## Installation of Packages

Before your set up your writing **or** developing enivronment you need to install some packages to make your production as smooth as possible.

The two packages you need to install are [`git`](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [`hugo`](https://gohugo.io/installation/). **Note** that, Git is *not* the same thing as GitHub. Git is a version control system that lets you *manage* and keep track of your source code history. GitHub is a cloud-based hosting service that lets you manage Git repositories. On the topic of GitHub, make sure you have a [GitHub account](https://github.com/join) that you can use to contribute to the website.

Now that you have installed all of these packages, here are some tests that you should run to make sure it installed correctly. For `git` simply run:
```
git --version
```
If Git is installed, it will display the installed version (e.g., `git version 2.41.0`). If not, you'll see an error message.

For `hugo` simple run:
```
hugo version
```
If Hugo is installed, it will display the installed version (e.g., `hugo v0.139.2+extended linux/amd64 BuildDate=unknown`). If not, you'll see an error message.

Now that you have all your packges ready, you can begin with cloning the repository and checking if it works.

## Setup of Local Environment

The first thing you need to do is to clone the team repository. You can do this through the GitHub website. Navigate to the [repository](https://github.com/team467/team467.github.io) and in the top right you will see the option to fork the repository. Forks let you make changes to a project without affecting the original repository, also known as the "upstream" repository.

In a command prompt, type the following commands:
```
git clone https://github.com/username/team467.github.io.git --recursive
```
**Replace "username" with your own username!** 

This will create a new subfolder named `team467.github.io`. Make this your current directory:
```
cd team467.github.io
```

The website content can be found in the `content` sub-directory, the file layout loosely matches the website.

You can either edit an existing page (the files ending in `.md`), or create a new one.

For example to create a new blog post, run the following from a command prompt

```
hugo new content/posts/2024-09-16-NewBlog.md
```

If you want more specifics about how to **write posts and more read the [guidelines](GUIDELINES.md)**.

Once you have saved your changes, **after reading throughougly through the [guidelines](GUIDELINES.md)**, you can test them locally on your computer by running this command:
```
hugo server
```

And connecting in your web browser to http://localhost:1313/.

## Commiting Work
### Add Content
Once content looks good, push to github using the following sequence of commands from the root directory
```
git add content
```
This adds all your changes to the staging area on git
### Setup Email
```
git config user.name username
git config user.email email
```
This sets the account and email the commits will be connected to. For example:
```
git config user.name pgund
git config user.email 183660136+pgund@users.noreply.github.com
```
Of course change the email and username to what your GitHub account is associated to, unless you want to give me credit!
### Commit Work
```
git commit -m "A meaningful message used to describe the change"
```
This checks in the change to the local copy of git along with a message describing why these changes were made
### Push Work
```
git push
```

This pushes the changes to your clone of the GitHub repository, **not the live repository**.

1. Now, go back to your cloned version of the repository. 
2. You should see a message like "Your recently pushed branches" with an option to "Compare & pull request". Click it. 
3. Add a descriptive title for your pull request (e.g., "Fix bug with homepage styling").
4. In the comment section, provide a more detailed explanation of the changes you’ve made and why.
5. Choose the base branch (usually main) and compare it with your branch.
6. Click Create pull request.

At this point, a mentor will review the changes and will either accept or will send back to you for updates. If accepted, then the website will be automatically regenerated and your changes will be live.