# Guide utilisateur Téléassistance

## Sommaire
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


### 2. Utilisation basique bureau d'accès à distance

### 3. Utilisation basique TightVNC

### 4. Utilisation avancé bureau d'accès à distance

### 5. Utilisation avancé TightVNC

### 6. FAQ bureau d'accès à distance

### 7. FAQ TightVNC

#### - Quelles sont les versions de Windows supportées par TightVNC ?

TightVNC fonctionne en principe sur toutes les versions de Windows (les systèmes 32 bits et 64 bits sont pris en charge) :
    Windows XP / Vista / 7 / 8 / 8.1 / 10 / 11,
    les versions correspondantes de Windows Server.
Sous Windows XP, vous devez avoir installé le dernier Service Pack. Les systèmes Windows CE ne sont pas pris en charge.
Il n'y a pas d'exigences minimales en matière d'espace disque ou de mémoire vive. TightVNC utilise si peu d'espace et de mémoire qu'il peut fonctionner partout où Windows est en cours d'exécution.
Les versions antérieures 1.2 et 1.3 de TightVNC présentent toutefois certaines limitations. Il n'est pas possible d'utiliser TightVNC Server en tant que service système sur Windows Vista / Windows 7 dans ce cas. 

#### - Comment quitter le mode plein écran de TightVNC Viewer ?

Pour quitter le mode plein écran de TightVNC Viewer pour Windows, vous pouvez utiliser la combinaison de clavier Ctrl-Alt-Shift-F.
La raison de cette combinaison de clavier complexe est que nous devons utiliser un raccourci clavier qui n'est pas susceptible d'être utilisé par des applications normales. Si une combinaison est utilisée comme raccourci clavier dans la visionneuse TightVNC, elle sera traitée localement dans la visionneuse et ne sera donc pas transmise au serveur VNC, ce qui peut poser des problèmes avec les applications distantes qui utilisent le même raccourci clavier.
Dans nos applications modernes telles que Remote Ripple et MightyViewer, il est beaucoup plus facile de quitter le mode plein écran. Il suffit de déplacer le pointeur de la souris sur le bord supérieur de l'écran et une barre d'outils flottante apparaît, dans laquelle vous pouvez choisir de quitter le mode plein écran. 

#### - TightVNC fonctionne-t-il sur Mac OS X ?

Actuellement, nous ne proposons pas de version pour Mac OS X. Il est très probable que TightVNC en propose une à l'avenir, mais pas dans les jours qui viennent. Actuellement, notre équipe est occupée à travailler sur la version Windows.
Si vous avez besoin d'une partie visionneuse sur Mac OS X, essayez TightVNC Java Viewer. Il est multiplateforme et devrait fonctionner correctement sur tout système où l'environnement Java peut être installé, y compris Mac OS X.
Notez également que les versions récentes de Mac OS X comprennent un serveur VNC intégré qui est également compatible avec TightVNC. En d'autres termes, vous pouvez vous connecter à n'importe quel système Mac OS X moderne avec TightVNC Viewer. 
### 8. Annexes
