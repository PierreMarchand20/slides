class: title-slide

# Git: Why and how?

### Pierre Marchand

10th January 2019 - Infomath

### .font50[Team-project Alpine, Inria Laboratoire J.-L. Lions, Sorbonne Université]

---

# What is git?

.right-column-third[.right[<i class="fab fa-git fa-5x"></i>]]

It is a *decentralized version control system*, it manages changes to [source code](https://en.wikipedia.org/wiki/Source_code), it allows

???
version control system: source code is usually **plain text** -> `.py`, `.tex`, `.marshmallow`...

--

- having a clean history,
- seeing changes,
- easier collaborative development,
- recovering previous versions,
- having a backup.

--

It is a Free and Open-Source Software (FOSS) under [GNU General Public License version 2.0](https://git-scm.com/about/free-and-open-source)

---

# Why use it?

Several use cases:
- <i class="fas fa-user-alt fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-laptop fa-2x" style="color:#4C4B4C"></i> without internet: **versioning**,

--

- <i class="fas fa-user-alt fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-laptop fa-2x" style="color:#4C4B4C"></i> with internet: **versioning** and **backup**,

--

- <i class="fas fa-user-alt fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i><i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i><i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i> with internet: **versioning**, **backup** and **synchronization**,

--

- <i class="fas fa-users fa-2x" style="color:#4C4B4C"></i> with <i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i><i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i><i class="fas fa-laptop fa-sm" style="color:#4C4B4C"></i> with internet: **versioning**, **backup**, **synchronization** and **collaborative work**.


---

# Don't be afraid!

It is one of the most basic tool in programming, so it is **everywhere**

- Atom, text editor

![full](https://blog.atom.io/img/posts/github-package-git.png)
.footnote[[sources](https://blog.atom.io/2017/05/16/git-and-github-integration-comes-to-atom.html)]
---

# Don't be afraid!

It is one of the most basic tool in programming, so it is **everywhere**

- VS Code, text editor

![full](https://code.visualstudio.com/assets/docs/editor/versioncontrol/overview.png)
.footnote[[sources](https://code.visualstudio.com/docs/editor/versioncontrol)]

---

# Don't be afraid!

It is one of the most basic tool in programming, so it is **everywhere**

- Tortoisegit, GUI on Windows

![full](https://tortoisegit.org/docs/tortoisegit/images/Overlays.png)
.footnote[[sources: tortoisegit.org](https://tortoisegit.org/about/screenshots/)]

---

# Don't be afraid!

It is one of the most basic tool in programming, so it is **everywhere**

- GitKraken, GUI cross-plateform

![full](https://www.gitkraken.com/img/misc/gk-merge-edit.gif)
.footnote[[sources: gitkraken.com](https://www.gitkraken.com/git-client)]

---

# Don't be afraid!

It is one of the most basic tool in programming, so it is **everywhere**

- and so on, https://git-scm.com/downloads/guis/

.center[But knowing how to use it with command lines is **important**]

---

# How does it works?

## Centralized vs Distributed

.left-column-half[![full](https://git-scm.com/book/en/v2/images/centralized.png)]
.right-column-half[![full](https://git-scm.com/book/en/v2/images/distributed.png)]


.footnote[[sources: git-scm.com](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)]

---

# How does it works?

## Git is *distributed*

So you can add a remote repository with <i class="fab fa-github-alt fa-2x" style="color:#4C4B4C"></i> [GitHub](https://github.com), <i class="fab fa-gitlab fa-2x" style="color:#4C4B4C"></i> [Gitlab](https://gitlab.com), <i class="fab fa-bitbucket fa-2x" style="color:#4C4B4C"></i> [Bitbucket](https://bitbucket.org/product) and [others](https://en.wikipedia.org/wiki/Comparison_of_source-code-hosting_facilities)

--

## Bonus: Web interfaces

![full](https://help.github.com/assets/images/help/graphs/repo_network_graph.png)
.footnote[[sources: github.com](https://help.github.com/articles/viewing-a-repository-s-network/)]

---

# How does it works?

## Staging area

.right-column-half[![full](https://git-scm.com/images/about/index1@2x.png)]
.footnote[[sources: git-scm.com](https://git-scm.com/about/staging-area)]