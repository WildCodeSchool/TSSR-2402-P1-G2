# Guide d'installation et mise en place de la Téléassistance
## Sommaire
1. Pré-requis techniques
2. Configurations Poste Serveur et Poste Client
3. Configuration et test connexion du Bureau d'accès à distance
4. Installation & Configuration TightVNC Poste Serveur et Poste Client
5. Test connexion TightVNC
6. Configuration de l'accès sécurisé via TightVNC par filtrage d'adresse IP (depuis serveur)
7. FAQ problèmes techniques et améliorations possibles

### 1. Pré-requis techniques
- Poste serveur : Windows serveur 2022, firewall desactivé, Remote management et Remote Desktop activés, Firewall désactivé
- Poste serveur : Windows 10 Pro, firewall desactivé

### 2. Configurations Poste Serveur et Poste Client
**Configuration Serveur windows**

**Serveur Manager**

• Dans **Serveur Manager**, se rendre dans **Local Server**
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-1.png?raw=true)

Vérifier les points suivants:

*   Remote management “**Enabled**” (Activer)
    
*   Remote desktop “**Enabled**” (Activer)
    
*   IE Enhanced Security Configuration “**Off**” 
    

**Adresse IP**

• Ouvrir le menu *Démarrer*, chercher le **Panel Control**. Ouvrir le **Panel Control**.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-2.png?raw=true)

• Définir la préférence pour afficher les dossiers : "**large**" ou "**small**".
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-3.png?raw=true)


• Ouvrir “**Network and Sharing center**”.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-4.png?raw=true)

• Aller dans la catégorie “**Change adapter settings”**.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-5.png?raw=true)

• Sélectionner la carte **“Ethernet 2”**.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-6.png?raw=true)

• Effectuer un clic droit puis sélectionner “**Properties**”. 
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-7.png?raw=true)
  
• Sélectionner “**Internet Protocol Version 4(TCP/IPV4)**” puis cliquer sur “**Properties**”.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-8.png?raw=true)
  
• Dans "**IP adresse**", rentrer les valeurs suivantes: “**172.16.10.10**”, 
puis dans: “Subnet Mask/masque de sous réseaux”:”**255.255.255.0”**.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-9.png?raw=true)


**Firewall/Pare-feu**

• Ouvrir le menu *Démarrer*, chercher le **Panel Control**. Ouvrir le "**Panel Control**". 
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-2.png?raw=true)
  
• Sélectionner “**Systemes and Securities**”.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-10.png?raw=true)
  
• Ouvrir “**Windows Defender Firewall**”.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-11.png?raw=true)
  
• Sélectionner “**Turn Windows Defender Firewall on or off**”.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-12.png?raw=true)
  
• Désactiver les "*settings*" *privés* et *publics*.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/Config%20ServeurWin-13.png?raw=true)

### Configuration Poste Client

#### Configuration adresse IP

- Renseigner dans la barre de recherche en bas à gauche de votre écran : “Panneau de configuration”. Cliquer sur l’onglet “Panneau de configuration”.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/39e086b1-6656-4398-9735-515bb9331edc)


- Ensuite, aller dans l’onglet “Réseau et Internet”.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/7c53537e-e6d3-49c1-b1f6-030f281345e8)


- Puis l’onglet “Centre Réseau et partage”.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/9bb81101-4e01-4994-a2fb-868590bf33d2)


- En suivant, sur la gauche de la fenêtre, cliquer sur l’onglet “Modifier les paramètres de la carte”.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/70c9fd61-dc7d-47e4-8cd9-83c987618fdc)


- Sélectionner “Ethernet 2”.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/2906debf-f245-45fc-a1ab-6946f0f8b131)


- Effectuer un clic droit > “Propriétés”. 

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/d951adf3-29e1-47b3-b9e8-afacd61bbd5c)


- Sélectionner “Protocole Internet version 4 (TCP/IPv4)” puis cliquer sur “Propriétés”.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/0670bd84-39a9-4a9c-aa04-4660ca9e0db9)


