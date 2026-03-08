🔐 Durcissement d’un serveur Debian avec Ansible (Apache + MariaDB + DVWA)
📌 Description
Ce projet propose un playbook d’automatisation avec Ansible permettant de sécuriser un serveur Debian hébergeant une application web.
L’environnement comprend :
  -Apache HTTP Server comme serveur web
  -MariaDB comme base de données
  -DVWA comme application de test
  
Le playbook applique plusieurs mesures de hardening afin de protéger le serveur contre des attaques courantes (brute force, mauvaises configurations, élévation de privilèges, exécution de commandes malveillantes).
Ce projet met en pratique :
  -l’administration système Linux
  -l’automatisation d’infrastructure
  -la sécurisation d’un serveur web
  -les bonnes pratiques de cybersécurité

⚙️ Fonctionnalités principales
🛠 Installation et outils de sécurité
Installation et configuration automatique de plusieurs outils :
  -pare-feu avec UFW
  -protection contre les attaques avec Fail2ban
  -surveillance d’intégrité avec AIDE
  -audit système avec Auditd
  -confinement d’applications avec AppArmor
  
🔐 Sécurisation des services
Le playbook applique plusieurs mesures de sécurité :
  -Apache : désactivation des informations serveur, activation d’en-têtes de sécurité et modules mod_security et mod_evasive.
  -SSH : changement du port par défaut, désactivation du login root et restriction par adresse IP.
  -Pare-feu : politique restrictive avec autorisation du trafic HTTP et SSH contrôlé.
  -Fail2ban : protection contre les attaques brute force sur SSH et Apache.
  -MariaDB : suppression des comptes anonymes, suppression de la base test et restriction de l’accès root
  -PHP : désactivation de fonctions dangereuses.

🏗 Architecture
Client
  |
Pare-feu (UFW)
  |
Apache Web Server
  |
DVWA
  |
MariaDB

🚀 Utilisation
.Cloner le projet
.Créer un dossier pour le playbook avec l'inventaire
.Exécuter le playbook : -ansible-playbook -i inventory linux-hardening.yml
⚠️ Avertissement

Ce projet est destiné à un environnement de laboratoire ou d’apprentissage.
DVWA est volontairement vulnérable et ne doit pas être exposé sur Internet.
