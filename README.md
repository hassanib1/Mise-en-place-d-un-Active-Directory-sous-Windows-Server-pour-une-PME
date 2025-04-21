# Mise-en-place-d-un-Active-Directory-sous-Windows-Server-pour-une-PME
L'objectif de ce projet est de centraliser la gestion des utilisateurs, des groupes et des ressources sur un réseau Windows en utilisant Windows Server.
# Déploiement Active Directory 

Projet de mise en place d’un environnement Active Directory sous Windows Server, 
## 🏢 Contexte

une PME souhaite centraliser la gestion de ses utilisateurs, groupes et machines via un annuaire Active Directory pour améliorer la sécurité et l’administration du réseau.

## 🛠️ Technologies utilisées

- VMware Workstation
- Windows Server 2019
- Active Directory (AD DS)
- powershell

## 🧱 Architecture cible

- Nom du domaine : `reseau.local`
- Contrôleur de domaine : `SRV-AD`
- Utilisateurs : hassan.ibrahim, sndongo, jmbarga, atchouake
- Groupes : Informatique_Groupe, RH_Groupe, Comptabilite_Groupe, securite_Groupe

## ⚙️ Étapes principales

1. Création de la machine virtuelle serveur (RAM, disque, réseau)
2. Installation de Windows Server
3. Configuration IP statique et DNS
4. Installation du rôle Active Directory
5. Promotion du serveur en tant que contrôleur de domaine
6. Création d’utilisateurs et de groupes dans ADUC
8. Connexion avec un utilisateur de domaine

## 🔐 Exemple de vérification

```powershell
Get-ADUser -Identity hibrahim -Properties MemberOf | Select -ExpandProperty MemberOf

📂 Structure Active Directory
RESEAU.local
├── Utilisateurs
│   ├── hassan.ibrahim
│   ├── sndongo
│   └── jmbarga
└── Groupes
    ├── Informatique_Groupe
    ├── RH_Groupe
    └── Comptabilite_Groupe

👨‍💻 Auteur
Hassan Ibrahim – Étudiant en informatique, spécialisé en réseaux et sécurité.
