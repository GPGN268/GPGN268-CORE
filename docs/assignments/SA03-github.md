
# 🪚 Sharpening the saw: GitHub
Due end of day Monday Feb 9th 2026.

## Part I: Developing your resume 
For this exercise, we will continue working on the `resume.md` file that you created earlier this week. First, open the terminal and navigate to your resume directory

```
$ cd ~/work/classes/GPGN268/resume
$ ls -F
resume.md
```

Check the status of your repository to make sure there aren't any changes that have not been committed.

```
$ git status

On branch main
nothing to commit, working tree clean
```

⚠️ In case you made changes to `resume.md` directly on GitHub (using the browser), you need to pull these changes to your local repository to make sure everything is in sync.

```
$ git pull
```

Now, edit your resume to make it more complete. An example resume for Blaster is shown below. You may choose to do this for you (adding information about yourself) or you can create a fictional character.  **Your document must have at least:**

- [ ] Two levels of section headings
- [ ] One image
- [ ] Something in bold
- [ ] A list
- [ ] A hyperlink

![sample-blaster-resume](https://user-images.githubusercontent.com/2079352/215233684-f9e33a99-a61b-4bad-9be4-fff88e791770.png)


Save your modifications. Commit your changes and push them to the GitHub remote repository. You can check your work at  `http://github.com/<your github username>/resume`

To “hand in” this part of the assignment, put a link to your resume in the `README.md` file in the next part.

## Part II: Updating your coursework repository

Using the terminal, navigate to your coursework directory

```
$ cd ~/work/classes/GPGN268/coursework-yourlastname
```

⚠️ Remember to check for the status of your repository using `$ git log`. In case you made changes to `README.md` directly on GitHub (using the browser), you need to pull these changes to your local repository to make sure everything is in sync.

⚠️ Sorry I got stuck in class, you can try this. After 
```
$ git remote add origin git@github.com:GPGN268/coursework-yourlastname.git
```
You should do
```
git pull --rebase origin main
```
Then
```
git push origin main
```
And that might work (data set size of 2). If that does not work for you, don't worry. You can edit the README.md on GitHub. But try to do tit he way below just for extra practice with git. Thanks!

Open the `README.md` file that you created. Now, add a section "Short Assignments" to your file and add a link to your resume. Save. Stage and commit your changes. Push it to your remote repository.

```
$ vim README.md
```

```
# Your Name
## Short Assignments
### SA03 - GitHub 
- [My resume](link-to-your-resume)
```

