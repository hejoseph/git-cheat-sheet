# Git Cheat Sheet

## Git Commit Guidelines

We have very precise rules over how our git commit messages can be formatted.  This leads to **more
readable messages** that are easy to follow when looking through the **project history**.  But also,
we use the git commit messages to **generate the AngularJS change log**.

The commit message formatting can be added using a typical git workflow or through the use of a CLI
wizard ([Commitizen](https://github.com/commitizen/cz-cli)). To use the wizard, run `yarn run commit`
in your terminal after staging your changes in git.

### Commit Message Format
Each commit message consists of a **header**, a **body** and a **footer**.  The header has a special
format that includes a **type**, a **scope** and a **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The **header** is mandatory and the **scope** of the header is optional.

Any line of the commit message cannot be longer 100 characters! This allows the message to be easier
to read on GitHub as well as in various git tools.

### Revert
If the commit reverts a previous commit, it should begin with `revert: `, followed by the header of the reverted commit.
In the body it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit being reverted.

### Type
Must be one of the following:

* **feat**: A new feature
* **fix**: A bug fix
* **docs**: Documentation only changes
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing
  semi-colons, etc)
* **refactor**: A code change that neither fixes a bug nor adds a feature
* **perf**: A code change that improves performance
* **test**: Adding missing or correcting existing tests
* **chore**: Changes to the build process or auxiliary tools and libraries such as documentation
  generation

### Scope
The scope could be anything specifying place of the commit change. For example `$location`,
`$browser`, `$compile`, `$rootScope`, `ngHref`, `ngClick`, `ngView`, etc...

You can use `*` when the change affects more than a single scope.

### Subject
The subject contains succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize first letter
* no dot (.) at the end

### Body
Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Footer
The footer should contain any information about **Breaking Changes** and is also the place to
[reference GitHub issues that this commit closes][closing-issues].

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines.
The rest of the commit message is then used for this.

A detailed explanation can be found in this [document][commit-message-format].

git status: état du repository local
git diff: différence entre les fichiers courants et le dernier commit
git init : création d’un nouveau repository (projet au sens git)
git clone username@host:/path/to/repositorygit clone username@host:/path/to/repository : Récupérer un repository
git checkout –b mabranche : création d’une branche
git add <filename> / * : ajouter des documents à l’index de notre repository local
git commit -m "Commit message …  : ajouter des fichiers l’historique de notre repository local
git push origin master : pousser ses changements sur le repository central
git pull : récupérer le repository distant (écrase ce que l’on en local)
git remote add origin <server> : pour se connecter à repository (si par exemple vous n’avez pas cloner votre répertoire courant)
git log : historique de commits du repository local

Votre répertoire local de travail va être « organisé » en trois parties par GIT :
La première : le « working directory » qui contient les contenus actuels de vos fichiers/répertoires. 
Le second : l’index qui se comporte comme une « staging area » (zone de transit).
Le troisième : la « head » qui pointe vers votre dernier commit. 


.gitignore : Spécifie les fichiers qui ne doivent pas être traqués dans le contrôleur de code source
Chaque ligne du .gitignore spécifie un pattern

La pull request est indispensable !

Elle permet de faire valider les modifications avant que celles-ci ne soient mises à disposition de tous

C’est une revue de code asynchrone permettant de facilement tracer et prendre en compte les remarques de chacun

Avec VSTS nous pouvons lier plusieurs règles permettant de refuser les modifications lorsque la Build est KO, que les remarques ne sont pas prises en comptes, que le nombre d’approbateurs n’est pas suffisant ..
