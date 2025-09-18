<h1> Work-case 1 </h1>

(This task does Evhen Okhrimenko)

<h2>1. Опишіть для чого використовують git, які основні дії та команди в ньому виконують.  </h2>

 <b> Git is a version control system that helps developers </b>

 - track changes in files over time,

 - collaborate on code with a team,

 - restore previous versions if needed,
   
 - work on different features in parallel using branches.

<b> Main git commands </b>
---
- git init — initializes an empty repository.

- git clone <URL> — copies a remote repository.

- git status — checks the status of the working directory.

- git add <file> or git add . — adds changes to the index.

- git commit -m "message" — saves changes to the local history.

- git branch — lists local branches.

- git checkout <branch> or git switch <branch> — switches between branches.

- git merge <branch> — merges changes from another branch.

- git remote add origin <URL> — attaches a remote repository.

- git pull — downloads and merges changes from the remote repository.

- git push — pushes local changes to the remote.

- git revert <hash> — undoes a specific commit.

- git reset --soft|--mixed|--hard <hash> — resets the state to a specific commit with different levels of impact.

- git stash — temporarily saves unstaged changes.

- git stash apply — restores the most recent stash.

- git tag <name> — creates a tag.

- git show <tag> — shows changes associated with a tag.

---
(This task does Andrii Berdiaiev)

<h3> 2. Що таке "комміт", як він дозволяє відслідковувати зміни у файлах? </h3>
   
<p> A commit is a snapshot of the state of your project at a specific point in time, which stores information about all changes to files. A commit allows you to track changes because each entry contains a unique identifier, description, author information, and creation date, allowing you to review and revert to previous states of the project and see exactly how the code has changed over time.

 Each commit contains: 

- Author information
  
 - Date and time
   
 - A commit message describing the changes.
   
 Thanks to commits you can:

- Track who made changes and when
  
- Review the project’s history
  
- Go back to earlier versions if something breaks </p>

3\. Зареєструйте власний git-аккаунт (gitlab, github або інша платформа).  
Створіть новий публічний репозиторій, який будете використовувати для додавання всіх виконаних робіт з дисципліни «Операційні системи» (якщо працюєте в команді долучіть інших учасників команди до його редакторів).  
4\. Розмістіть свій перший колективний звіт про виконаний Work-case 1 (презентацію, текстовий файл, html-сторінку) у даному репозиторії. У git мають бути комміти від кожного учасника команди  
