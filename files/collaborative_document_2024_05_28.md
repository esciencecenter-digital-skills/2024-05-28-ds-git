![](https://i.imgur.com/iywjz8s.png)


# Collaborative Document

2024-05-28 Collaborative version control with git and GitHub (2024-05-28-ds-git)

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: [link](https://tinyurl.com/2024-05-28)
https://tinyurl.com/2024-05-28


##  🫱🏽‍🫲🏻 Code of Conduct

Participants are expected to follow these guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.
 
 For more details, see [here](https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html).

Want to report a Code of Conduct incident and you prefer to do it anonymously? You can do it [here](https://goo.gl/forms/KoUfO53Za3apOuOK2).

## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, just raise your hand.

If you need help from a helper, place a pink post-it note on your laptop lid. A helper will come to assist you as soon as possible.

## 🖥 Workshop website

[Link](https://esciencecenter-digital-skills.github.io/2024-05-28-ds-git)

🛠 Setup

We will assume everyone can access the command line on their laptop and managed to follow these [**setup instructions**](https://esciencecenter-digital-skills.github.io/2024-05-28-ds-git/).

Please put a pink post-it note on you laptop lid, if you need a bit more help with the setup.

## 👩‍🏫👩‍💻🎓 Instructors

Olga Lyashevska, Sven van der Burg

## 🧑‍🙋 Helpers

Sven van der Burg

## 👩‍💻👩‍💼👨‍🔬🧑‍🔬🧑‍🚀🧙‍♂️🔧 Roll Call
Name/ pronouns (optional) / job, role / social media (twitter, github, ...) / background or interests (optional) / city

## 🗓️ Agenda

|  Time | Topic                             |
| -----:|:--------------------------------- |
| 09:30 | Welcome and icebreaker            |
| 09:45 | Workshop Introduction             |
| 10:00 | Version control with Git          |
| 10:30 | **Coffee break**                  |
| 10:45 | Version control with Git          |
| 11:30 | **Coffee break**                  |
| 11:45 | Version control with Git          |
| 12:30 | **Lunch Break**                   |
| 13:30 | Collaboration with Git and GitHub |
| 14:15 | **Coffee break**                  |
| 14:30 | Collaboration with Git and GitHub |
| 15:15 | **Coffee break**                  | 
| 15:30 | Collaboration with Git and GitHub |
| 16:15 | Wrap-up                           |
| 16:30 | DRINKS 🍾🍻                        |
	

## 🏢 Location logistics
* Coffee and toilets
* Emergency exit
* Wifi

## 🎓 Certificate of attendance
If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl .

## :ice_cream: Icebreaker
**Imagine you are a flavour. Which would you be and why?**

[Think of flavours that flavor reflect your personality, work style, or approach to collaboration.

E.g. "I would be strawberry because I'm sweet and approachable. I bring a positive, friendly vibe to the group and help keep morale high."]


## 🔧 Exercises

### Places to Create Git Repositories

Along with tracking information about planets (the project we have already created),
Dracula would also like to track information about moons.
Despite Wolfman's concerns, Dracula creates a `moons` project inside his `planets`
project with the following sequence of commands:

```bash
$ cd ~/Desktop   # return to Desktop directory
$ cd planets     # go into planets directory, which is already a Git repository
$ ls -a          # ensure the .git subdirectory is still present in the planets directory
$ mkdir moons    # make a subdirectory planets/moons
$ cd moons       # go into moons subdirectory
$ git init       # make the moons subdirectory a Git repository
$ ls -a          # ensure the .git subdirectory is present indicating we have created a new Git repository
```

Is the `git init` command, run inside the `moons` subdirectory, required for
tracking files stored in the `moons` subdirectory?

### Tracking changes exercise

#### 1. Which command(s) below would save the changes of myfile.txt to my local Git repository?

1. `git commit -m "my recent changes"`
2. `git init myfile.txt`
   `git commit -m "my recent changes"`
3. `git add myfile.txt`
   `git commit -m "my recent changes"`
4. `git commit -m myfile.txt "my recent changes"`




#### 2. Committing Multiple Files
Remember that the staging area can hold changes from any number of files that you want to commit as a single snapshot.

1. Add some text to ``mars.txt`` noting your decision to consider Venus as a base
2. Create a new file ``venus.txt`` with your initial thoughts about Venus as a base for you and your friends
3. Add changes from both files to the staging area, and commit those changes.

#### 3. (optional) A new repository
1. Create a new Git repository on your computer called bio.
2. Write a three-line biography for yourself in a file called me.txt.
3. Add the file to the staging area, and commit your changes.
4. Make a modification.
5. Display the differences between its updated state and its original state.


### Exploring history exercise

#### 1. Recovering Older Versions of a File
Jennifer has made changes to the Python script that she has been working on for weeks, and the modifications she made this morning “broke” the script and it no longer runs. She has spent ~ 1hr trying to fix it, with no luck…

Luckily, she has been keeping track of her project’s versions using Git! Which commands below will let her recover the last committed version of her Python script called `data_cruncher.py?` Multiple options might be correct:


1. `$ git checkout HEAD`
2. `$ git checkout HEAD data_cruncher.py`
3. `$ git checkout HEAD~1 data_cruncher.py`
4. `$ git checkout <unique ID of last commit> data_cruncher.py`
    
    
A:     I think they all work , except 3. I think 3 recovers the version before the latest committed one.

#### 2. (optional) Understanding Workflow and History

What is the output of the last command in
```
$ cd planets
$ echo "Venus is beautiful and full of love" > venus.txt
$ git add venus.txt
$ echo "Venus is too hot to be suitable as a base" >> venus.txt
$ git commit -m "Comment on Venus as an unsuitable base"
$ git checkout HEAD venus.txt
$ cat venus.txt #this will print the contents of venus.txt to the screen
```
1. Venus is too hot to be suitable as a base
2. Venus is beautiful and full of love
3. Venus is beautiful and full of love
4. Venus is too hot to be suitable as a base
5. Error because you have changed venus.txt without committing the changes

CORRECT ANSWER: 

The answer is 2.

The command git add venus.txt places the current version of venus.txt into the staging area. The changes to the file from the second echo command are only applied to the working copy, not the version in the staging area.

So, when git commit -m "Comment on Venus as an unsuitable base" is executed, the version of venus.txt committed to the repository is the one from the staging area and has only one line.

At this time, the working copy still has the second line (and git status will show that the file is modified). However, git checkout HEAD venus.txt replaces the working copy with the most recently committed version of venus.txt.


#### 3. (optional) Reverting a Commit

Jennifer is collaborating on her Python script with her colleagues and realizes her last commit to the project’s repository contained an error and she wants to undo it. `git revert [erroneous commit ID]` will create a new commit that reverses Jennifer’s erroneous commit. Therefore `git revert` is different to `git checkout [commit ID]` because `git checkout` returns the files within the local repository to a previous state, whereas `git revert` reverses changes committed to the local and project repositories.
Below are the right steps and explanations for Jennifer to use `git revert`, what is the missing command?

1. `________ # Look at the git history of the project to find the commit ID`
2. `Copy the ID (the first few characters of the ID, e.g. 0b1d055).`
3. `git revert [commit ID]`
4. Type in the new commit message.
5. Save and close

CORRECT ANSWER: `git log`

* Funda: 
* Allerdien: 3 & 4
* Koen: 2&4, 2&3, git log
* Anneke: 1+2+4, 2&3
* Aske: 2 & 4
* David: 3 & 4


### Optional exercises during SSH setup check
#### 1. CHECKING UNDERSTANDING OF `git diff`
Consider this command: `git diff HEAD~9 mars.txt`. What do you predict this command will do if you execute it? What happens when you do execute it? Why?

Try another command, `git diff [ID] mars.txt`, where [ID] is replaced with the unique identifier for your most recent commit. What do you think will happen, and what does happen?

#### 2. GETTING RID OF STAGED CHANGES
`git checkout` can be used to restore a previous commit when unstaged changes have been made, but will it also work for changes that have been staged but not committed? Make a change to mars.txt, add that change using `git add`, then use `git checkout` to see if you can remove your change.

#### 3. IGNORING NESTED FILES
Given a directory structure that looks like:

```bash
results/data
results/plots
```

How would you ignore only `results/plots` and not `results/data`?

#### 4. INCLUDING SPECIFIC FILES
How would you ignore all `.csv` files in your root directory except for final.csv? Hint: Find out what `!` (the exclamation point operator) does

Add me (koen) as a collaborator @github: koen-leijnse
or collab at https://github.com/koen-leijnse/oak

#### Exercise: Working as a project collaborator (in groups):
- Log into Github and create a new repository
- Make the repository public
- clone it to your desktop
- add some code
- push the changes to the repository
- Add one person as a collaborator (settings -> Manage Access). Make sure everyone in the group has a collaborator.
- Clone that repo
- make changes on a new branch
- push the changes
- submit a Pull Request
- wait for approval
- At the same time review a collaborators Pull Request
- (Optionally) Learn about [protecting branches](https://docs.github.com/en/github/administering-a-repository/about-protected-branches) and try it out. 

#### Exercise: Working as an external contributor (in breakout rooms):
- Remove your group member(s) as collaborators from your repository
- Fork another group members repo (Repository page, top right corner)
- Create an issue on the original repository
- Clone your forked repo to your computer
- Make some changes, use a somewhat real-world example so it makes sense to review it (but don't overdo it).
- Push it to your fork
- make a pull request from your fork to the main repository mentioning the issue
- Consider turning your Pull Request into a draft Pull Request.
- let your code be reviewed by tagging the repo owner using (@Username)
- At the same time review Pull Request using comments on individual lines. Try to act as if it was a real peer review as much as possible.
- Accept or reject the Pull Request
- (Optionally) learn about [merge conflicts](https://www.atlassian.com/git/tutorials/using-branches/merge-conflicts) and try it out in your collaboration. 


## 🧠 Collaborative Notes

## :ear: Feedback
### What went well?
* The pace is ok, it's not too fast
* The level of exercises are optimal
* It is good to do it from bash, so no other program knowledge needed
* Small group
* It is nice with a visual guide
* Personal guidance
* learned a lot
### What can be improved?
* Adding use of main commands/functions in the slides could useful (while co-writing the code I get too excited to code and cannot follow info that might be important)
* a bit too easy
* Trying implementation with python or other language
* Example usage with IDE, like VS Code -> good idea
* a little bit deeper. Beter understanding of difference repository and branch


## 💬 Post-workshop survey
https://www.surveymonkey.com/r/PGGPP7K

## 📚 Resources
* Upcoming workshops: https://www.esciencecenter.nl/events/?f=workshops
* Schedule of all workshops in the year: https://www.esciencecenter.nl/digital-skills/ (scroll down)
* Subscribe to our newsletter (stay updated on upcoming workshops): eepurl.com/dtjzwP
* Slides: https://lyashevska.github.io/ds-cr-slides/
* Really nice free book: https://git-scm.com/book/en/v2
* Blog about atomic commits: https://blog.esciencecenter.nl/the-utopic-git-history-d44b81c09593
* Git cheat sheet: https://education.github.com/git-cheat-sheet-education.pdf
* A logical, reasonably standardized but flexible project structure for data science.: https://cookiecutter-data-science.drivendata.org/
* Lesson material collaborating in the same repository https://coderefinery.github.io/git-collaborative/same-repository/
* Lesson material collaborating to a repository from someone else: https://coderefinery.github.io/git-collaborative/forking-workflow/


