# Personal wiki

## Tools

### **Code editor**

[![VSCode][vscode]][vscode-url]  
Visual studio code is my choice of code editor.  
It is a good code editor with a lot of extensions that help the process of coding and I am also used to i since it is what I have always used to code.

**Extensions:**

- Vue VSCode Snippets

- Vue Language Features (Volar)

- Prettier - Code formatter

- Tailwind CSS IntelliSense

### **Browser**

[![Edge][edge]][edge-url]  
Microsoft Edge is my browser of choice.  
It comes already downloaded with any Windows device which is the OS I am using.

### **Javascript runtime**

[![Node][node.js]][node-url]  
Node.js

**Installation process**

Automatically install necessary tools

### **Source control management**

[![Git][git]][git-url]  
Git is the source control management I use.  
I use Git to track the modifications I make to the code by publishing it to a repository on Github. Git makes it so that I can easily work with others and share code to a shared directory. When installing Git it adds useful dependencies such as npm, node.js and chocolately.

**Installation process**

When installing mark the "check for daily updates" box

Choose Visual Studio Code as Git's default editor

Override the default branch name for new repositories to "main"

Use Windows' default console window as terminal emulator

### **SSH as authentication on Github**

**Generate a SSH key**  
Open Git Bash

You generate a keypair using this line: `$ ssh-keygen -t ed25519 -C your_email@example.com`

Enter a filename or press "Enter" to accept default file location.  
At the prompt about you can either leave it empty for no passphrase or write a secure one for yourself. A passphrase is used as an extra layer of security if someone gains access to every system that uses that SSH key.

**Adding SSH key to the ssh-agent**

Start it by using the line: `$ eval $(ssh-agent -s)`

Then, add the private ssh key to the ssh-agent using the filelocation: `$ ssh-add ~/filename`

**Adding public key to Github**

Copy the contents of your SSH public key.

Then login to your Github account in the browser. Then, in the top right corner, press your profile button and then settings.

In the sidebar on the left, press "SSH and GPG keys".

Click "New SSH key" and in the title field write a descriptive label for the key.

Choose either "Authentication key" or "Signing key". For this, chhose "Authentication key" or read more about signing commits [here](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification).

Paste the contents of your SSH public key into the "Key" field and press the "Add SSH key" button.

You have now created a SSH key to use as authentication when connecting with Github.

**Useful Git commands**

```
git init
```

This initializes a Git repository in a certain folder.

```
git branch
```

With this you can add a branch, view the existing branches and delete a branch.

```
git checkout
```

Is used to navigate existing branches and can also discard changes you've made.

```
git add \<filename> // git add -A
```

This moves your changes from the working directory to the staging area. Either choosing one file, \<filename>, or every file in the folder, -A.

```
git remote add \<shortname> \<repository url>
```

This adds a remote to a repository on Github. Choose a shortname, often named "origin", and the link to the Github repository.

```
git push
```

This is used to share your changes in the code and "push" them, often to a Github repository. You can also add \<remote> \<branch> after "push" which enables you to push it to a certain branch.

```
git pull
```

This is used to integrate the remote changes in a project to your working branch.

```
git clone
```

This allows you to get a copy of an existing Git repository. With this you can make contributions or just look at code other people have made.

```
git commit -m "\<your commit>"
```

When you use this command it saves your changes to the Git repository. This allows you to revert back to any of these points where you made a commit.

```
git config --global
```

- This is used to set your login in info in Git.

  If followed by:

  ```
  user.email "<example@example.com>"
  ```

  to set your email

  ```
  user.name "<username>"
  ```

  to set your username

### **How git works**

![gitFlow]

## **FAQ**

**What is Github?**

```

Github is a software development platform online. You can use it to store your projects, track your progress and collaborate on projects with other users. It is very easy to access your code or anyone else's. You can look at what other people have done, download their code, and even contribute to it.

```

**Why do I need Github?**

```

Github is an easy way to store your code and collaborate with others on projects. When someone contributes with a change you can always look at what they have changed and simply pull the code so you have the latest changes locally.

```

**Common issues when collaborating using Git**

```

Merge conflicts can be very annoying, but there are some things you can try and do to avoid them:

Make sure you use "git pull" often to always have the latest changes and avoid unnecessary conflicts.

If you have multiple branches make sure to push your changes to the correct branch.

But, if you happen to get a merge conflict, there are a few ways to handle it:

Maybe you just made a mistake, then you can write "git merge --abort" in the console to abort the merge

A simple way to resolve a conflict is using "checkout". When you know whose version of the file you want to keep you can write one of two lines in the console:
Keep your own file: "git checkout --ours <filename>"
Keep your collaborators file: "git checkout --theirs <filename>"

Another way to fix it is to pull and edit the file. You can do this using Visual Studio Code. VSCode shows you exactly what the conflict is which makes it easy to edit to fix the conflict.
```

[vscode]: https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white
[vscode-url]: https://code.visualstudio.com/
[git]: https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white
[git-url]: https://git-scm.com/
[edge]: https://img.shields.io/badge/Microsoft_Edge-0078D7?style=for-the-badge&logo=Microsoft-edge&logoColor=white
[edge-url]: https://www.microsoft.com/edge
[node.js]: https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white
[node-url]: https://nodejs.org/
[gitflow]: gitFlow.png