- Décocher “Obtenir une adresse IP automatiquement” en cochant “Utiliser l’adresse IP suivante”
Inscrire comme adresse IP : “172.16.10.20”; et comme masque de sous-réseau : “255.255.255.0”.
Laisser le reste par défaut et valider en appuyant sur “OK”.

#### Désactivation des Pare-feu

- Depuis le Panneau de configuration, aller dans “Système et sécurité” > “Pare-Feu Windows Defender”

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/bb6a808d-1ea0-4bde-a025-5e495a5a837a)

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/8495b8d9-c51f-4f60-9fd5-19aa4b170fe2)

- Sur la gauche de la fenêtre, aller dans l’onglet “Activer ou désactiver le Pare-Feu Windows Defender”.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/6e8b0443-bc0f-4305-bbe2-264aede18e5b)

- Décocher “Activer le Pare-Feu Windows Defender” en cochant “Désactiver le Pare-Feu Windows Defender” pour les paramètres des réseaux privés et publics.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/c8da54d1-80d2-41b7-83b4-3617b3259afd)

- Valider l’opération en cliquant sur “OK”.


### 3. Configuration et test connexion du Bureau d'accès à distance


### ***ACTIVER LE BUREAU A DISTANCE***

#
- Se rendre dans le menu "**DEMARRER**".

![alt text](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/ACTIV%20%20demarrer.jpg?raw=true>)

#
- Aller dans "**PARAMETRES**".

![alt text](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/ACTIV%20parametre.jpg>)

#
- Cliquer sur "**SYSTEME**".

![alt text](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/ACTIV%20systeme.jpg>)

#
- Aller dans "**BUREAU A DISTANCE**"

![alt text](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/ACTIV%20bureau%20a%20distance.jpg>)

#
- Cocher l'onglet "**ACTIVER LE BUREAU A DISTANCE**".

![alt text](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/ACTIV%20activer.jpg>)

#
- Puis "**CONFIRMER**" pour valider l'activation.

![alt text](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/ACTIV%20confirmer.jpg>)

### Test connexion

#
- Se rendre dans "**BARRE DES TACHES**".

![](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20bad.jpg>)

#
- Taper "**CONNEXION BUREAU A DISTANCE**".

![](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20%20barre%20co.jpg>)

#
- Cliquer sur l'application "**CONNEXION BUREAU A DISTANCE**".

![](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20connex%20bad.jpg>)

#
- Renseigner dans le champs, l'adresse IP ou le nom de l'ordinateur dans l'onglet "**ORDINATEUR**".
- Adresse IP : 172.16.10.10
- Nom de l'ordinateur : SRVWIN01

![](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20adresse%20ip.jpg>)

#
- Cliquer sur "**CONNEXION**".

![](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20connexion.jpg>)

#
- Renseigner le **MOT DE PASSE** de la session, puis valider avec "**OK**".

![](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20mot%20de%20passe.jpg>)

![alt text](<https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/CONNEX%20%20valider.jpg>)

### 4. Installation & Configuration TightVNC Poste Serveur et Poste Client

﻿**Le logiciel TightVNC**

Téléchargeable sur https://www.tightvnc.com/download.php 

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
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVnc1.png)

Le programme d’installation propose **3 options** classiques :

- L’installation **typique**, tout se passe de manière automatique avec les composants et leurs valeurs par défaut (partie serveur, partie cliente, mot de passe, emplacement sur le disque, etc.) ;
- L’installation **Custom,** ici le programme demande confirmation et de chaque étape ;
- L’installation **complète,** identique à la première option, mais en incluant tous les composants disponibles. 
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC2%20(2).png)


Dans notre cas, je vous propose de passer par **l’installation personnalisée(Custom)**.

L’étape suivante consiste à sélectionner le type d’installation. S'il s'agit du poste **qui sera contrôlé** à distance, dans ce cas il faut installer TightVNC **Server.** S’il s’agit du poste avec lequel **vous prendrez le contrôle** à distance d’un autre, il faut installer TightVNC **Client.(voir installation coté client)**

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ3.png)

