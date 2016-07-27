# Contributing

## General Workflow

1. Fork from master branch in Github to your account:

2. Clone down from your Github
  -> git clone http://github.com/#yourname#/projectOne.git

3. cd into folder
  -> cd projectOne

4. Add the upstream master

  -> git remote add upstream https://github.com/untitledProject/projectOne.git

5. Create a new feature branch from master, If it's a new feature, name the branch "feat#". If it's a bug fix, name the branch "bug#". # should be the associated issue number on the GitHub repo.

  -> git checkout -b feat3

  OR

  -> git checkout -b bug11

6. Make changes to your feature branch.

  -> git add -p

7. Commit changes

  -> git commit -m "#present tense commit message which should include info about what was changed e.g. which files were changed and what was added. More commits with fewer changes are easier to track.#"

8. Pull down the changes from the the upstream master

  -> git pull upstream master

9. Fix merge conflicts

10. TEST YOUR CODE

11. Push up to your Github feature branch

  -> git push #branch#

12. Create a well documented pull request from your feature branch on Github


## Detailed Workflow

### Cut a namespaced feature branch from master

Your branch should follow this naming convention:
  - bug#
  - feat#
  - test#
  - doc#
  - refactor#

  Where # associates directly with the issue number in the GitHub repo

These commands will help you do this:

# Creates your branch and brings you there

git checkout -b `your-branch-name`

### Make commits to your feature branch.

Prefix each commit like so
  - (feat#) Added a new feature
  - (fix#) Fixed inconsistent tests [Fixes #0]
  - (refactor#) ...
  - (cleanup#) ...
  - (test#) ...
  - (doc#) ...

Make changes and commits on your branch, and make sure that you
only make changes that are relevant to this branch. If you find
yourself making unrelated changes, make a new branch for those
changes.

#### Commit Message Guidelines

- Commit messages should be written in the present tense; e.g. "Fixes continuous 
  integration script".
- Your commit message should be a brief summary of what the commit changes. 
- If you want to explain the commit in more depth, following the first line should
  be a blank line and then a more detailed description of the commit. This can be
  as detailed as you want.


### Make a pull request

Make a clear pull request from your fork and branch to the upstream master
branch, detailing exactly what changes you made and what feature this
should add. The clearer your pull request is the faster you can get
your changes incorporated into this repo.

At least one other person MUST give your changes a code review, and once
they are satisfied they will merge your changes into upstream. Alternatively,
they may have some requested changes. You should make more commits to your
branch to fix these, then follow this process again from rebasing onwards.

Note: A pull request will be immediately rejected if there are any conflicts!

Once you get back here, make a comment requesting further review and
someone will look at your code again. If they like it, it will get merged,
else, just repeat again.

Thanks for contributing!

### Guidelines

1. Uphold the current code standard:
    - Keep your code [DRY][].
    - Apply the [boy scout rule][].
    - Follow [STYLE-GUIDE.md](STYLE-GUIDE.md)
1. Run the [tests][] before submitting a pull request.
1. Tests are very, very important. Submit tests if your pull request contains
   new, testable behavior.
1. Your pull request is comprised of a single ([squashed][]) commit.

## Checklist:

This is just to help you organize your process

- [ ] Did I cut my work branch off of master (don't cut new branches from existing feature brances)?
- [ ] Did I follow the correct naming convention for my branch?
- [ ] Is my branch focused on a single main change?
 - [ ] Do all of my changes directly relate to this change?
- [ ] Did I pull the upstream master branch after I finished all my
  work?
- [ ] Did I write a clear pull request message detailing what changes I made?
- [ ] Did I get a code review?
 - [ ] Did I make any requested changes from that code review?

If you follow all of these guidelines and make good changes, you should have
no problem getting your changes merged in.

<!-- Links -->
[pull request]: https://help.github.com/articles/using-pull-requests/
[DRY]: http://en.wikipedia.org/wiki/Don%27t_repeat_yourself
[boy scout rule]: http://programmer.97things.oreilly.com/wiki/index.php/The_Boy_Scout_Rule
[squashed]: http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html
<!-- A link to your directory of tests on github -->
[tests]: tests/
