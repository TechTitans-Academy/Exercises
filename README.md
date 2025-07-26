# GitHub Hands-on Exercise. 

## Pre-requisites:

1. Ensure you save a personal copy of the scenario answers along with all relevant Git commands.
2. For each scenario, capture and document the output of git log before and after performing the solution steps.

## Q1. Creating a Repository

- Go to GitHub and make a new repository. Name it `cloneme`.
- Inside that repository, create a new file called `script.py`.
- In that file, add the following line of code:
```
print(f"Line-1")
```
- Now, copy the link to your GitHub repo and use it to download (clone) the repo to your computer.

## Q2. Making a Save Point (Commit) in Your Code

- First, download (clone) your GitHub repo to your computer if you haven't already.
- Inside the folder you downloaded, run the command to start using Git (initialize Git).
- Make some changes to the file then save the changes as a commit.
- After saving, send (push) those changes back to GitHub so they are stored online.

## Q3. Working with Branches

[This is a follow-up to Q2.]
- Imagine you’re ready to show your project to customers.
- Create a new branch called `release`.
- In this new branch, make changes to the `script.py` file.
- Save these changes as a commit in the `release` branch.
- Now that the release branch has new updates, you need to merge those updates back into the main branch.
- After merging, push (upload) the changes to GitHub on `main` branch only.
- Finally, check your GitHub page to verify the changes have been uploaded. Review the commit page as well.

## Q4. Undoing Changes Using Git Reset

[You don’t need GitHub for this one—just do it on your computer.]
1. Make a folder and start using Git inside it.
2. Create a file called code.txt, write something in it, and save it as your first commit.
3. Make 3 more changes (commits), so now you have 4 commits total.
4. Now, let’s say you want to undo the last 2 changes (commits). What command would you use?
5. Show the command you ran and the list of commits logs before and after the reset.

## Q5. Fixing a Mistake in Your Last Commit

- You’re working in a branch called feature/login-page and made these 3 commits:
	- Added the login form
	- Designed the login button
	- Removed the password field.
- You now realize the password field should not have been removed.
- What Git command would you use to undo only the last change?
- Try this out in your local computer by creating a test directory and inintating a git:
	- Make 3 similar commits
	- Then undo only the last commit
	- Share the steps and solution.
	- Compare the commit log output before and after.

## Q6. Squashing Commits (Combining Them)

- Run this command in your terminal to create a test project with 5 commits:
```
mkdir -p /tmp/techtitans && cd /tmp/techtitans && git init && touch code.txt && for i in {1..5}; do echo "Line-$i" >> code.txt && git add code.txt && git commit -m "$i-commit"; done
```
- Now, you want to combine the last 2 commits into one.
- Use Git’s squash command to do this.
	- When you’re inside the squash window:
		- Change the first pick to r
		- Change the second pick to s
	- Save and exit.

## Q7. Connecting Your Project to GitHub (Remote Work)

- Run this in your terminal to create a new test project and make 2 commits:
```
mkdir -p /tmp/myremote && cd /tmp/myremote && git init && touch code.txt && for i in {1..2}; do echo "Line-$i" >> code.txt && git add code.txt && git commit -m "$i-commit"; done
```
- Go to GitHub and make a new repository called `myremote`.
- Copy the remote URL of your GitHub repo.
- Use the Git command to connect your local project to the GitHub repo (set up the remote).
- Then push (upload) your code to GitHub.

## Q8. Git Rebase vs Merge
- <b>Scenario</b>: Your team uses both git merge and git rebase in different situations
- <b>Question</b>: What are the key differences between the two, and when would you prefer one over the other?