Type d'installation : client ou serveur ?

Ici, nous allons choisir d’installer les **deux composants**.

Le programme d’installer propose ensuite la configuration de **4 options distinctes** :

- **L’association des fichiers avec une extension .vnc** est pratique, vous pouvez garder cette option ;
- **Déclarer TightVNC en tant que service** va dépendre de vos contraintes de sécurité. Dans le cas où vous souhaitez démarrer les programmes TightVNC de manière automatique avec le poste, il faut cocher cette option. Je reviendrai plus en détail sur cet aspect dans le chapitre suivant ;
- L’option suivante autorise les programmes TightVNC à exécuter la séquence « **Ctrl-Alt-Del** » bien connue permettant notamment d’envoyer un ordre de redémarrage au système d’exploitation. En la cochant, vous autorisez l’utilisateur ayant le contrôle du poste à effectuer cette opération ;
- Enfin, dernière option, il s’agit d’ajouter une règle dans le **Firewall** Windows afin de **laisser passer les flux réseaux** concernant TightVNC.


![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ4.png)

Fenêtre de tâches additionnelles

Je vous propose donc de **cocher les 4 options** proposées. Notez que Windows vous demandera très probablement confirmation de l’action, car nous ajoutons ici des règles systèmes supplémentaires.


![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ5.png)


Demande de confirmation de Windows

Le panneau suivant est important car il permet de **sécuriser** l’installation de TightVNC sur le poste. Il s’agit ici de définir **deux mots de passe différents** :

- **Le premier** mot de passe va permettre de **sécuriser la prise de contrôle** à distance sur ce poste. **Chaque client** VNC souhaitant s’y connecter devra connaître ce mot de passe ;
- **Le second** permet de **sécuriser le comportement et la configuration** de TighVNC sur ce poste. **Chaque modification** dans la configuration ou l’exécution du serveur TightVNC devra être confirmée avec ce mot de passe.
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ6.png)

Définition des mots de passe

N’hésitez pas à saisir les mots de passe « **forts** », c’est à dire avec au moins un **caractère spécial**, un **chiffre** et une **majuscule.**

Voilà ! L’installation se termine ici. Nous allons maintenant vérifier que tout s’est bien passé.

**Que venons-nous d'installer ?**

Normalement, un icône supplémentaire VNC s’est ajoutée dans la barre des tâches Windows.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ7.png)

Icône VNC dans la barre des tâches Windows

Cet icône nous permet d’accéder au panneau de configuration, je reviendrai sur le sujet dans le chapitre suivant.

Vous avez également des **raccourcis supplémentaires** en fonction des composants installés dans le menu Windows tels que par exemple : 

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ8.png)

Raccourcis supplémentaires 


Par ailleurs, si vous avez sélectionnez l’option d’installation de TightVNC en tant que service, vous retrouverez la ligne associée dans le menu services de Windows, telle que :

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ9.png)

Service de TightVNC dans le menu services Windows

De plus, vous pouvez également retrouver la règle ajoutée pour TightVNC dans le **Firewall** de Windows telle que :


![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ10.png)


Règle de TightVNC Server du Firewall


Cette autorisation se traduit par **l’ouverture de ports** en écoute sur le poste. Vous pouvez **lister ces ports** en lançant la commande suivante (depuis une invite de commande en mode Administrateur) :

netstat -abp TCP

Vous pourrez constater l’ouverture de deux ports par défaut, 5800 et 5900.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ11.png)

Les ports 5900 et 5800 sont ouverts

Le port **5900** correspondant au port **d’écoute principal** de TightVNC, celui qui permet la prise de contrôle à distance. Le port **5800** permet de **s’interfacer avec le serveur** TightVNC depuis le poste client.

**Démarrez automatiquement TightVNC sous Windows**

Nous avons vu précédemment qu’il est possible d’installer le serveur TightVNC directement en tant que **service Windows**. Avec cette méthode, TightVNC sera lancé automatiquement **à chaque démarrage de la machine**.

