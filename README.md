# unity-game-template
This is a repo set up w/ proper gitignore and project board for a game development team using Unity


## Git Workflow
- 📌Clone down the organization's repo as your `origin` ("the trunk" | "the org repo" | "org remote" | "origin")
  - This should probably be done as a .zip
- 📌Pick up a Ticket from the [Project Board](https://github.com/orgs/<org-name/projects/1/views/1)
  - Assign yourself to the ticket and move it into the "In Progress" lane
  - Create a branch directly from that ticket's full view on GitHub<sup>see diagram 1.0 - 1.2</sup>
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

## Footnotes:

diagram<sup>1.0</sup>
![image](https://github.com/Nola-Devs/Nola-Devs-v2/assets/92059005/2e40f7b5-e109-4062-b323-96228da620bd)

diagram<sup>1.1</sup>
![image](https://github.com/Nola-Devs/Nola-Devs-v2/assets/92059005/012294aa-41c0-4a0e-aa19-1ea287045eb5)

diagram<sup>1.2</sup>
![image](https://github.com/Nola-Devs/Nola-Devs-v2/assets/92059005/9ebcf2a7-ef65-43ff-8cf4-193af1a6239b)
