# Mise en place d'une Téléassistance

![](https://raw.githubusercontent.com/WildCodeSchool/TSSR-2402-P1-G2-Teleassistance/main/Images/TAexemple.png)


## Sommaire 
1. Présentation du projet et objectifs
2. Mise en contexte
3. Présentation de l'équipe
4. Choix techniques
5. Difficultés & solutions trouvées
6. Améliorations

   
### 1. Présentation du projet et objectifs
- Objectif principal :
   - Configurer un accès sécurisé pour faire de la téléassistance sur un serveur en utilisant une interface graphique depuis un client.
   - Téléassitance à mettre en place via logiciel **_TightVNC_** et la **_connexion Bureau à distance de Windows_**.

- Objectif secondaire :
   - Script Powershell pour faciliter la connexion initiale de la téléassitance.

### 2. Mise en contexte
Mettre en place une téléassitance d'un poste serveur depuis un poste distant pour faciliter les opérations de maintenance, le tout par le biais d'un accès sécurisé.

### 3. Présentation de l'équipe
L'équipe pour le projet est constituée des personnes suivantes :
- Charles Caulier
- Damien Legay
- Nicolas Maggiori
- Luca Pouilly
- Bruno Serna

Durant tout le projet les rôles et taches de chacun sont répartis de la façon suivante :

Rôle Semaine 1 :
| PO | SM |
|:-: |:-:|
| Luca Pouilly | Bruno Serna |

Tâches Semaine 1 :
| Tâche | Personne |
|:-: |:-:|
| Configuration VM Poste Serveur | Luca Pouilly |
| Configuration VM Poste Client | Nicolas Maggiori |
| Bureau d'accès à distance | Charles Caulier |
| Logiciel TightVNC |  Damien Legay |
| Objectif secondaire prise d'infos | Bruno Serna |

Rôle Semaine 2 :
| PO | SM |
|:-: |:-:|
| Damien Legay | Charles Caulier |

Tâches Semaine 2 :
| Tâche | Personne |
|:-: |:-:|
| Rédaction documentations | Luca Pouilly, Nicolas Maggiori |
| Réalisation démonstration logiciels | Damien Legay, Charles Caulier |
| Ecriture script PowerShell | Bruno Serna |

### 4. Choix techniques

Le client est sous Windows 10
- Nom : CLIWIN01
- Compte : wilder
- Mot de passe : Azerty1*
- Adresse IP fixe : 172.16.10.20/24

Le Serveur est sous OS Windows Server 2022
- Nom : SRVWIN01
- Compte : Administrator
- Mot de passe : Azerty1*
- Adresse IP fixe : 172.16.10.10/24

Logiciel de prise en main à distance
- TightVNC Version 2.8.81 ( logiciel gratuit et OpenSource )
- Bureau d'accès à distance ( solution native de Windows )

### 5. Difficultés & solutions trouvées

- Lors de la première connexion avec TightVNC, on a eu un écran noir côté poste client, impossible de voir ce que l'on faisait sur le poste serveur.
  - Paramétrage à revoir côté serveur de TighVNC pour optimiser la connexion.
- Lenteur de la prise en main à distance via TighVNC.
  - Possibilté de changer les paramètres côté viewer (diminution de la qualité graphique) pour avoir moins de latence.
- Optimiser le code pour l'initialisation du script PowerShell.

### 6. Améliorations 

- Faire évoluer le script pour demander à l'utilisateur s'il souhaite personnaliser sa demande de connexion avec différents paramètres :
  - Affichage en plein écran ou non;
  - Résolution d'affichage;
  - Partage de dossiers entre les deux postes;
  - Autres possiblités.

- Voir comment mettre en place une connexion si les deux postes ne sont pas sur le même réseau.
  - Autre solution logiciel;
  - Utilisation d'un VPN;
  - Solution payante ou gratuite.


