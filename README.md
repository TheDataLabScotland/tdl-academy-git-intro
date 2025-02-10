![The Data Lab, University of Glasgow, and University of Edinburgh combined logo](images/combined_logo.png)

# Introduction to git and GitHub webinar


## Ideas for content:

- Intro
	- Why version control is important, why should you learn git and GitHub?
		- expected skill to have if in a role which requires coding
	- There's many different version control tools out there, git is just one of them that is widely used
	- Difference between git and GitHub

- Slides on [basic git commands](https://docs.github.com/en/get-started/using-git/about-git#basic-git-commands) with nice visualisations to explain concepts such as origin and remote/push and pull, branching, pull requests, etc.

- Maybe highlight useful GUI tools to use with git? eg. RStudio has a nice in-built feature... GitHub dekstop? VSCode?

- A few slides each on how we both use git day-to-day, highlight tips and tricks we both find useful? Or story/experience of using git?

- Maybe a bit too advanced... highlighting some other useful features of GitHub - eg. GitHub actions, deploying a website with GitHub pages?

## Repository setup

The current repository has the following structure (designed around building a [Quarto](https://quarto.org/) based introduction to git presentation)

```
📦tdl-academy-git-intro
 ┣ 📂images # required images like logos
 ┣ 📜.gitignore # what git should ignore
 ┣ 📜.pre-commit-config.yaml # pre-commit setup
 ┣ 📜introduction_to_git.qmd # quarto presentation
 ┣ 📜LICENSE # open-source license
 ┣ 📜presentation_styles.css # style additions to quarto presentation
 ┗ 📜README.md # <- you are here
```

## `git` command glossary
Here are a few useful `git` commands and what they do:
|Command                                                  |Definition                                                                                                                                                                            |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`git status`                                             |Check current status of local repository - is it up to date?                                                                                                                          |
|`git pull`                                               |Pull changes from GitHub to local repository                                                                                                                                          |
|`git add [FileName]`                                     |Stage file for committing                                                                                                                                                             |
|`git commit -m [message]`                                |Commit staged changes to GitHub. Always add meaningful message.                                                                                                                       |
|`git push`                                               |Push committed changes to GitHub                                                                                                                                                      |
|`git fetch`                                              |Get latest version references for repository                                                                                                                                          |
|`git stash`                                              |Stash changes so that I can send to different branch ( I use when I forgot to switch branches before making change. Run this command - then switch to branch - then run command below)|
|`git stash pop`                                          |Unstash changes that were previously stashed (Used in combination with command above to move changes onto different branch)                                                           |
|`git branch`                                             |List existing branches                                                                                                                                                                |
|`git branch [branchName]`                                |Create new branch                                                                                                                                                                     |
|`git push --set-upstream origin [branchName]`            |Push a branch online                                                                                                                                                                  |
|`git branch -d [branchName]`                             |Delete branch                                                                                                                                                                         |
|`git checkout [branchName]`                              |Switch to branch                                                                                                                                                                      |
|`git checkout -t origin/[branchName]`                    |Switch to remote branch (note you'll need to run git fetch first)                                                                                                                     |
|`git merge [branchName]`                                 |Merge changes from one branch to another                                                                                                                                              |
|`git rm [fileName]`                                      |Remove file and record                                                                                                                                                                |
|`git mv [fileName]`                                      |Move file and version history within repository                                                                                                                                       |
|`git reset`                                              |Remove any staged/added files                                                                                                                                                         |
|`git diff [fileName]`                                    |Check for any changes in a file compared to when the file last had a commit associated with it                                                                                        |
|`git add --patch`                                        |Select a particular change within a file to stage/add and commit
|`git --help`                                             |Get help on any git command                                                                                                                                                           |

### Quarto installation

[Quarto](https://quarto.org/) is an open-source report/presentation building tool that can be used across a range of programming languages. It is based on [Rmarkdown](https://rmarkdown.rstudio.com/) - a reporting tool for the R programming language. The introduction to git presentation is built using the `introduction_to_git.qmd` file producing the `introduction_to_git.html`. To edit and build the `html` based output presentation, you'll need to [install Quarto](https://quarto.org/docs/get-started/) and use a tool like [RStudio](https://posit.co/downloads/) or [Visual Studio Code](https://code.visualstudio.com/).

### `pre-commit` installation

The current repository uses a [pre-commit](https://pre-commit.com/) workflow to run some simple checks and formatting steps on any changes you are committing before pushing them to your remote (online) repository on GitHub. If you'd like to using the pre-commit workflow while editing this codebase you can install it by following these steps:

To install the `pre-commit` workflow, follow these steps:
1. Install the [python](https://www.python.org/downloads/) programming language
2. Install pre-commit with: `pip install pre-commit` in the command line
3. Navigate to your repository on your computer in the command line and run `pre-commit install`

## Some useful resources

- [Introduction to GitHub](https://docs.github.com/en/get-started/start-your-journey/hello-world)
- GitHub [documentation](https://docs.github.com/en) pages
- A [game](https://learngitbranching.js.org/) to help us think about git branches
- See this `git` in the command line [tutorial](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line)
- Check out the [`git` handbook](https://guides.github.com/introduction/git-handbook/)
- [`git` glossary](https://github.com/datasciencecampus/gov-uk-rap-materials/blob/master/git-glossary/git-command-glossary.csv) of commands to remember
- Check out [`git` flow](https://www.alexhyett.com/git-flow-github-flow/) for collaboration
