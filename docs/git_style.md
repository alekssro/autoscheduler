# How to write a good commit message

A commit message is a short description of the changes you've made to a file added before committing the changes.

Good commit messages are important not only for others who you may be collaborating on the project but also for you, to keep track of all your commits and knowing exactly what changes where maybe during that particular commit.

Even if you're working on a personal project, I'd recommend that you start getting in the habit of writing good commit messages.

This is the format that I use most of the time (this may change depending on your preference or organization your working for):

type: subject

body (optional)

footer (optional)

## 1. Type

    feat - a new feature
    fix - a bug fix
    docs - changes in documentation
    style - everything related to styling
    refactor - code changes that neither fixes a bug or adds a feature
    test - everything related to testing
    chore - updating build tasks, package manager configs, etc

## 2. Subject

This contains a short description of the changes made. It shouldn't be greater than 50 characters, should begin with a capital letter and written in the imperative eg. Add instead of Added or Adds.

## 3. Body

The body is used to explain what changes you made and why you made them. Not all commits are complex enough that they need a body, especially if you are working on a personal project alone, and as such writing a body is optional.

A blank line between the body and the subject is required and each line should have no more than 72 characters.

## 4. Footer

The footer is also optional and mainly used when you are using an issue tracker to reference the issue ID.

------------------

Example of a good commit message used by Udacity student Udacity Git Commit Message Style Guide

    feat: Summarize changes in around 50 characters or less

    More detailed explanatory text, if necessary. Wrap it to about 72
    characters or so. In some contexts, the first line is treated as the
    subject of the commit and the rest of the text as the body. The
    blank line separating the summary from the body is critical (unless
    you omit the body entirely); various tools like log, shortlog
    and rebase can get confused if you run the two together.

    Explain the problem that this commit is solving. Focus on why you
    are making this change as opposed to how (the code explains that).
    Are there side effects or other unintuitive consequences of this
    change? Here's the place to explain to them.

    Further paragraphs come after blank lines.

        Bullet points are okay, too

        Typically a hyphen or asterisk is used for the bullet, preceded
        by a single space, with blank lines in between, but conventions
        vary here

    If you use an issue tracker, put references to them at the bottom,
    like this:

    Resolves: #123
    See also: #456, #789



A more practical example:

``docs: Fix typo in README.md``

-----------------

Borrowed from https://dev.to/chrissiemhrk/git-commit-message-5e21