Git c'est simple!

Trois emplacements : 

R ( remote ) ------- : serveur remote ( github ) appelé aussi origin.
S ( staged ) ------- : emplacement fichiers locaux en attente de commit.
L ( local )  ------- : emplacement fichiers locaux en cour de modification travail.

git status -> Où je suis ? Qu'est ce qui se passe ? Qu'est ce que j'ai modifié ?

git add ./file_path -> ajouter un fichier de L dans S.

git reset HEAD ./file_path -> retirer un fichier de S vers L ( sans supprimer les modifications ).
git reset HEAD -> retirer tout les fichiers de S vers L ( sans supprimer les modifications ).
git checkout -- ./file_path -> effacer les modifications d'un fichier sur L ( attention dangereux ).
git checkout -- . -> effacer les modifications de tous les fichiers sur L ( attention dangeurex ).
git clean -df -> effacer toutes modifications + ajout de fichier sur L ( attention dangereux ).

git commit -m "Message" -> prend tout ce qui est sur S pour le mettre dans un commit en preparation pour être push sur R.
git commit --amend -> prend tout ce qui est sur S pour le mettre dans le dernier commit ( non pushé !! ) et permet le rename du dernier commit.
git commit --amend ( S vide ) -> permet le rename du commit seulement.

git checkout -b nom-branch -> créer une branch à partir de celle sur laquelle on se trouve.

git fetch (origin) -> récupère le status des modifications sur R.
git merge (origin) -> récupère les modifications et lance une procédure de merge ( pas bien ).
git pull -> fait un git fetch + git merge ( pas bien ).


"Message git" si message git fast-forward 