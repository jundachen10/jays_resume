# [*View Resume*](https://github.com/jundachen10/jays_resume/blob/main/Jay_Chen_Resume.pdf)
## Features
- [**LaTeX**](https://www.latex-project.org) resume
- Github actions
- Generates pdf resume file with each commit
- Modular structure for easier maintenance
## What I learned
- Github Actions triggers. In this repo we trigger the action on a push while ignoring triggers on markdown files with the paths-ignore: attribute.
- Refactor out components in a LaTeX document by using \input{src/NAME}.
- The Yaml actions file and creating jobs that run as well as multi line run commands.
- Refreshed myself on how to deal with divergent branches. There's an issue where the action will auto generate .aux and .log files and push to the repo. If I don't pull these changes from the repo to the local, then a merge conflict can result.
- How to set up Personal Access Tokens that work with Actions, and how to load the token into the repo using the command line.
## Planned Features
- Automated deploy using actions on github pages.
- Look to include a pull command in the yaml file.
## Challenges 9.28.23
- when deploying the action I ran into an PAT Token auth issue. My existing PAT did not have workflow access.
- github actions Node12 deprecated and uses Node16
- new PAT still doesn't work, going to see if repo settings are blocking it.
## Solutions 9.28.23
- generate a new PAT with workflows access
- change the current repo remote path to HTTPS
- load the new PAT in the command line
- not only was it the PAT workflow access check box, it was also the repo settings not allowing WRITE access

- here are the commands
<ul>git remote -v</ul>
<ul>git remote -v</ul>
<ul>git remote remove origin</ul>
<ul>git remote add origin https://MyAuthToken@github.com/MyUserName/MyRepo.git<ul>
