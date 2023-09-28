# jays_resume
latex based resume

## Features
- Latex based resume

## Planned Features
- modular sections for maintainability
- github actions to render pdf version

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