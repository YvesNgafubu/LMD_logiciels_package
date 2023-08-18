# LMD_logiciels_package
Dans ce package, contient quelques logiciels nécessaire pour un étudiant débutant en Math-info. 
    NB: Ce travail n'est que la version Beta et n'hésiter pas 
####################################################################################################

1. Avantages du packages   
Ce package est richement bénis et offres plusieurs  
avantages aux étudiants admis en math-info et même pour ceux de mathématique, les avantages sont :  
 Chaque logiciel a une description là-dessus et vous permet d’installer le logiciel dont vous voulez avec plus de précision et exactitude ;  
 Le package est vraiment facile à installer, il suffit de suivre les directives et taper une ligne de code puis procéder à l’installation, la possibilité est d’installer soit le package entier ou un logiciel spécifique uniquement 
;  
  
2. Fonctionnement du package et de l’environnement   
Le package est hébergé dans une machine serveur, alors une machine cliente effectuera une demande de téléchargement de ce package et peux installer maintenant les différents logiciels sur la machine cliente ou soit l’installation de tous les logiciels commence automatiquement lorsque la machine cliente fais appelle à la machine serveur pour avoir le package.   
  
3. Procédure d'installation  
1.	Téléchargez  le  package  depuis https://mathinfopackage.genielectrik.com/download/mathinfopackage.deb   
2.	Placez-vous dans le répertoire de téléchargement.  
3.	Exécutez la commande suivante en tant qu'utilisateur root pour installer le package :  
 sudo dpkg -i mathinfo-package.deb  
  
Après l'installation, vous pouvez lancer le package en utilisant la commande suivante :  
 	 LMD_logiciels_package

  
4.	Attention : Si vous rencontrez l’erreur : dpkg frontend verrouillé par un autre processus, suivez ceci:  
  
L'erreur "dpkg: erreur: dpkg frontend verrouillé par  
un autre processus" signifie que le gestionnaire de paquets dpkg est déjà en cours d'utilisation par un autre processus sur votre système. Cela peut se produire si vous avez un autre gestionnaire de paquets ou une mise à jour en cours d'exécution en arrière-plan. Voici quelques étapes que vous pouvez suivre pour résoudre ce problème :  
1.	Vérifiez les processus en cours d'exécution : Ouvrez un terminal et exécutez la commande suivante pour vérifier si un autre processus dpkg est en cours d'exécution :  
 ps aux | grep -i dpkg  
Cela affichera une liste de processus associés à dpkg. Si vous en trouvez un autre en cours d'exécution, vous devrez le terminer avant de continuer.  
  
2.	Supprimez le fichier de verrouillage : Le verrouillage de dpkg est généralement géré par un fichier situé dans le répertoire `/var/lib/dpkg/`. Vous pouvez le supprimer en exécutant la commande suivante :   sudo rm /var/lib/dpkg/lock  
Assurez-vous d'exécuter cette commande avec les privilèges de superutilisateur (sudo).  
  
  
3.	Réparez les paquets cassés : Si le problème persiste, vous pouvez essayer de réparer les paquets cassés en exécutant les commandes suivantes :  
 sudo dpkg --configure -a  sudo apt --fix-broken install  
  
Cela aidera à réparer les dépendances manquantes ou cassées qui pourraient causer des problèmes avec dpkg.  
  
4.	Redémarrez le système : Si toutes les étapes précédentes échouent, vous pouvez essayer de redémarrer votre système. Cela permettra de terminer tous les processus en cours d'exécution et de réinitialiser les verrouillages de dpkg.  
Après avoir suivi ces étapes, vous devriez pouvoir utiliser dpkg sans rencontrer l'erreur de verrouillage du frontend.  
Reprenez alors l'installation depuis le début  
  
Profitez de cette collection d'outils logiciels pour faciliter votre parcours d'étudiant en informatique et améliorer votre productivité dans vos projets et études. N'hésitez pas à explorer chaque logiciel pour en découvrir les fonctionnalités et les avantages.  
7. Installation :  
Après la phase de développement, il fallait convertir le projet en un package Debian ; pour ce faire voici la procédure empruntée :  
o	Ouvrir le terminal puis se positionner dans le répertoire parent du projet  
o	Taper: 	>dpkg-deb 	–build LMD_logiciels_package mathinfopackage.deb  
Après cette procédure un fichier LMD_logiciels_package.deb est généré, ainsi nous pouvons installer notre package via cette commande :   
o	> sudo dpkg -i LMD_logiciels_package.deb
  
 
  
Fin de l’installation, nous pouvons à présent vérifier si notre package s’est correctement installé en faisant :  
> dpkg l > pack.txt  
> gedit pack.txt  
Ces commandes va nous générer un fichier contenant la liste de tous les packages installés sur notre machine et en déroulant cette liste, à la 1352ème ligne nous voyons clairement que notre package est correctement installé et reprend la description renseignée dans le fichier control  
  
  
On peut aussi vérifier la disponibilité de notre package :
  
8. Utilisation du package :  
Maintenant que notre package est correctement installé nous pouvons le lancer en tapant juste :  
