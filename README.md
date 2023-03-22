# github-intro-repo

A repo to introduce those new to collaborative development on git


[Link to Notion Article](https://sugar-cheque-304.notion.site/GitHub-in-a-Nutshell-df079c88b0334b7fbee5eadde15bd0e9)


# GitHub in a Nutshell


- Check if Git is already installed on your Ubuntu

```bash
git --version
```

- If not

```bash
sudo apt update
sudo apt install git
```

- Create a [GitHub account](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)
- Create a repository on the website, or find a repository of interest to which you have collaborative access as follows.

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled.png)

- Click on the green button drop-down saying Code

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%201.png)

- Create an SSH key if prompted, following these for instructions
- Links for SSH key generation
    
    [Generating a new SSH key and adding it to the ssh-agent - GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux)
    
    [Adding a new SSH key to your GitHub account - GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
    
- After generating an SSH key copy the link in SSH column of Code dropdown
- Clone the repository as follows

```bash
git clone git@github.com:rohankalbag/github-intro-repo.git
```

*Aside: make sure to star a repo whenever you clone it to show your appreciation to the developer* 

- you should see something like this

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%202.png)

- enter the repository directory, to make a dummy commit onto the main branch do the following see the following code next (not recommended however), development should generally done on branches and later merged into main

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%203.png)

- the above changes will be held locally to push it to the GitHub remote upstream do the following

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%204.png)

**How to work on branches** 

- I will create a branch for my commits in a branch called `rohan`
- I will make a change in `intro_logs.txt` and make a commit

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%205.png)

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%206.png)

- This pushes the changes only to the `rohan` branch on the repo and doesn’t modify the main branch

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%207.png)

- how to check progress of someone else’s work on a different branch, if you are in a collaborative team ?

```bash
git switch that_branch
git log
```

- What if you want to merge your changes onto the main branch without any conflicts? (very important so pay attention :D)
    - Just for an example I will make some changes on the main repo by adding something to the `./readme.md` file on the remote and I have to make sure to take that change into my branch before making a pull request. Added the orange line for example
    
    ![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%208.png)
    
    ![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%209.png)
    
    - Now there is a change on the remote which I don’t have locally so I should be careful to consider it
    
    ![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%2010.png)
    
    ```bash
    #this is important to prevent conflicts
    git merge origin/main
    # a pop up might come here asking for commit message, exit the window with ctrl + x
    git push
    ```
    

**Time to create a pull request**

- Open your GitHub repo, and click on compare and pull request

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%2011.png)

- click on create pull request

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%2012.png)

- you can assign your teammates as reviewees just to make sure before merging
- if you have discussed and you are ready to merge this into the main repository then click/ask your teammates to click on **merge pull request** and we are done.

![Untitled](GitHub%20in%20a%20Nutshell%20df079c88b0334b7fbee5eadde15bd0e9/Untitled%2013.png)

- your changes would now reflect on the main branch of the repo, congratulations you have successfully made your first successful contribution.

## You are armed with the basic skills need to collaborate on GitHub now

- If you need some more info, always use Stack Overflow, ask people around you or check Git documentation online/the man page

```bash
man git
```

### created with ❤️ by Rohan
