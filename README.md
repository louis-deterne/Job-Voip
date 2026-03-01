# Projet VoIP - Infrastructure Asterisk 22

Ce projet consiste en la mise en place d'une architecture de téléphonie sur IP complète sur Debian, incluant l'automatisation de la gestion des utilisateurs et un serveur vocal interactif (IVR).

## Fonctionnalités
- **Serveur VoIP** : Basé sur Asterisk 22 LTS avec le module PJSIP.
- **Automate (IVR)** : Menu interactif (Tapez 1 pour le service Compte, 2 pour les RH).
- **Gestion Dynamique** : Script Python pour importer des utilisateurs depuis un fichier CSV.
- **Sécurité** : Messageries vocales protégées et gestion des horaires (DND).
- **Supervision** : Monitoring des performances du serveur[cite: 65].

## Structure du Projet
- `asterisk-config/` : Contient la logique du Dialplan et la configuration des Endpoints.
- `scripts/` : Automatisation du provisionnement des utilisateurs.
- `docs/screenshots/` : Preuves de fonctionnement (appels réussis, logs console).

## Installation & Tests
1. **Prérequis** : Machine virtuelle Debian, Asterisk 22.
2. **Configuration** : Importer les fichiers du dossier `asterisk-config/` dans `/etc/asterisk/`.
3. **Automatisation** : Lancer `python3 scripts/generate_voip.py` pour charger les utilisateurs du CSV.
4. **Validation** : Utiliser le plan de test détaillé dans le rapport pour vérifier les fonctionnalités critiques.

## Documentation
Le rapport détaillé incluant la veille technologique, les avantages/inconvénients de la solution et les exemples d'implémentation est disponible dans le dossier `docs/`.
