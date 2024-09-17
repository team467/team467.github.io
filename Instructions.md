In a command prompt, type the following commands:
```
git clone git@github.com:team467/team467.github.io.git --recursive
```

This will create a new subfolder named team467.github.io

Run the following command at a command prompt to create a new branch for your changes:
```
git checkout <your_branch_name>
```
... where <your_branch_name> is something that you define that is unique to you.  It can be your name <john_branch> or the feature you are working on <spirit_of_shrewsbury>.  The name doesn't matter, it is only temporary for you to make your edits. 

The website content can be found in the 'content' sub-directory, the file layout loosely matches the website. 

You can either edit an existing page (the files ending in .md), or create a new one.  

For example to create a new blog post, run the following from a command prompt
```
hugo new content/posts/2024-09-16-NewBlog.md
```
... where `2024-09-16-NewBlog.md` should be given an appropriate date and name based on the content in your blog. 

Then edit the file you just created in a text editor. It should look like this
```
---
title: 'NewBlog'
date: 2024-09-16T19:27:19-04:00
---
```

You can edit the title to reflect the content of your post.  Add your content at the end of the file using the Markdown syntax.  You can find more information on Markdown [here](https://www.markdownguide.org/basic-syntax/) and a tutorial to learn the basic concepts [here](https://www.markdowntutorial.com)

As an example, here is the content from the introductory welcome post I made:
```
---
title: 'Welcome to the new Shrewsbury Robotics Website'
date: 2024-09-16T11:59:48-04:00
---

This is a new website based on the static website generator [hugo](https://gohugo.io/) that allows for easy creation of website content using [Markdown](https://www.markdownguide.org/basic-syntax/).

The website is auto-generated and hosted on [Github Pages](https://pages.github.com). 
```

Once you have saved your changes, you can test them locally on your computer by running this command:
```
hugo server
```

and connecting in your web browser to http://localhost:1313/

---
Once content looks good, push to github using the following sequence of commands from the root directory
```
git add content
```
This adds all your changes to the staging area on git

```
git commit -m "A meaningful message used to describe the change"
```
This checks in the change to the local copy of git along with a message describing why these changes were made

```
git push
```
This pushes the changes live to the main github.com repository

At this point, a mentor will review the changes and will either accept or will send back to you for updates.  If accepted, then the website will be automatically regenerated and your changes will be live. 