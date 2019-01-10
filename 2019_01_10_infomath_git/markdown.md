class: title-slide

# Git: Why and how?

### Pierre Marchand

10th January 2019 - Infomath

### .font50[Team-project Alpines, Inria and Laboratoire J.-L. Lions, Sorbonne Université]

???
You found the slide notes ?
![full](https://media.giphy.com/media/l396GDVdFycbmiZDG/giphy.gif)
- Give the link of the website so that they can access to the sources


---

# What is git?

.right-column-third[.right[<i class="fab fa-git fa-5x"></i>]]

*Decentralized version control system* for [source code](https://en.wikipedia.org/wiki/Source_code)

???
version control system: source code is usually **plain text** -> `.py`, `.tex`, `.marshmallow`...

--

- a clean history
- changes between versions
- easy collaborative development
- reset to a previous versions
- online backup

--

It is a Free and Open-Source Software (FOSS) under [GNU General Public License version 2.0](https://git-scm.com/about/free-and-open-source)

---

# Why use it?

Several use cases:
- <i class="fas fa-user-alt fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-laptop fa-2x" style="color:#4C4B4C"></i>: **versioning**,

???
git scales ! from your article/proto code to Linux kernel and Windows
--

- <i class="fas fa-user-alt fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-laptop fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-at fa-2x" style="color:#4C4B4C"></i>: **versioning** and **backup**,

--

- <i class="fas fa-user-alt fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i><i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i><i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i> with <i class="fas fa-at fa-2x" style="color:#4C4B4C"></i>: **versioning**, **backup** and **synchronization**,

--

- <i class="fas fa-users fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i><i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i><i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i> with <i class="fas fa-at fa-2x" style="color:#4C4B4C"></i>: **versioning**, **backup**, **synchronization** and **collaborative work**.


---

# Do

It is one of the most basic tool in programming, so it is **everywhere**

--

- Atom, text editor

![full](https://blog.atom.io/img/posts/github-package-git.png)
.footnote[[sources: blog.atom.io](https://blog.atom.io/2017/05/16/git-and-github-integration-comes-to-atom.html)]
---

# Do not

It is one of the most basic tool in programming, so it is **everywhere**

- VS Code, text editor

![full](https://code.visualstudio.com/assets/docs/editor/versioncontrol/overview.png)
.footnote[[sources: code.visualstudio.com](https://code.visualstudio.com/docs/editor/versioncontrol)]

---

# Do not be

It is one of the most basic tool in programming, so it is **everywhere**

- Tortoisegit, GUI on Windows

![full](https://tortoisegit.org/docs/tortoisegit/images/Overlays.png)
.footnote[[sources: tortoisegit.org](https://tortoisegit.org/about/screenshots/)]

---

# Do not be afraid

It is one of the most basic tool in programming, so it is **everywhere**

- GitKraken, GUI cross-plateform

![full](https://www.gitkraken.com/img/misc/gk-merge-edit.gif)
.footnote[[sources: gitkraken.com](https://www.gitkraken.com/git-client)]

---

# Do not be afraid!

It is one of the most basic tool in programming, so it is **everywhere**

- and so on, see https://git-scm.com/downloads/guis/

.center[*But knowing how to use it with command lines is **important***]

---

# How does it work?

## Centralized vs Distributed ~~(Subversion vs git)~~

.left-column-half[![full](https://git-scm.com/book/en/v2/images/centralized.png)]
.right-column-half[![full](https://git-scm.com/book/en/v2/images/distributed.png)]


.footnote[[sources: git-scm.com](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)]

---

# How does it work?

## Git is *distributed*

So you can add a remote repository with <i class="fab fa-github-alt fa-2x" style="color:#4C4B4C"></i> [GitHub](https://github.com), <i class="fab fa-gitlab fa-2x" style="color:#4C4B4C"></i> [Gitlab](https://gitlab.com), <i class="fab fa-bitbucket fa-2x" style="color:#4C4B4C"></i> [Bitbucket](https://bitbucket.org/product) and [others](https://en.wikipedia.org/wiki/Comparison_of_source-code-hosting_facilities)

--

## Bonus: Web interfaces

![full](https://help.github.com/assets/images/help/graphs/repo_network_graph.png)
.footnote[[sources: github.com](https://help.github.com/articles/viewing-a-repository-s-network/)]

???
Let us say that we have an installed git repository, local and remote.

---

# Local repository

## Staging area

.right-column-half[![full](https://git-scm.com/images/about/index1@2x.png)]

- Untracked files needs to be *added* to be seen by git to be staged
- A modified file needs to be *added* to the repository to be staged
- Added files need to be *committed* to the repository

### Why a staging area?

- logical separation of changes to commit
- reviewing changes before commit

See this [discussion](https://stackoverflow.com/questions/49228209/whats-the-use-of-the-staging-area-in-git) or this [one](https://stackoverflow.com/questions/4878358/why-would-i-want-stage-before-committing-in-git). Don't care? `git commit -a`
.footnote[[sources: git-scm.com](https://git-scm.com/about/staging-area)]

---

# States of a file

<i class="fas fa-exclamation-triangle fa-2x"></i> `git status` (gives also clues on what to do)


![full](https://www.git-scm.com/book/en/v2/images/lifecycle.png)

.footnote[[sources: git-scm.com](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)]

---

# Working with a remote

## Working with a remote 

- `git clone <url>`: download the remote repository
- `git pull`: download changes from remote
- `git push`: upload changes to remote

## Navigating between commits

- `git log`: view commit history
- `git checkout <commit-hash>`: take a look to old commit
- `git diff <commit-hash>`: show diff between present commit and `<commit-hash>`

---

# Conclusion

## To go further

A few more advanced concepts

- [Stashing](https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning) 
- [Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
- [Branching](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)

Collaborative work development is related to dealing with branch usually, a few examples of workflow [here](https://www.atlassian.com/git/tutorials/comparing-workflows) or [here](https://guides.github.com/introduction/flow/)

## To start

- To start on your computer: you need to setup git see [this](https://www.git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup), but to sum up

```bash
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

- To create a repository: I suggest you first create the remote repository

---

# Conclusion

## References

- https://git-scm.com where you can find [Pro Git](https://git-scm.com/book/en/v2) (available in several langages)
- an interesting discussion on Quora: [What is git and why should I use it?](https://www.quora.com/What-is-git-and-why-should-I-use-it)
- a [talk](https://www.youtube.com/watch?v=ZDR433b0HJY) of Scott Chacon

## git is everywhere

- deployment of static webpage: Hugo+Academic+Netlify
- automatic testing
- overleaf