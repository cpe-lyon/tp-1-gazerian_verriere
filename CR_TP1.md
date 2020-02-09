Nicolas GAZERIAN, Nicolas VERRIERE
4ETI

**TP1 - Administration système : Compte Rendu**

**Exercice 1 :**

Installation du serveur sur machine virtuelle


**Exercice 2**

*Manuel*

Question 1)
La commande which renvoie le chemin complet jsuqu'au fichier ou à l'éxécutable entré en paramètre.

Question 2)
C'est la commande / qui permet de rechercher un terme dans le terminal.

Question 3)
La touche 'q' permet de quitter le manuel.

Question 4)
La section 6 du manuel contient des informations concernant les jeux disponibles dans le système.
On utilise la commande "man 6 intro" pour y avoir accès.

*Navigation dans l’arborescence des fichiers*

Question 1)
La commande cd ../../var/log permet de remonter 2 crans dans l'arborescence puis de "redescendre" jusqu'au fichier log de var.

Question 2)
Pour remonter d'un rang jusqu'au fichier père, on utilise la commande  cd . .

Question 3)
La commande Pour retourner dans le dossier personnel, on utilise la commande : *. ./. ./home*.

Question 4)
La commande cd /var permet de se rendre directement au dossier var.

Question 5)
Nous n'avons pas l'autorisation pour accéder au dossier root directement.

Question 6)
Le résultat est le même, nous ne pouvons pas nous rendre dans le dossier root. En effet, sudo ne peut s'appliquer qu'au programmes alros que cd est une commande.

Question 7)
L'utilisation des commandes mkdir (MaKe DIRectory pour la création de dossier), cd (Change Directory vers les dossiers créés ou leur père) et touch pour la création de fichier permettent la création de l'arborescence demandée.

Question 8)
Fichier1 ne se trouve pas dans le répertoire personnel, on ne peut donc pas le supprimer.
Dossier1, lui, n'est pas vide et ne peut donc pas non plus être supprimé même s'il appartient au dossier personnel. De plus, la commande rm ne peut supprimer que des fichiers et pas des dossiers.

Question 9)
Pour supprimer un dossier, il faut utiliser la commande rmdir (ReMove DIRectory).

Question 10)
Dossier2 n'est pas vide et ne peut donc pas être supprimé en l'état.

Question 11)
L'option -r permet une suppression récursive d'un dossier et de son contenu. 

*Commandes importantes*

Question 1)
C'est la commande date qui le permet.
La commande time sert à connaître le temps qu'une commande a mis pour s'éxécuter.

Question 2)
La commande ls affiche les fichiers et sous-dossiers contenus dans un répertoire dont le nom ne commencent pas par un point.
La commande la affiche tous les fichiers, même ceux cachés à la commande ls.

Question 3)
La commande whereis nous renvoie :
"ls: /bin/ls /usr/share/man/man1p/ls.1p.gz /usr/share/man/man1/ls.1.gz"
Ce sont les différents chemins de localisation de ls


Question 4) 
La commande *ll* permet d'afficher les fichiers du repertoire où l'on se situe, même les fichiers cachés. Cette commande n'a pas d'entrée de manuel car il s'agit d'un alias pour *ls -alF* comme le confirme la commande *alias*:.


Question 5)
La commande ls/bin permet de voir le contenu du dossier bin

Question 6) 
La commande ls . . renvoie le contenu du repertoire parent à celui dans lequel on se trouve.

Question 7)
C'est la commande pwd qui donne le chemin complet du dossier courant.

Question 8)
Cette manipulation crée un fichier nommé *plop* dans le repertoire courant, avec comme contenu : *yo*.

Question 9)
Cette manipulation crée un fichier nommé *plop* dans le repertoire courant, avec comme contenu : *yo* deux fois.
*>* écrase le contenu et ecris.
*>>* ajoute du contenu.

Question 10)
La commande *file* sert à donner le type d'un fichier. (ex : mp3, ASCII text,...)

Question 11)
Lorsque l'on modifie *toto* on remarque que l'on modifie aussi *titi*.
Si on supprime *toto* *titi* n'est pas supprimé et son contenu ne change pas.

Question 12)
La modification de *titi* ou *tutu* engendre la modification de l'autre. 
Quand on suuprime *titi* on recoit un message qui explique que *tutu* n'est plus lié à *titi*.

Question 13) *CTRL + S* arrête le défilement, et *CTRL + Q* reprend le défilement.

Question 14) 
Affichage des 5 premières lignes de *syslog*: *head -5 /var/log/syslog*

Affichage des 15 dernières lignes de *syslog* : *tail -15 /var/log/syslog*

Affichage des lignes entre 10 et 20 de *syslog* : *head -n 10 /var/log/syslog | tail -n 20*


Question 15)
dmesg | less permet d'afficher la mémoire tampon du message du noyau.

Question 16)
/etc/passwd contien les mots de passes associés aux utilisateurs du systèmes.
Pour afficher la page du manuel associé on fait : *man passwd*
*Passwd* est aussi une commande permettant à l'utilisateur de changer son mot de passe.

Question 17) 
Affichage de la colonne triée par ordre alphabétique inverse : *sort +0 -r /etc/passwd*

Question 18)
Commande pour connaitre le nombre d'utilisateurs sur cette machine : *wc -l /etc/passwd*

Question 19) 
Commande pour savoir combien de pages de manuel comportent le mot-clé conversion dans leur description: *man -k conversion*
Résultat : 4 pages de manuel contiennent ce mot clé.


Question 20) 
Commande : *find / -name passwd*


Question 21) 
Pour rediriger le résultat dans un fihcier *~/list_passwd_files.txt* et que les erreurs soient redirigées vers me fichier spécial */dev/null* on fait la commande : *find / -name passwd > ~/list_passwd_files.txt 2>> /dev/null*

Question 22) 
En utilisant la commande suivante :
Commande : *grep -ll*
Résultat : l'alias *ll* est défini dans *grep [OPTION]... PATTERNS[FILE]...*


Question 23) 
Installation de *locate* : *apt install mlocate*
Chercher le fichier history.log : *locate history.log*
Résultat : */var/log/apt/history.log*

Question 24) 
Rien ne s'affiche lorsqu'on fait la commande *locate fichier_a_trouver*, alors que nous avions créé le fichier précédemment.
Rien apparait après avoir utiliser *locate* . Cela est surement du au fait que la base de donnée n'a pas été mise à jour depuis la création du fichier créé. Pour actualiser il faut faire la commande : updatedb.

**Exercice 4**

Question 3)
L’invite de commande change nien de couleur :  *rootoor@serveur* est vert,*:$* devient blanc et  *~* devient bleu.

Question 4)
Modifier la séquence dans .bashrc : *nano .bashrc*
A la ligne commençant par *P1=* on ajoute * \[\e[31m\A\e[0m-\[\033[1;92m]\u@\h\[\033[00m\]*

Résultat : rootoor@serveur est en vert clair, le chemin est en bleu et l'heure est en rouge.

