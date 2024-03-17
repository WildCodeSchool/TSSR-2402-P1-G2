**Le logiciel TightVNC**

Téléchargable sur https://www.tightvnc.com/download.php 

**Avantages de TightVNC :**

1. **Gratuit et open-source :** TightVNC est un logiciel open-source, ce qui signifie qu'il est disponible gratuitement et que son code source peut être consulté et modifié selon les besoins.
1. **Facilité d'utilisation :** TightVNC est relativement facile à installer et à configurer, ce qui le rend accessible même pour les utilisateurs moins expérimentés.
1. **Multiplateforme :** TightVNC est compatible avec différentes plateformes, notamment Windows, Linux et macOS, ce qui permet une plus grande flexibilité dans les environnements hétérogènes.
1. **Faible bande passante :** Il offre une bonne performance même dans des conditions de bande passante limitée, ce qui le rend adapté aux connexions Internet plus lentes.
1. **Sécurité :** Bien que cela dépende de la configuration, TightVNC propose des options de sécurité telles que l'authentification par mot de passe et le cryptage des données, ce qui permet de protéger les connexions à distance.

**Inconvénients de TightVNC :**

1. **Sécurité :** Bien que TightVNC offre des options de sécurité, il peut être considéré comme moins sécurisé que d'autres solutions de téléassistance plus avancées, surtout si la configuration n'est pas correctement réalisée.
1. **Performance :** Dans certains cas, TightVNC peut être moins performant que d'autres solutions de téléassistance, en particulier sur des réseaux très chargés ou avec une latence élevée.
1. **Interface utilisateur limitée :** L'interface utilisateur de TightVNC est assez basique et peut manquer de certaines fonctionnalités avancées présentes dans d'autres logiciels similaires.
1. **Support limité :** Étant un logiciel open-source, le support technique officiel peut être limité, bien que la communauté des utilisateurs puisse fournir une assistance via des forums et des discussions en ligne.

En résumé, TightVNC est une option populaire pour la téléassistance en raison de sa simplicité, de sa compatibilité multiplateforme et de sa gratuité. Cependant, il peut présenter des limitations en termes de sécurité et de performances par rapport à d'autres solutions commerciales. Il convient donc de peser ces avantages et inconvénients en fonction des besoins spécifiques de votre projet.





**Installation et configuration sous Windows : partie server**

TightVNC est disponible au téléchargement depuis l’adresse suivante : <https://www.tightvnc.com/download.php>.

La méthode la plus simple est de télécharger le fichier compatible pour l’installateur **WindowsServer**
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/lien%20t%C3%A9l%C3%A9chargement.png)

Section d'installation de TightVNC sous Windows

Le fichier s’exécute sous la forme d’un **didacticiel** vous guidant pendant les étapes de l’installation.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC2%20(2).png)










Le programme d’installation propose **3 options** classiques :

- L’installation **typique**, tout se passe de manière automatique avec les composants et leurs valeurs par défaut (partie serveur, partie cliente, mot de passe, emplacement sur le disque, etc.) ;
- L’installation **Custom,** ici le programme demande confirmation et de chaque étape ;
- L’installation **complète,** identique à la première option, mais en incluant tous les composants disponibles. 

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ3.png)

Dans notre cas, je vous propose de passer par **l’installation personnalisée(Custom)**.













L’étape suivante consiste à sélectionner le type d’installation. S'il s'agit du poste **qui sera contrôlé** à distance, dans ce cas il faut installer TightVNC **Server.** S’il s’agit du poste avec lequel **vous prendrez le contrôle** à distance d’un autre, il faut installer TightVNC **Client.(voir installation coté client)**


![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ4.png)

Type d'installation : client ou serveur ?

Ici, nous allons choisir d’installer les **deux composants**.











Le programme d’installer propose ensuite la configuration de **4 options distinctes** :

- **L’association des fichiers avec une extension .vnc** est pratique, vous pouvez garder cette option ;
- **Déclarer TightVNC en tant que service** va dépendre de vos contraintes de sécurité. Dans le cas où vous souhaitez démarrer les programmes TightVNC de manière automatique avec le poste, il faut cocher cette option. Je reviendrai plus en détail sur cet aspect dans le chapitre suivant ;
- L’option suivante autorise les programmes TightVNC à exécuter la séquence « **Ctrl-Alt-Del** » bien connue permettant notamment d’envoyer un ordre de redémarrage au système d’exploitation. En la cochant, vous autorisez l’utilisateur ayant le contrôle du poste à effectuer cette opération ;
- Enfin, dernière option, il s’agit d’ajouter une règle dans le **Firewall** Windows afin de **laisser passer les flux réseaux** concernant TightVNC. Cela me paraît tout à fait justifié.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ5.png)

