# Git Comment Convention


## Comment structure
1.	First line is a subject line. It should have size about 50 characters, maximum limit is 80. Subject line is capitalized and hasn't period at the end;
2.	A blank line separates subject from body;
3.	Detailed description of the change in the body, breaking paragraphs where needed.The body should explain what  you did and why vs. how. The body also starts with a capitalized letter. Bullet points are made with an asterisk (*);
4.	In case if a bug tracking system is used, bug Id is line is placed at the very end after a blank line.


## Subject line tags
- [FEATURE]: A new feature (also small additions). Most likely it will be an added feature, but it could also be removed;
- [BUGFIX]: A fix for a bug;
- [STYLE]: Changes in layout, page style and css files;
- [CLEANUP]: Code formatting, improves in code style and readability;
- [DOCS]: Changes to documentation;
- [TEST]: Adding, changing, refactoring tests - no production code change;
- [OTHER]: Anything not covered by the above categories.


## Flags have to be added under certain circumstances
- (!!!) : Breaking change. Significant changes in software architecture or logic, that affect existing features and extentions or change user experience;
- (DB): Changes that require database structure or data to be updated;
- (WIP): Work in progress. This flag will be removed, once the final version of a change is available. Changes marked WIP are never merged.


## Tags usage examples
1. [STYLE]  Измение размера тэга h1
2. [CLEANUP] Небольшое форматирование кода
3. [BUGFIX] При изменении модели ApplicationUser, не происходит автоматическое удаление базы и создание ее с новой структурой
4. [FEATURE] Добавлен универсальный объект для создания графиков
5. (!!!)[FEATURE] Исправлен класс ChartItem
6. (!!!)(DB)[FEATURE] Добавлен целочисленный ApplicationUserID

## Commit Message Example
(!!!)(DB)[FEATURE]Возврат к строковым идентификаторам в таблицах для авторизации пользователей

Поскольку не все встроенные в Microsoft Identity Owin 2.0 методы поддерживают
использование целочисленных значений в ID, тип данных для этого поля был сменен на string.


## Source
- [WIKI OpenStack Information in commit messages](https://wiki.openstack.org/wiki/GitCommitMessages#Information_in_commit_messages)
- [Karma-Runner Git Commit Msg](http://karma-runner.github.io/0.8/dev/git-commit-msg.html)
- [Wiki.Typo3.Org CommitMessage Format](http://wiki.typo3.org/CommitMessage_Format_(Git))
- [How to Write a Git Commit Message ](http://www.chrisbeams.com/posts/git-commit/)
