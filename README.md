# P system models of COVID-19 propagation

## Context

Membrane systems or [P
systems](https://en.wikipedia.org/wiki/P_system) are a hierarchical
abstract computing device based on multiset rewriting.  They were
first introduced by [Gheorghe
Păun](https://en.wikipedia.org/wiki/Gheorghe_P%C4%83un) in 1999 and
have since been modified and extended to yield a very rich ecosystem
of variants.

We are currently holding an [online
course](https://ecampus.paris-saclay.fr/course/view.php?id=21726) on P
systems. We decided to build P systems models of
[COVID-19](https://en.wikipedia.org/wiki/Coronavirus_disease_2019)
propagation.

## Repository structure

This repository contains one directory for each of the teams of
students.  Every directory contains the file `members.md` giving the
list of the members of the corresponding team, and will contain
various other resources contributed by the team: textual
documentation,
[P-Lingua](http://www.p-lingua.org/wiki/index.php/Main_Page) models,
additional pre- or post-processing code, visualisation, etc.

## How to contribute

### Where to start

**Step 1:** Designate an administrative head of each team.

**Step 2:** The team head
[forks](https://help.github.com/en/github/getting-started-with-github/fork-a-repo)
the *central repository* (this one) to make the *team repository*.
Every member of the team forks the team repository to make their own
*personal repository*.

**Step 3:** The team head adds the names of the members to the file
`members.md` in the corresponding directory.

**Step 4:** Contribute!

### Contribution workflow

Every member of the team commits changes locally and pushes them to
their personal repository.  Whenever they finish a logically
independent subsection of their work, they submit a [pull
request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests)
to the team repository, which is merged by the team head.  The team
head submits a pull request to the central repository whenever the
team hits any minor milestone: model draft finished, P-Lingua model
added, post-processing finished, etc.

You don't have to send pull requests after every single commit.  Team
members should send a pull request to the team repository after about
a day of work.  Team head should sent a pull request to the central
repository approximately every 2–3 days.

The teachers will take care of reviewing and merging team pull
requests into the central repository.  You will not have direct access
to the central repository, since any contribution can be done via a
pull request.

Every team will only modify the files in their directory.  You can of
course look at what the others are doing.

Within the team, it is best to avoid multiple people modifying the
same parts of the same file at once.  Such concurrent modifications
usually lead to merge conflicts which may be tricky to resolve.
Multiple people may work on the same files at the same time
seamlessly, provided that they modify *different* parts of those
files.

Commit often and keep your commits small and localised.  This will
reduce the risk of merge conflicts and will allow you to have a
finer-grained history.

### Git workflow

#### Checking out

Start by checking out your personal repository using a command similar
to this one:

```
git checkout git@github.com:[your-username]/covid-p-models.git
```

You will have to
[generate](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
and
[upload](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
SSH keys in order to use such a link.  Note that you can just open the
`~/.ssh/id_rsa.pub` with a text editor and copy and paste the public
key by hand, without relying on `xclip`.

#### Committing

A commit corresponds to a logical block of your work which you can
describe with a short sentence.  Commit often and keep the
descriptions clear.  This will help you and your teammates understand
and debug your work.  The simplest way to commit all your local
changes is the following command:

```
git commit -a -m "Helpful commit message."
```

#### Pushing and pull requests

Pushing is the operation by which the commits you added to a branch
locally get into the corresponding branch in your personal repository.
When you push to a branch, you can [create a pull
request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)
from that branch to the team repository.

The team head may either create a fork of their team's repository and
work as a regular member, using the team's repository to centralise
everyone's pull requests, or they may commit directly to their team's
repository.

The whole team should review the pull requests of the members to make
sure everyone stays in sync with the team's current objectives.

Whenever appropriate, the team head submits a pull request to the
central repository.  The teachers will review and merge the pull
request, which may also be reviewed by the members of the team.

#### GUIs and porcelains

You can of course use one of the very [many graphical user
interfaces](https://git-scm.com/downloads/guis) to Git and/or GitHub.

If you like GNU Emacs, you may consider using
[Magit](https://magit.vc/).

### Resources

1. [To Git or Not to
   Git](https://www.ibisc.univ-evry.fr/~sivanov/content/courses/togit/togit.pdf)
   — An overly simplified explanation of some of the concepts behind
   Git.
2. [The Git Book](https://git-scm.com/book/en/v2) — If you don't have
   much experience with Git, I highly recommend that you glance
   through the first 6 chapters of this document.  The basic concepts
   of Git are very simple, even if somewhat numerous, but a surprising
   number of "simplified" explanations get them wrong.
3. [Hello World](https://guides.github.com/activities/hello-world/) —
   A hugely simplified explanation of how to work with GitHub.
4. [Generating a new SSH key and adding it to the
   ssh-agent](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
   — Note that you don't actually have to add the key to ssh-agent,
   but it's probably a good idea.
5. [Adding a new SSH key to your GitHub
   account](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
   — Note that you can just open `~/.ssh/id_rsa.pub` with a text
   editor and copy and paste the public key by hand, without relying
   on `xclip`.
6. [About Pull
   Requests](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests)
   — A detailed presentation of different operations related to pull
   requests: creating, reviewing, merging, etc.
   
One important thing to remember: Git is **not** GitHub.  GitHub is a
Web resource based on Git and extending it with tons of new
functionality.  Git on the other hand is a separate, stand-alone tool,
which doesn't even need to be connected to a platform like GitHub.
