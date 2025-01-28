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
