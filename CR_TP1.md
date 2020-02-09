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


4. La commande *ll* permet d'afficher l'intégralité des fichiers, y compris les fichiers cachés. Elle ne possède pas d'entrée dans le manuel car il s'agit d'un raccourci de la commande :

	> *ls -alF* (cf. alias).


Question 5)
La commande ls/bin permet de voir le contenu du dossier bin

6. La commande ls . . renvoie les répertoires parents du dossier dans lequel on se trouve.

Question 7)
C'est la commande pwd qui a ce rôle.

8. On obtient un fichier texte *plop* dans le répertoire courant, avec écrit *yo* une fois dedans.

9. On obtient un fichier texte *plop* dans le répertoire courant, avec écrit *yo* deux fois dedans.

	On en déduit que l'utilisation d'un seul chevron (>) écrase et ajoute du texte. L'utilisation de deux chevrons ajoute simplement le texte dans le fichier avec un retour à la ligne.

10. La commande *file* permet de déterminer le type d'un fichier ou d'un dossier. Par exemple, pour *plop*, il s'agit d'un *ASCII text*, pour *fichier1* d'un *empty*, pour *dossier1* d'un *directory*.

11. On remarque qu'en modifiant *toto*, on modifie également *titi*. En revanche, lorsque l'on supprime *toto*, cela ne supprime pas *titi* et son contenu reste inchangé.

12. Lorsqu'on modifie l'un des documents, l'autre s'actualise automatiquement. Contrairement à la question précédente, lorsqu'on supprime *titi*, *tutu* ne pointe plus vers rien. Le lien symbolique est cassé (*broken symbolic link to titi*).

13. Pour arrêter le défilement, il faut taper *CTRL + S*, et *CTRL + Q* pour reprendre le défilement.

14. Nous réalisons la commande suivante afin d'afficher les 5 premières lignes de *syslog* :

	> *head -5 /var/log/syslog*

	Pour afficher les 15 dernières lignes de *syslog* :

	> *tail -15 /var/log/syslog*

	Pour afficher les lignes entre 10 et 20 de *syslog* :

	> *head -n 10 /var/log/syslog | tail -n 20*

15. Cette commande *dmesg* | *less* (*display message*) permet d'afficher la mémoire tampon de message du noyau.

16. Le fichier *passwd* contient toutes les informations relatives aux logins et mots de passe des comptes d'utilisateurs.

	Pour afficher la page du manuel de passwd, il suffit de taper :

	> *man passwd*

17. Pour afficher uniquement la colonne triée par ordre alphabétique inverse, il faut utiliser la commande :

	> *sort +0 -r /etc/passwd*

18. Pour connaître le nombre d'utilisateurs, on utlise la commande suivante :

	> *wc -l /etc/passwd*

	Cette commande nous indique 31 utilisateurs.

19. Pour connaître le nombre des pages contenant le mot-clé *conversion*, on utilise la commande suivante :

	> *man -k conversion*

	On obtient 4 lignes de résultats, on en déduit que 4 pages de manuel contiennent le mot *conversion*.

20. La commande suivante permet de trouver les fichiers dont le nom est *passwd* sur l'ordinateur :

	> *find / -name passwd*

21. Pour que la liste des fichiers trouvés soit enregistrée dans le fichier~/list_passwd_files.txtet que les erreurs soient redirigées vers le fichier spécial/dev/null, on utilise la commande suivante :

	> *find / -name passwd > ~/list_passwd_files.txt 2>> /dev/null*

22. En utilisant la commande suivante :

	> *grep -ll*

	on voit que ll est défini dans *grep [OPTION]... PATTERNS[FILE]...*

23. On installe d'abord la commande *locate* avec la commande suivante :

	> *apt install mlocate*

	On peut ensuite chercher le chemin vers le fichier avec la commande suivante :

	> *locate history.log*

	On obtient alors le chemin */var/log/apt/history.log*

24. Rien ne s'affiche lorsqu'on fait la commande *locate fichier_a_trouver*, alors que nous avions créé le fichier précédemment.

**Exercice 4**

3. L’invite de commande passe en effet en couleur. La partie *rootoor@serveur* est verte, *~* devient bleue et *:$* blanche.

4. Il faut changer une séquence dans .bashrc. Pour cela on exécute la commande suivante :

	> *nano .bashrc*

	Puis on recherche dans le fichier les lignes commençant pas *P1=*.

	Enfin on rajoute la ligne :

	> * \[\e[31m\A\e[0m-\[\033[1;92m]\u@\h\[\033[00m\]*

	On a ainsi l’heure en rouge, rootoor@serveur en vert clair et le chemin en bleu.
