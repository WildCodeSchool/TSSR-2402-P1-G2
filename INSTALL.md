# Guide d'installation et mise en place de la Téléassistance
## Somaire
1. Pré-requis techniques
2. Configuration Poste Serveur
3. Configuration Poste Client
4. Configuraiton Bureau d'accès à distance
5. Test et connextion Bureau d'accès à distance
6. Installation & Configuraiton TightVNC Poster Serveur
7. Installation & Configuraiton TightVNC Poster Client
8. Test connection TightVNC
9. FAQ probleme technique et amélioration possibles

### 1. Pré-requis techniques
- Poste serveur : Windows serveur 2022, firewell desactivé, Remote management et Remote Desktop activé, Firewall désactivé
- Poste serveur : Windows 10 Pro, firewell desactivé

### 2. Configuration Poste Serveur


### 3. Configuration Poste Client

#### Configuration adresse IP

- Renseigner dans la barre de recherche en bas à gauche de votre écran : “Panneau de configuration”. Cliquer sur l’onglet “Panneau de configuration”.

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/39e086b1-6656-4398-9735-515bb9331edc" width="400" height="350"></p>


- Ensuite, aller dans l’onglet “Réseau et Internet”.

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/7c53537e-e6d3-49c1-b1f6-030f281345e8" width="650" height="350"></p>


- Puis l’onglet “Centre Réseau et partage”.

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/9bb81101-4e01-4994-a2fb-868590bf33d2" widht="650" height="350"></p>


- En suivant, sur la gauche de la fenêtre, cliquer sur l’onglet “Modifier les paramètres de la carte”.

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/70c9fd61-dc7d-47e4-8cd9-83c987618fdc" widht="650" height="350"></p>


- Sélectionner “Ethernet 2”.

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/2906debf-f245-45fc-a1ab-6946f0f8b131" widht="650" height="350"></p>


- Effectuer un clic droit > “Propriétés”. 

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/d951adf3-29e1-47b3-b9e8-afacd61bbd5c" widht="650" height="350"></p>


- Sélectionner “Protocole Internet version 4 (TCP/IPv4)” puis cliquer sur “Propriétés”.

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/0670bd84-39a9-4a9c-aa04-4660ca9e0db9" widht="650" height="350"></p>


- Décocher “Obtenir une adresse IP automatiquement” en cochant “Utiliser l’adresse IP suivante”
Inscrire comme adresse IP : “172.16.10.20”; et comme masque de sous-réseau : “255.255.255.0”.
Laisser le reste par défaut et valider en appuyant sur “OK”.

#### Désactivation des Pare-feu

- Depuis le Panneau de configuration, aller dans “Système et sécurité” > “Pare-Feu Windows Defender”

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/bb6a808d-1ea0-4bde-a025-5e495a5a837a" widht="650" height="350"></p>

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/8495b8d9-c51f-4f60-9fd5-19aa4b170fe2" widht="650" height="350"></p>

- Sur la gauche de la fenêtre, aller dans l’onglet “Activer ou désactiver le Pare-Feu Windows Defender”.

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/6e8b0443-bc0f-4305-bbe2-264aede18e5b" widht="650" height="350"></p>

- Décocher “Activer le Pare-Feu Windows Defender” en cochant “Désactiver le Pare-Feu Windows Defender” pour les paramètres des réseaux privés et publics.

<p align="center"><img src="https://github.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/assets/158192308/c8da54d1-80d2-41b7-83b4-3617b3259afd" widht="650" height="350"></p>

- Valider l’opération en cliquant sur “OK”.


### 4. Configuraiton Bureau d'accès à distance
insérer doc faites par charles

### 5. Test et connextion Bureau d'accès à distance
insérer doc faites par charles

### 6. Installation & Configuraiton TightVNC Poster Serveur
insérer doc faites par Damien

### 7. Installation & Configuraiton TightVNC Poster Client
insérer doc faites par Damien

### 8. Test connection TightVNC
insérer doc faites par Damien

###< 10. Configuration de l'accès sécurisé via TightVNC par filtrage d'adresse IP (depuis serveur)

Renseigner dans la barre de recherche en bas à gauche de votre écran : “TightVNC Service - Offline Configuration". Cliquer sur l'application du même nom.


Dans la fenêtre de l'application, accèder à l'onglet "Acces Control".


Cliquer sur le bouton "Add" pour paramètrer la ou les adresses IP considérées.


Dans la case "First matching", entrer l'adresse IP du poste client concerné (dans notre cas 172.16.10.20). Si vous souhaitez étendre la plage des adresses IP concernées, alors remplir la case "Last matching IP" au-dessous avec la dernière adresse IP voulue. Dans le cas contraire, laisser cette case vide. Il est alors possible de donner l'accès "Allow", refuser l'accès "Deny" ou encore de laisser le choix à l'utilisateur par le biais d'une fenêtre qui s'ouvrira lors de la requête de téléassistance émise par le poste client "Query local user".
Dans notre cas, et pour des raisons de sécurité et de contrôle, nous cochons cette dernière et appuyons sur "OK".


Ne pas oublier d'appliquer nos options à l'utilisation de TightVNC en cliquant d'abord sur "Apply" avant de fermer la fenêtre ou d'appuyer sur "OK".




### 9. FAQ probleme technique et amélioration possibles
doc commune