Cependant, si vous n’avez pas coché l’option lors du processus d’installation il est toujours possible après coup d’enregistrer TightVNC en tant que service depuis les raccourcis ajoutés dans le menu Windows.

Par exemple, pour **enregistrer TightVNC** en tant que service :

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ12.png)

Attention, cette action inscrit le service dans les registres Windows **sans le démarrer**. Il est nécessaire soit de **redémarrer** Windows, soit de le **lancer à la main** pour démarrer le serveur.


A l’inverse pour **supprimer le service** TightVNC (sans pour autant désinstaller le programme) :

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNCServ13.png)

Supprimer le service TightVNC

Windows sollicitera une **confirmation** pour ces deux actions, qui sont également disponibles via les options des **lignes de commande** TightVNC comme je vous le montrerai dans le **chapitre suivant**.


﻿**Logiciel TightVNC client**

Télécharger et installer TightVNC Viewer : <http://www.tightvnc.com/download.php>

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/lien%20t%C3%A9l%C3%A9chargement.png)

Une fois installé, il suffit de suivre les étapes telles qu'indiqué dans les images.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVnc1.png)

Description générée automatiquement](Aspose.Words.fec98584-ffde-4546-ad08-bc8045e413c7.003.png)


![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC2%20(2).png)

Choisir « Custom ».

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC3.png)

Cliquer sur la petite icône à coté de TightVNC et sélectionner la petite croix. De ce fait, il n'y aura que le TightVNC Viewer d'installé. L’autre sera inutile du coté client. Puis appuyer sur « Next ».

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC4.png)

De nouveau sur « Next ».

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC5.png)

Puis « Install ».

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC6.png)


![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC7.png)

L'installation devrait alors se dérouler normalement.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC8.png)

Aller dans le disque dur de votre ordinateur > Program Files > rentrer dans le dossier de TightVNC. Une fois dedans, clic droit sur le fichier indiqué sur l’image puis sélectionner « Create shortcut ».

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/blob/main/Images/tightVNC9.png)

Ceci est l’icône qui devrait apparaître sur votre Bureau.

### 5. Test connexion TightVNC
insérer doc faites par Damien

### 6. Configuration de l'accès sécurisé via TightVNC par filtrage d'adresse IP (depuis serveur)

Renseigner dans la barre de recherche en bas à gauche de votre écran : “TightVNC Service - Offline Configuration". Cliquer sur l'application du même nom.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/bd6ada6d-48fe-4aae-96bd-7cebea294301)


Dans la fenêtre de l'application, accèder à l'onglet "Acces Control".

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/e8226071-0b9e-4d02-9521-11aa0392334b)


Cliquer sur le bouton "Add" pour paramétrer la ou les adresses IP considérées.

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/cea50dac-c67a-4c8f-826d-5a1c21b56422)


Dans la case "First matching", entrer l'adresse IP du poste client concerné (dans notre cas 172.16.10.20). Si vous souhaitez étendre la plage des adresses IP concernées, alors remplir la case "Last matching IP" au-dessous avec la dernière adresse IP voulue. Dans le cas contraire, laisser cette case vide. Il est alors possible de donner l'accès "Allow", refuser l'accès "Deny" ou encore de laisser le choix à l'utilisateur par le biais d'une fenêtre qui s'ouvrira lors de la requête de téléassistance émise par le poste client "Query local user".
Dans notre cas, et pour des raisons de sécurité et de contrôle, nous cochons cette dernière et appuyons sur "OK".

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/5aef92f3-fbad-4a32-a15b-d47370a4774b)
![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/7467abef-7c51-4f88-a940-20d6894da41c)


Ne pas oublier d'appliquer nos options à l'utilisation de TightVNC en cliquant d'abord sur "Apply" avant de fermer la fenêtre ou d'appuyer sur "OK".

![](https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/e7a30f8d-0600-4826-8c6e-cd19ff4b7815)


### 7. FAQ probleme technique et amélioration possibles
doc commune
