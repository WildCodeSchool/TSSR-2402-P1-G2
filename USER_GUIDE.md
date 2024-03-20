# Guide utilisateur Téléassistance


## Sommaire
1. Utilité de la téléassitance
2. Utilisation du Bureau d'accès à distance de Windows
3. Utilisation du logiciel TightVNC
4. FAQ 



### 1. Utilité de la téléassitance


#### Un support plus efficace

Vous êtes technicien de support informatique. Vous gérez un parc conséquent de postes de travail et vos utilisateurs ont un système de relève d'anomalie ou de demande d'assistance sous la forme de ticket. Dans tous les cas conduisant à une intervention directement sur le poste, les systèmes de prise de contrôle à distance se révèlent très profitables.

#### Une intervention plus rapide

Le bénéfice le plus important de ces technologies est l'intervention directe, à distance et immédiate sur le poste cible. Mais, en conséquence, je citerais également les apports suivants :

- Une augmentation nette de la qualité de service, les tickets sont résolus rapidement car ils ne nécessitent aucune logistique ;

- Un entretien indéniable de la confiance des utilisateurs, qui prennent très rapidement l'habitude de vos prises de contrôle pour résoudre leurs soucis ;

- Une productivité accrue car les diagnostiques sont rapides et les interventions sont très peu coûteuses.

#### Un service plus facile côté utilisateur

Concrètement, il est souvent laborieux pour un utilisateur de devoir expliquer son besoin ou problème par écrit avec un vocabulaire qu'il ne maîtrise pas. A l'inverse, il est très efficace pour lui d'en faire une démonstration en temps réel à une équipe de maintenance qui peut intervenir immédiatement et de manière interactive. Cette technique évite de nombreux échanges inutiles que ce soit pour la description du problème, ou encore pour la vérification de la correction.

Avec le contrôle à distance vous intervenez quasiment dans les mêmes conditions qu'un support personnalisé où vous êtes physiquement à côté de l'utilisateur.




### 2. Utilisation du Bureau d'accès à distance de Windows


Voici l'explication de la connexion du **Bureau A Distance**

Double clique sur l'icône de lancement situé sur le bureau

![](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/RDP_shortcut.png>)

Une fois le logiciel lancé, on devrait avoir cette fenêtre qui s'ouvre

![](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20ip.jpg>)

Cliquer sur connexion puis inserer le mot de passe : Azerty1* (definit par votre administrateur) 

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20MDP.jpg)

Une fois connecté(e) vous devriez avoir ce rendu

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20connecte%C3%A9%20serv.jpg)

Il y a une barre d'icone en haut de votre fenêtre

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Barre%20info.jpg)

De gauche à droite :
- épingler : permet d'épingler cette barre en haut de l'écran (si décochée, elle disparait sous 3 sec et réapparait en passant la souris dessus)
- barres réseaux : permet de connaitre l'intensité du signal réseaux
- adresse IP (ou nom) : permet de savoir sur quel poste on travail
- reduire : permet de reduire la fenêtre dans la barre des tâches
- niveau inferieur : permet de rétrecir la fenêtre
- fermer : ferme et quitte la session de travail


### 3. Utilisation du logiciel TightVNC


Voici l'explication de connexion sur **TightVnc** Viewer:

Double clique sur l'icône de lancement situé sur le bureau

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/vnc_shortcut.png)

Une fois le logiciel lancé, on devrait avoir cette fenêtre qui s'ouvre

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/TightVnc%20ouverture.png)

Puis insérer le mot de passe : Remote1* (définit par votre administrateur)


Une fois connecté(e) vous devriez avoir ce rendu.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/TightVnc%20%C3%A9crans.png)
L'affichage d'un écran noir en fond sur le poste Serveur est normal.

Il y a une barre d'icônes en haut de la fenêtre de TightVNC.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/TightVnc%20barre%20d'icons.jpg)

De gauche à droite : 
- nouvelle connexion: permet d'ouvrir une nouvelle connexion en plus de la première
- sauvegarde 
- ouverture des options
- info connexion
- pause 
- actualisation image
- raccourci ctrl+alt+del
- raccourci ctrl+esc
- raccourci ctrl
- raccourci alt
- transfert de fichier entre client/server
- zoomer
- dézoomer
- zoomer par pourcentage
- zoom auto
- plein écran

En cliquant sur le bouton option, cela vous permet d'ajuster les paramètres de la prise en main :

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/option%20par%20defaut.png)

Si vous notez des ralentissements ou un peu de latence dans l'exécution de votre prise en main:
Vous pouvez jouez sur les paramètres suivants :
- Laissez l'option "**Prefered encoding**" sur *Tigh*. C'est le format conseillé par l'éditeur du logiciel.
- Cocher **256 colors**, cela affichera le poste serveur en 256 colours et donc améliorera grandement la latence entre les deux postes.
- Vous pouvez aussi jouer sur le taux de compression **Set custom compression level**.
- Vous pouvez aussi baissez la qualité des images en cochant **Allow JPEG, set image quality** et en mettant la qualité sur **poor**.

Les autres paramètres sont aussi intéressants :
- Dans la partie **Display** :
  - Afficher en plein écran via la case à cocher **Full-screen mode**
  - Encore via l'option **Scale-by** changer la mise à l'échelle (par défaut à 100%)
