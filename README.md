# GIT commit message guidelines

# Introduction

These guidelines are written minding that most teams at the moment use Squash Merge when merging pull requests into the main branch.

These are guidelines and not hard rules, its up to the individual team to find the right balance.

The idea of this guideline is to act as a quick glance reference when merging a Pull Request.

If possible we would like this page to act as a more detailed page with descriptions, but have get infographic made if possible, inspired by 
 [this example](https://cdn.hashnode.com/res/hashnode/image/upload/v1577374984862/Q7QGKgtEB.png?auto=compress) that will be the quick reference guide you can use when you understand this guide.

This guide is inspired these sites

* [Chris Beams - Git commits](https://chris.beams.io/posts/git-commit/)
* [Freecodecamp - Writing good code commits](https://www.freecodecamp.org/news/writing-good-commit-messages-a-practical-guide/)
* [Hashcode - Commit message convention questionnaire](https://hashnode.com/post/which-commit-message-convention-do-you-use-at-work-ck3e4jbdd00zyo4s1h7mc7e0g)
* [Midori-global - Maximum characters rule](https://www.midori-global.com/blog/2018/04/02/git-50-72-rule)
 
# The Guide

## Example

![image](https://user-images.githubusercontent.com/2316684/120662079-21b4e900-c489-11eb-905e-d0925120b778.png)


## Subject / Header

#### Types
To make it easier to look in Git log and search across the codebase we make 
the following types that are prefixed in the subject, our example is copied from [this](https://cdn.hashnode.com/res/hashnode/image/upload/v1577374984862/Q7QGKgtEB.png?auto=compress) they are on purpose shortend to not "steal" from the maximum of 50 characters.

Also only 1 type should be used, if the code contains both a feature and a bug fix, those should be 2 different commits.

* **feat**
	- A new feature including tests
* **fix**
	- A bug fix, this can also add test to cover the bug
* **docs**
	- Changes in documentation
* **style**
	- Style changes, formatting
* **refac**
	- Refactoring

* **perf**
	- Performance improvements
* **test**
	- Add missing tests
* **build**
	- Changes to the build process

#### Writing style
Git itself uses the imperative whenever it creates a commit on your behalf.

To test if your subject is written imperative use the following sentence

If applied, this commit will *your subject line here*

For example:

    If applied, this commit will Refactor subsystem X for readability
    If applied, this commit will Update getting started documentation
    If applied, this commit will Remove deprecated methods
    If applied, this commit will Release version 1.0.0
    If applied, this commit will Merge pull request #123 from user/branch

Notice how this doesn’t work for the other non-imperative forms:

    If applied, this commit will fixed bug with Y
    If applied, this commit will changing behavior of X
    If applied, this commit will more fixes for broken stuff
    If applied, this commit will sweet new API methods

#### Pull request number
When merging a PR, GitHub will automatically write e.g. (#314), this should be persisted in the final commit message to make it easy to find the PR.

#### Maximum length of subject: 50 <= characters.
When writing the subject, the total length including type and PR information should be 50 chars or below, this is to ensure easy readability in all Git Clients, see [this](https://www.midori-global.com/blog/2018/04/02/git-50-72-rule) for reference  following format.
GitHub will truncate any subject line longer than 72 characters with an ellipsis.

#### Do not end the subject line with a period

Trailing punctuation is unnecessary in subject lines. Besides, space is precious when you’re trying to keep them to 50 chars or less.

#### Capitalize the subject line

This is as simple as it sounds. Begin all subject lines with a capital letter.

For example:

    Accelerate to 88 miles per hour

Instead of:

    accelerate to 88 miles per hour

#### Subject template
Type: Description (#123)

##### Example subject
* feat: Validate Id of TimeSeries (#123)
* test: Add Id validation null check (#124)
* perf: Make Id null validation linear (#125)

## Body

#### Wrap the body at 72 characters
Git never wraps text automatically. When you write the body of a commit message, you must mind its right margin, and wrap text manually.

#### Use the body to explain what and why vs. how
This [commit from Bitcoin Core](https://github.com/bitcoin/bitcoin/commit/eb0b56b19017ab5c16c745e6da39c53126924ed6) is a great example of explaining what changed and why 

#### Include link to issue if any
GitHub have support for the following synonyms
[GitHub - Blog](https://github.blog/2011-04-09-issues-2-0-the-next-generation/)

* fixes #xxx
* fixed #xxx
* fix #xxx
* closes #xxx
* close #xxx
* closed #xxx

#### Body template and example


    Id input validation of TimeSeries was added
    
    A given TimeSeries should fail input validation
    if Id is not supplied when receiving the message
    
    closes #123
   
