# Strateg code of conduct

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## Contents

- [Git](#git)
    - [Branching](#branching)
      - [Branch naming](#branch-naming)
    - [Rebasing](#rebasing)
    - [Committing](#committing)
      - [Separation of concerns](#separation-of-concerns)
      - [Messages](#messages)
        - ["Tagging" commits.](#tagging-commits)
    - [Pull Requests](#pull-requests)
      - [Preparation](#preparation)
      - [Review](#review)
    - [Merging](#merging)
- [JavaScript](#javascript)
- [(S)CSS](#scss)
- [PHP](#php)
  - [Code standard](#code-standard)
  - [Code style](#code-style)
  - [Statement structure](#statement-structure)
  - [Autoloading](#autoloading)
  - [HTTP-Messages](#http-messages)
  - [Documentation](#documentation)
- [SiteVision](#sitevision)
  - [Documentation](#documentation-1)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Git
`kebab-case` repository names with year suffix if it's a client project, e.g. `boilerplate` or `svebio-2016`

Every project should contain a **README** which details on how to setup the project to a buildable/runnable state.

#### Branching
Branching in Git is easy and cheap and you should therefore be encouraged to branch as often as you feel like, when working on a new feature, fixing a bug or just tinkering around.

While you are encouraged to branch whenever you feel like it, you MUST branch if you are working on a new feature or fixing an issue. The workflow for this should be as follow:
- Create a feature/issue branch of master
- Make the necessary changes
- Submit a pull request to have the changes reviewed by peers
- If approved, squash and merge the branch into master.

##### Branch naming
To keep some sort of consistency when working with branches, you should name your branch in the form of `initials/short_description`. Examples:

`git checkout -b ak/ft-add-stuff`
`git checkout -b ak/ft-add-other-stuff`
`git checkout -b ak/iss-fix-stuff`

This convention easily allows us to see who owns the branch and what changes reside within.

#### Rebasing
Since most repositories wont live in a vacuum there will usually be changes from other developers merged into the `master` branch. You should therefore get into the habbit of pulling from `origin/master` into your local `master` and rebasing your feature branch off of that to keep up-to-date:

`git checkout master`
`git pull`
`git checkout ft-something`
`git rebase master`

There's a chance this will cause conflicts in which case `rebase` will pause at the current step and allow you to resolve these issues before continuing by running `git rebase --continue`

#### Committing
Just as branches, commits as easy and cheap to make. Therefore you should get into the habit of making frequent commits along the way instead of one huge commit at the end. This will be easier to review and, _if needed_, rollback, instead of trying to split the huge commit into smaller ones.

##### Separation of concerns
Each commit should be self-contained, related and fully-functional.

By self-contained and related we mean that a single commit should contain **all** changes related to the commit in question and **only** those changes. A commit should therefore not contain code for adding a new button while also containing code for fixing a bug in a seperate file. These changes should be in two seperate commits.

By fully-functional we mean that every commit should be buildable/runnable, for example if anyone where to checkout any specific commit it should still be fully functional and runnable.

##### Messages
Commit messages should contain a short and descriptive first line followed by a completely blank line then any supporting descriptive paragraphs as desired.

Most of the time the single first line is all that is needed, but if you feel like you need more space for documentation or to describe the changes in detail you should feel free to use as much additional space as needed in the commit "body".

Single-line commit:
`[docs] Added documentation regarding thing.`
More descriptive multi-line commit:
```
[Fix] Lorem ipsum bug

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam bibendum sit amet metus in malesuada. Integer porttitor consequat nulla, eu lobortis lectus mattis eu. Fusce dignissim risus in porta tempor.
```

###### "Tagging" commits.
All commits should be "tagged" with any of the following "tags" to allow easier scanning of the commit log. A tag is always contained within square brackets.
`[fix]` Commit that fixes a bug/issue.
`[add]` Adding new functionality.
`[remove]` Removing old, unneeded functionality.
`[change]` Changes that change the flow/logic of existing functionality.
`[refactor]` Changes that optimize, clean-up or restructures existing functionality without actually changing the flow/logic.
`[docs]` Adding documentation.

#### Pull Requests
When you feel like a feature is complete and ready to be reviewed and/or tested by other developers you can signal this by creating a pull request.

##### Preparation
Before opening a pull request you should rebase your feature branch onto `master`. This will make merging the branch into master easier after the request has been approved.

##### Review
All developers on the project should actively participate in reviewing open pull requests. This keeps the whole team "in the loop" and helps them see what pieces are moving. This is also beneficial since more eyes on the code will potentially catch more bugs but also help enforce architectual consistency.

If you are working solo on a project and therefore don't have any other developers to tag for the review, you should instead tag someone who has the needed skillset to effectively review your changes.

You are encouraged to leave comments to ask questions regarding any code changes in the pull request.

#### Merging
When the review is complete and everyone has approved the pull request, the Pull Request should be merged into `master` and the feature branch will be closed.

All merges should either be squashed and merged, or cherry-picked.

## JavaScript
See [our styleguide](https://github.com/strt/javascript)

## (S)CSS
See [our styleguide](https://github.com/strt/css)

## PHP
### Code standard
- Use the full php tag instead of the shorthand php tag.
- Always use UTF-8 encoding
- Files should only define classes, functions, or produce content. But not both.
- Namespacing shall follow the PSR-standard.
- Classes should be written in a PascalCase manner.
- Constants should be capitalized and seperated with an underscore.
- Methods must be written in camelCase.
- Variables and properties must be written in camelCase.

### Code style
- A tab is four spaces.
- A soft line is 80 characters.
- A hard line is 120 characters.
- A newline after end of namespace and use statements.
- Curly bracets are opened on a new line when writing functions or methods.
- Visibility must be given on all properties and methods.
- True, false and null must be lowercase.
- Extend and implement must be on the same line as the class name.
- Properties and methods should not be prefixed with one or several underscores.
- Methods should not include a spacing between method name and parenthesis.
- If the method name and its arguments exeeds the soft or hard line, make a new line for each argument.
- Abstract and final keywords must be set before visibility.
- Static keyword must come after visibility.
- There should be no spacing before the first and after the last argument in a method or function.

### Statement structure
- Elseif should not contain spaces.
- A switch statement must not contain comments that refers to pieces of code further down.
- A foreach does not need to include both key and value variables.
- In unstable operations, always use a try/catch.

### Autoloading
- See www.php-fig.org

### HTTP-Messages
- When applicable use HTTP status as much as you can.
- See www.php-fig.org

### Documentation
- Should follow the standard set by PHPDoc.
- A block of documentation should always have a author, param and return tag if applicable.
- A block for methods and functions should always exist.
- Inline comments are not needed for all lines.

## SiteVision
- Only use the official [public API](https://help4.sitevision.se/webdav/files/apidocs/index.html) to avoid problems with future versions of SiteVision
- Code should be wrapped in a self-invoking function to avoid leaking varaibles to the Velocity parser
- Lint your code with eslint and use the [eslint-config-strt-sitevision](https://github.com/strt/eslint-config-strt-sitevision) config

### Documentation
- Documentation should follow the [JSDoc](http://usejsdoc.org/) specification
- Begin every script module with a block comment containing description, SiteVision version number and author
