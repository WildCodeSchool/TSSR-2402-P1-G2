# Guide d'installation et mise en place de la Téléassistance
## Sommaire
1. Pré-requis techniques
2. Configuration Poste Serveur
3. Configuration Poste Client
4. Configuration Bureau d'accès à distance
5. Test et connexion Bureau d'accès à distance
6. Installation & Configuration TightVNC Poste Serveur
7. Installation & Configuration TightVNC Poste Client
8. Test connexion TightVNC
9. Configuration de l'accès sécurisé via TightVNC par filtrage d'adresse IP (depuis serveur)
10. FAQ problèmes techniques et améliorations possibles

### 1. Pré-requis techniques
- Poste serveur : Windows serveur 2022, firewall desactivé, Remote management et Remote Desktop activés, Firewall désactivé
- Poste serveur : Windows 10 Pro, firewall desactivé

### 2. Configuration Poste Serveur
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

### 3. Configuration Poste Client

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


### 4. Configuration Bureau d'accès à distance
insérer doc faites par charles

### 5. Test & Connexion Bureau d'accès à distance
insérer doc faites par charles

### 6. Installation & Configuration TightVNC Poste Serveur
insérer doc faites par Damien

### 7. Installation & Configuration TightVNC Poste Client
insérer doc faites par Damien

### 8. Test connexion TightVNC
insérer doc faites par Damien

### 9. Configuration de l'accès sécurisé via TightVNC par filtrage d'adresse IP (depuis serveur)

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


### 10. FAQ probleme technique et amélioration possibles
doc commune