Fenêtre de tâches additionnelles

Je vous propose donc de **cocher les 4 options** proposées. Notez que Windows vous demandera très probablement confirmation de l’action, car nous ajoutons ici des règles systèmes supplémentaires.








![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ6.png)

Demande de confirmation de Windows

Le panneau suivant est important car il permet de **sécuriser** l’installation de TightVNC sur le poste. Il s’agit ici de définir **deux mots de passe différents** :

- **Le premier** mot de passe va permettre de **sécuriser la prise de contrôle** à distance sur ce poste. **Chaque client** VNC souhaitant s’y connecter devra connaître ce mot de passe ;
- **Le second** permet de **sécuriser le comportement et la configuration** de TighVNC sur ce poste. **Chaque modification** dans la configuration ou l’exécution du serveur TightVNC devra être confirmée avec ce mot de passe.





















![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ7.png)


Définition des mots de passe

N’hésitez pas à saisir les mots de passe « **forts** », c’est à dire avec au moins un **caractère spécial**, un **chiffre** et une **majuscule.**













Voilà ! L’installation se termine ici. Nous allons maintenant vérifier que tout s’est bien passé.

**Que venons-nous d'installer ?**

Normalement, un icône supplémentaire VNC s’est ajoutée dans la barre des tâches Windows.


![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ8.png)

Icône VNC dans la barre des tâches Windows

Cet icône nous permet d’accéder au panneau de configuration, je reviendrai sur le sujet dans le chapitre suivant.

Vous avez également des **raccourcis supplémentaires** en fonction des composants installés dans le menu Windows tels que par exemple : 

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ9.png)

Raccourcis supplémentaires 


Par ailleurs, si vous avez sélectionnez l’option d’installation de TightVNC en tant que service, vous retrouverez la ligne associée dans le menu services de Windows, telle que :

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ10.png)


Service de TightVNC dans le menu services Windows

De plus, vous pouvez également retrouver la règle ajoutée pour TightVNC dans le **Firewall** de Windows telle que :

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ11.png)



Règle de TightVNC Server du Firewall


Cette autorisation se traduit par **l’ouverture de ports** en écoute sur le poste. Vous pouvez **lister ces ports** en lançant la commande suivante (depuis une invite de commande en mode Administrateur) :

netstat -abp TCP

Vous pourrez constater l’ouverture de deux ports par défaut, 5800 et 5900.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ12.png)


Les ports 5900 et 5800 sont ouverts

Le port **5900** correspondant au port **d’écoute principal** de TightVNC, celui qui permet la prise de contrôle à distance. Le port **5800** permet de **s’interfacer avec le serveur** TightVNC depuis le poste client.

**Démarrez automatiquement TightVNC sous Windows**

Nous avons vu précédemment qu’il est possible d’installer le serveur TightVNC directement en tant que **service Windows**. Avec cette méthode, TightVNC sera lancé automatiquement **à chaque démarrage de la machine**.

Cependant, si vous n’avez pas coché l’option lors du processus d’installation il est toujours possible après coup d’enregistrer TightVNC en tant que service depuis les raccourcis ajoutés dans le menu Windows.

Par exemple, pour **enregistrer TightVNC** en tant que service :

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ13.png)


Attention, cette action inscrit le service dans les registres Windows **sans le démarrer**. Il est nécessaire soit de **redémarrer** Windows, soit de le **lancer à la main** pour démarrer le serveur.








A l’inverse pour **supprimer le service** TightVNC (sans pour autant désinstaller le programme) :

![Capture des actions possibles pour TightVNC dans le menu Windows, clic sur Unregister TightVNC Service.](Aspose.Words.0af24a61-a349-4af6-8030-9ca6306b37b1.016.png)


Supprimer le service TightVNC

Windows sollicitera une **confirmation** pour ces deux actions, qui sont également disponibles via les options des **lignes de commande** TightVNC comme je vous le montrerai dans le **chapitre suivant**.