- Dans la partie **Mouse** et **Mouse Cursor**
  - Changez l'affichage du pointeur de la souris
- Ainsi que d'autres options que vous pouvez alors explorer.


### 4. FAQ


### Bureau d'accès à distance

Pourquoi ne puis-je pas me connecter à l’aide du Bureau à distance ?

Voici quelques solutions possibles aux problèmes courants que vous pouvez rencontrer lorsque vous tentez de vous connecter à un PC distant. Si ces solutions ne fonctionnent pas, vous trouverez plus d’informations sur le site web de Microsoft Community.

**Impossible de trouver un PC distant**. Assurez-vous d’avoir le nom de PC adéquat, puis vérifiez si vous avez entré ce nom correctement. Si vous ne pouvez toujours pas vous connecter, essayez d’utiliser l’adresse IP du PC distant au lieu de son nom.

**Un problème de réseau est survenu**. Vérifiez que vous disposez d’une connexion à Internet.

**Le port du Bureau à distance peut être bloqué par un pare-feu**. Si vous utilisez un pare-feu Windows, procédez comme suit :

  - Ouvrez le pare-feu Windows.
  - Cliquez sur **Autoriser une application ou une fonctionnalité via le Pare-feu Windows**.
  - Cliquez sur **Modifier les paramètres**. Vous devrez peut-être saisir votre mot de passe administrateur ou confirmer votre choix.
  - Sous **Applications et fonctionnalités autorisées**, sélectionnez **Bureau à distance**, puis appuyez ou cliquez sur **OK**.
  - Si vous utilisez un autre pare-feu, assurez-vous que le port Bureau à distance (généralement 3389) est ouvert.

**La fonctionnalité Connexion à distance ne peut pas être configurée sur le PC distant**. Pour résoudre ce problème, revenez à la question Comment configurer un PC pour le Bureau à distance ? de cette rubrique.

**Le PC à distance peut autoriser uniquement la connexion des PC dont l’authentification au niveau du réseau est configurée.**

**Le PC à distance est peut-être désactivé**. Vous ne pouvez pas vous connecter à un PC qui est désactivé, en veille ou en veille prolongée. Par conséquent, vérifiez que les paramètres de mise en veille et veille prolongée sur un PC distant sont définis sur **Jamais**. Remarque : La mise en veille prolongée n’est pas disponible pour tous les PC.


#### Quels PC puis-je utiliser pour accéder au client web ?

Le client web prend en charge Windows, macOS, Linux et ChromeOS. Il ne prend pas en charge les appareils mobiles pour l’instant.



### TightVNC


#### Quelles sont les versions de Windows supportées par TightVNC ?

TightVNC fonctionne en principe sur toutes les versions de Windows (les systèmes 32 bits et 64 bits sont pris en charge) :
    Windows XP / Vista / 7 / 8 / 8.1 / 10 / 11,
    les versions correspondantes de Windows Server.
Sous Windows XP, vous devez avoir installé le dernier Service Pack. Les systèmes Windows CE ne sont pas pris en charge.
Il n'y a pas d'exigences minimales en matière d'espace disque ou de mémoire vive. TightVNC utilise si peu d'espace et de mémoire qu'il peut fonctionner partout où Windows est en cours d'exécution.
Les versions antérieures 1.2 et 1.3 de TightVNC présentent toutefois certaines limitations. Il n'est pas possible d'utiliser TightVNC Server en tant que service système sur Windows Vista / Windows 7 dans ce cas. 

#### Comment quitter le mode plein écran de TightVNC Viewer ?

Pour quitter le mode plein écran de TightVNC Viewer pour Windows, vous pouvez utiliser la combinaison de clavier Ctrl-Alt-Shift-F.
La raison de cette combinaison de clavier complexe est que nous devons utiliser un raccourci clavier qui n'est pas susceptible d'être utilisé par des applications normales. Si une combinaison est utilisée comme raccourci clavier dans la visionneuse TightVNC, elle sera traitée localement dans la visionneuse et ne sera donc pas transmise au serveur VNC, ce qui peut poser des problèmes avec les applications distantes qui utilisent le même raccourci clavier.
Dans nos applications modernes telles que Remote Ripple et MightyViewer, il est beaucoup plus facile de quitter le mode plein écran. Il suffit de déplacer le pointeur de la souris sur le bord supérieur de l'écran et une barre d'outils flottante apparaît, dans laquelle vous pouvez choisir de quitter le mode plein écran. 

#### TightVNC fonctionne-t-il sur Mac OS X ?

Actuellement, nous ne proposons pas de version pour Mac OS X. Il est très probable que TightVNC en propose une à l'avenir, mais pas dans les jours qui viennent. Actuellement, notre équipe est occupée à travailler sur la version Windows.
Si vous avez besoin d'une partie visionneuse sur Mac OS X, essayez TightVNC Java Viewer. Il est multiplateforme et devrait fonctionner correctement sur tout système où l'environnement Java peut être installé, y compris Mac OS X.
Notez également que les versions récentes de Mac OS X comprennent un serveur VNC intégré qui est également compatible avec TightVNC. En d'autres termes, vous pouvez vous connecter à n'importe quel système Mac OS X moderne avec TightVNC Viewer. 


