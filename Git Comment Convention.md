# Git Comment Convention


## Comment structure
1.	First line is a subject line. It should have size about 50 characters, maximum limit is 80. Subject line is capitalized and hasn't period at the end;
2.	A blank line separates subject from body;
3.	Detailed description of the change in the body, breaking paragraphs where needed. The body should explain what  you did and why vs. how. The body also starts with a capitalized letter. Bullet points are made with an asterisk (*);
4.	In case if a bug tracking system is used, bug Id's line is placed at the very end after a blank line.


## Subject line tags
- [FEATURE]: A new feature (also small additions). Most likely it will be an added feature, but it could also be removed;
- [BUGFIX]: A fix for a bug;
- [STYLE]: Changes in layout, page style and css files;
- [CLEANUP]: Code formatting, improvements in code style and readability;
- [DOCS]: Changes to documentation;
- [TEST]: Adding, changing, refactoring tests - no production code change;
- [OTHER]: Anything not covered by the above categories.


## Flags have to be added under certain circumstances
- (!!!) : Breaking change. Significant changes in software architecture or logic, that affect existing features and extentions or change user experience;
- (DB): Changes that require database structure or data to be updated;
- (WIP): Work in progress. This flag will be removed, once the final version of a change is available. Changes marked WIP are never merged.


## Tags usage examples
1. [STYLE] Change size of tag h1
2. [CLEANUP] Few code formatting
3. [BUGFIX] Fix bugs 101 and 110
4. [FEATURE] Add new universal system class object
5. (!!!)[FEATURE] Added new class ChartItem
6. (!!!)(DB)[FEATURE] Add new column ApplicationUserID


## Commit Message Example
(!!!)(DB)[FEATURE] Rewrite stored procedure

Additional information about commit changes


## Source
- [WIKI OpenStack Information in commit messages](https://wiki.openstack.org/wiki/GitCommitMessages#Information_in_commit_messages)
- [Karma-Runner Git Commit Msg](http://karma-runner.github.io/0.8/dev/git-commit-msg.html)
- [Wiki.Typo3.Org CommitMessage Format](http://wiki.typo3.org/CommitMessage_Format_(Git))
- [How to Write a Git Commit Message ](https://webcache.googleusercontent.com/search?q=cache:PM7POmjONvgJ:https://chris.beams.io/posts/git-commit/+&cd=1&hl=sl&ct=clnk&gl=si&client=firefox-b-d)


## Useful links
 - [Better Code Reviews with GIT](https://www.red-gate.com/simple-talk/dotnet/software-delivery/better-code-reviews-with-git/)
 - [Part 1: Pre-Review Comments](https://www.red-gate.com/simple-talk/dotnet/.net-framework/the-zen-of-code-reviews-pre-review-comments/)
 - [Part 2: Best Practices](https://www.red-gate.com/simple-talk/dotnet/.net-framework/the-zen-of-code-reviews-best-practices/)
 - [Part 3: The Reviewer’s Tale](https://www.red-gate.com/simple-talk/dotnet/.net-framework/the-zen-of-code-reviews-the-reviewer's-tale/)
 - [Part 4: Review as if You Own the Code](https://www.red-gate.com/simple-talk/dotnet/.net-framework/the-zen-of-code-reviews-review-as-if-you-own-the-code/)
