## > command to clone distant repository on your local machine
- git clone https://github.com/othman-bouazzaoui/tips.git

## > show status (check before any action)
- git status 

## > if you modify a file you should add it to storage area
- git add folder/.. ou . ou /*

## > reverse to add
- git reset folder/.. ->

## > create a version 
- git commit -m "explain what I did"

5 : git branch

6 : git remote -v

7 : git push origin(remote server ex : gethub) main(repo local)  -> pour deployer vers serveur distant

8 : git pull origin main -> pour recuperer les modification depuis serveur distant le contraire de push

9 : git Init -> pour creer un repo vide

10: git remote add origin git@gihub.com:othman-bouazzaoui/(repo.git => nom de votre repository) il faut choisir le mode SSH pour deployer un projet depuis a 0 en local vers srv distant

11: git push -u origin main (-u pull & push)

12: git stash -> pour cacher les fichiers ... après une Add pour les stocker dans endroit

13: git stash list -> la liste des fichiers stocker

14: git stash pop -> pour les recupere ou cas ou je veux les supprimer ou les deployer 

15: git stash save "This is a msg" -> pour ajouter un msg avec les fichiers 

16: git stash apply -> pour les recupere ou cas ou je veux les supprimer ou les deployer et garder une copie dans le stash

17: git stash pop stash@{1} -> en cas plusieurs stash on donne l'id

18: git stash drop stash@{0} -> supprimer

19: git stash show stash@{0} -> s'il y a un dossier contient plusieurs fichiers ... on affiche le contenu

20: git stash clear -> pour supprimer tous les stash 

21: git restore --staged filename -> restaurer depuis staged

22: git clean -n -> pour afficher tous les fichiers que vous voulez supprimer

23: git clean -f -> pour supprimer les fichiers

24: git log -> pour consulter le log

25: git reset --hard -> puis git push origin main --force  -> si tu veux supprimer le head (dernier push)

26: git reset --hard hashCode-> puis git push origin main --force  -> si tu veux supprimer le head depuis ce hash

27: git .gitignore -> pour ingorer des extensions des fichier qu'on veux importer dans le projet
Contenu du fichier .gitignore :
*.log -> ingorer les extensions log
!valid.log -> sauf celui-là
dossier/ -> ingorer le dossier

28: git add -f xx.log -> ajouter un fichier malgré que ce n'est pas autorisé car l'extension .log

29: git tag V1.0 -> pour versionner votre projet

30: git push origin V1.0 -> 1er version
.... upload files ....

31: git tag -a V2.0 -m "2eme version" -> puis git push origin V2.0

32: git tag -l "V1.*" -> pour chercher en cas plusieurs resleases.

33: git tag -d V1.0 ->  pour supprimer tag qui se trouve dans mon PC local

34: git tag origin --delete V2.0 -> pour supprimer tag distant

35: git restore fileName -> cela te permet de récupèrer l'ancienne version d'un fichier


=> Alias 
  - git config --globale alias.st status -> resultat : git st
  - git config --globale alias.cm "commit -m" -> en double commandes
vous pouvez aussi tapper git config --globale --edit pour modifier tous les alias avec norepad :).
=> Configuration git

	1 - git config -l ou git help config -> pour voir tous les configuration de git

	2 - git config --globale user.email pour consulter les infos ou ajouter "oth.bouazzaoui@gmail.com" pour modifier
	
	3 - git config --globale user.name "othman-bouazzaoui"

	4 - git config -l --show-origin -> les sources des configurations

	5 - git config --globale unset user.name pour supprimer la valeur

	6 - git config --globale --edit -> pour modifier manuellement

	7 - ssh-keygen -t rsa -b 4096 -C "oth.bouazzaoui@gmail.com" -> pour generer un token public

	8 - ssh -T git@github.com -> pour se connecter avec server github à travers le token
=> branch

  1 - git branch NomBranch -> le nom du branch à créer
  2 - git checkout NomBranch -> pour accedre au nouveau branch
  3 - git checkout main -> pour revenir au branch main
  4 - git branch -d Nombranch -> pour supprimer (-D pour forcer la suppresion malgré une modification n'est pas commité)
  5 - git checkout -b Nombranch -> creer et acceder directement au branch
  6 - git branch -m NewNambranch -> pour renommer le branch
  7 - git merge nombranch -> pour merger avec le main afin d'envoyer tous ça après au serveur distant

- : check which files are committed :
     - git diff-tree --no-commit-id --name-only -r <-commit_id->