# P systems models of COVID-19 propagation

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

This repository contains one directory for each of the teams of the
students.  Every directory contains the file `students.md` giving the
list of the students of the corresponding teams, and will contain
various other resources contributed by the students: textual
documentation,
[P-Lingua](http://www.p-lingua.org/wiki/index.php/Main_Page) models,
additional pre- or post-processing code, visualisation, etc.

## How to contribute

### Where to start

**Step 1:** Designate an administrative head of each team.  The head
will send up the list of GitHub accounts of each member to me by
E-mail.  I will invite each member as a collaborator to this
repository.  This will give you almost full access rights to the
repository, so some care will be needed to not break other people's
work.  (It's easy to not break stuff, really.)

**Step 2:** Add the names of the students to the file `students.md` to
the directory corresponding to your team.  This will help you remember
what your teams are.

**Step 3:** Every member of the team checks out the repository.

**Step 4:** Contribute!

### Contribution workflow

Everyone will commit to `master`.  You can create your local branches
and push them here for the members of your team to share, but don't
forget to merge such branches into `master` often.

Every team will only modify the files on the directory of this team.
You can of course look at what the others are doing.

Within the team, it is best to avoid multiple people modifying the
same parts of the same file at once.  Such concurrent modifications
usually lead to merge conflicts which maybe tricky to resolve.
Multiple people may work on the same files at the same time
seamlessly, provided that they modify *different* parts of those
files.

Commit often and keep your commits small and localised.  This will
reduce the risk of merge conflicts and will allow you to have a
finer-grained history.  Push often so that your teammates can see what
your progress is.

### Git workflow

#### Checking out

Start by checking out this repository using a command similar to this
one:

```
git checkout git@github.com:scolobb/covid-p-models.git
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
descriptions clear.  This will help you and your teammates debug your
models.  The simplest way to commit all of your changes is the
following command:

```
git commit -a -m "Helpful commit message."
```

#### Pushing (sharing your contributions)

Pushing is the operation by which the commits you contributed to a
branch (e.g., `master`) get into the corresponding branch of this
online repository.  To avoid overriding other people's changes (Git
will normally not allow you to do that easily), I highly recommend
doing a pull **before** every push, for example:

```
git pull origin master
git push origin master
```

The pull command brings the latest version of `master` from this
repository (`origin`) and *merges* it with whatever you committed to
`master` locally.  When you follow by a push, your changes will be
merged back into `master` in this repository.  This ensures that the
updates to `master` are always monotonic (fast-forward, in Git
parlance.)

#### GUIs and porcelains

You can of course use one of the very [many graphical user
interfaces](https://git-scm.com/downloads/guis) to Git and/or GitHub.

If you like GNU Emacs, you may consider using
[Magit](https://magit.vc/).

## Resources

1. [The Git Book](https://git-scm.com/book/en/v2) — If you don't have
   much experience with Git, I highly recommend that you glance
   through the first 5 chapters of this document.  The basic concepts
   of Git are very simple, even if somewhat numerous, but a surprising
   number of "simplified" explanations get them wrong.
2. [Hello World](https://guides.github.com/activities/hello-world/) —
   A hugely simplified explanation of how to work with GitHub.
3. [Generating a new SSH key and adding it to the
   ssh-agent](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
   — Note that you don't actually have to add the key to ssh-agent,
   but it's probably a good idea.
4. [Adding a new SSH key to your GitHub
   account](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
   — Note that you can just open the
`~/.ssh/id_rsa.pub` with a text editor and copy and paste the public
key by hand, without relying on `xclip`.
5. [To Git or Not to
   Git](https://www.ibisc.univ-evry.fr/~sivanov/content/courses/togit/togit.pdf)
   — An overly simplified explanation of some of the concepts behind
   Git.
   
One important thing to remember: Git is **not** GitHub.  GitHub is a
Web resource based on Git and extending it with tons of new
functionality.  Git on the other hand is a separate, stand-alone tool,
which doesn't even need to be connected to a platform like GitHub (of
which there are several).
