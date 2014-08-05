# Accessing GitHub Repositories

# The Ocean Health Index and GitHub 
The Ocean Health Index (OHI) uses [GitHub](http://github.com), an [open-source development platform](http://en.wikipedia.org/wiki/GitHub) to develop and share software and data. GitHub has powerful versioning capabilities, which allow changes to be archived and tracked by each user.
  
OHI has several repositories ('repos') where data and code are stored. From the [GitHub glossary](https://help.github.com/articles/github-glossary#repository): 

> A repository is the most basic element of GitHub. They're easiest to imagine as a project's folder. A repository contains all of the project files (including documentation), and stores each file's revision history. Repositories can have multiple collaborators and can be either public or private.

[OHI-Science](https://github.com/OHI-Science) is the 'owner' of OHI repositories, and individual users contribute to these repositories when they have permission. Here is a simple diagram of GitHub's collaborative workflow, with the example of the `ohi-israel` repo owned by `OHI-Science`:

> ![](zfig_clone_push_pull.png)

### OHI regional assessments and GitHub
We recommend that groups interested in conducting OHI assessments do so through GitHub. This will enable collaboration and transparency, and will provide access to the latest developments in the Toolbox software. To get started, follow the steps below for creating a GitHub user account. The OHI team will create a repository for your regional assessment.  
  

## Sign up for GitHub
To get started, [signup](http://github.com) for a GitHub account, and provide your username to bbest@nceas.ucsb.edu or lowndes@nceas.ucsb.edu so you can access your ohi-[assessment] repository.

## Install *git*
*git* is required to work behind the scenes on your computer. [Download](http://git-scm.com/downloads) and install *git*. (Here are a few [tips](https://github.com/OHI-Science/ohiprep/wiki/Setup#git) 

## Create your ohi-[assessment] repo
Contact the OHI team (bbest@nceas.ucsb.edu or lowndes@nceas.ucsb.edu) to create a repository for your group. The repository will be called `OHI-Science/ohi-[assessment]`: for example, `OHI-Science/ohi-israel`.

## Clone your repo to your computer

Once there is a repository for your OHI regional assessment called `OHI-Science/ohi-[assessment]`, you can decide whether you will clone and work directly from that repository  or from a forked repository. There are benefits to both approaches:

* Working directly from the repository is simplest: you can make changes on your local computer and push them directly to the online repository, as in the figure above. You do not need to send pull requests; simply clone from `OHI-Science/ohi-[assessment]` (see [Cloning options](https://github.com/OHI-Science/ohimanual/blob/master/tutorials/accessing_a_repo/accessing_a_repo.md#cloning-options)) and push/pull from there.
* [Forking](https://help.github.com/articles/fork-a-repo) a repository is best when you have multiple collaborators working on the same repository. This would allow you to commit changes to your local version, push commits up to github for offsite archiving, and eventually make a pull request to have those changes merged back to `ohi-science/ohi-[assessment]` while your collaborators do the same. This is a good way for someone who is not in the core team of the assessment to contribute comments.

With either approach, we recommend cloning the repository to this file path: `~/github/ohi-[assessment]`. See [Setup](https://github.com/OHI-Science/ohiprep/wiki/Setup) for installation of git, GitHub and RStudio. 

### Cloning options
There are several options to clone the ohi-[assessment] repository to your local machine:

1. [The command line](https://help.github.com/articles/fork-a-repo#keep-your-fork-synced).
2. The GitHub app for [Mac](https://mac.github.com/) or [Windows](https://windows.github.com/).
3. RStudio. This is best after the initial clone, since RStudio occassionally has trouble with setting the username / password. 
(https://github.com/OHI-Science/ohiprep/wiki/Setup#github_fork)

Note that for each of these options, you will need to first [set up git](https://help.github.com/articles/fork-a-repo#step-1-set-up-git). From the [git documentation](http://git-scm.com/book/en/Getting-Started-First-Time-Git-Setup#Your-Identity): 

> "This is important because every Git commit uses this information, and it’s immutably baked into the commits you pass around." 

Launch Terminal in Mac or go to command line in Windows (Start > Run > cmd) and substitute your user information with the user John Doe:

```{bash}
git config --global user.name jdoe
git config --global user.email johndoe@example.com
git config --list
```

You can check settings with the following:

```{bash}
git config --list
```


## Committing locally
Commit locally, associating a message with each set of changes.

## Push commits to GitHub ohi-[assessment] repository.

## Pull commits to get changes from anyone else.


## More Information

* [presentation: Reproducible science with the Ocean Health Index](http://bbest.github.io/talks/2014-06_OHI-repro-sci/#1)
* [wiki: Using GitHub](https://github.com/OHI-Science/ohiprep/wiki/Using-GitHub)
* see www.oceanhealthindex.org and ohi-science.org for more information and resources.  
