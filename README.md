# unity-game-template
This is a repo set up w/ proper gitignore and project board for a game development team using Unity

## How to hook up Unity to Git/GH
- [ ] Make a Repository on GitHub (GH)
- [ ] Make a new project from Unity Hub (UH)
	- [ ] Make the name of the project the SAME as the cloned down repo (should just be the name of the repo (_sans-"main"_))
- [ ] Create a script in your new Unity project (within Unity) to open VS inside of it
- [ ] Open a terminal in the root folder in VS (your unity proj)
- [ ] Run `git init` to initialize a git repo inside of it
- [ ] Create a `main` branch if it isn't autogenerated from `git init`
- [ ] Run `git remote -v` to see if `origin` has been created automatically or not...
- [ ] If it HAS:
	- [ ] Run `git remote set-url origin https://gihub.com/your/repo.git`
	- [ ] to set the remote URL for origin to your clone URL for the GH repository
- [ ] Perform ONE of the FOLLOWING (**A** or **B**):
- [ ] **A:**
	- [ ] Run `git pull origin main` 
- [ ] **B.1: **(_if you have anything in your Unity git repo that you need merged with the remote repo_)
	- [ ] In the terminal where you ran `git init` (the root of your Unity project) run `git checkout main` (_if you are not already in main_)
	- [ ] Run `git branch -m main-holder` to rename this branch temporarily
	- [ ] Run `git fetch`
	- [ ] Run `git checkout main`
	- [ ] Run `git pull origin main` this will create a local main that matches the remote main and sync
	- [ ] Run `git merge main-holder --allow-unrelated-histories` to merge anything you need from your local Unity project
	- [ ] _If any of the above steps **fail** and you don't want to debug... (**experimental**)_ 
- [ ] **B.2:** (only if **B.1:** has failed)
	- [ ] In a new terminal or system explorer Navigate to the parent folder where your Unity project sits.
	- [ ] Run `git clone https://gihub.com/your/repo.git`
	- [ ] In the terminal where you ran `git init` (the root of your Unity project) run `git checkout main` (_if you are not already in main_)
	- [ ] Run `git merge ../your-cloned-gh-repo/main --allow-unrelated-histories` to merge the main from your local version of the remote GH repo into your local Unity project git repo you created
- [ ] Handle the merge into your Unity Project's git repository where the C# scripts will now be added by default from within the Unity Editor

## Git Workflow
- 📌Clone down the organization's repo as your `origin` ("the trunk" | "the org repo" | "org remote" | "origin")
  - This should probably be done as a .zip
- 📌Pick up a Ticket from the [Project Board](https://github.com/orgs/<org-name/projects/1/views/1)
  - Assign yourself to the ticket and move it into the "In Progress" lane
  - Create a branch directly from that ticket's full view on GitHub
- 📌Fetch from `origin main` (paste what you copied) in your IDE and checkout your new feature-branch which should share the same name as the issuing ticket
- 📌Use [Semantic Commit-Messages](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716) for feature development
- 📌Push your feature-branch to the trunk remote `git push origin feature/ticket-branch`
- 📌PR Workflow
  - 📝Author: PR to main for Code Review
    - 🔎Reviewer: "Approval" is required - this means acknowledging what the push will change
  - 📝Author: merges into `main`
    - 🔎Reviewer: checks out `main` and builds in Unity from new `main`
    - 🔎Reviewer: tests in Unity
    - 📌Once tested, notify 📝Author of approval
- 🎇PR to `prod` and merge


