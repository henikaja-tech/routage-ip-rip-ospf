# Étude et redistribution des protocoles de routage RIP v2 et OSPF

Projet de simulation réseau réalisé avec **GNS3**, portant sur la configuration, l'analyse et la redistribution de routes entre deux protocoles de routage dynamique : **RIP version 2** et **OSPF**.

## Contexte

Travail réalisé en groupe dans le cadre d'un cursus en administration système et réseau, sous la supervision de M. RAZAFINDRAMONJA Clément Aubert.

**Membres du groupe :**
- RATEFISON Yakin Ny Aina
- ANDRIANIRINA Henikaja David
- MIANDRISOA FANILOMANDRESY Orlando
- RAVALISON RABOANA Andoniaina Fenosoa

## Contenu du projet

### Domaine RIP v2 (routeurs R1 à R6)

- Configuration de chaque routeur et activation de RIP v2
- Analyse des tables de routage
- Étude du temps de convergence (jusqu'à 180 secondes après une panne)
- Observation des échanges de paquets RIP (UDP, port 520, adresse multicast 224.0.0.9)
- Simulation de panne : suppression de liaison et de routeur, analyse de la convergence

### Domaine OSPF (routeurs R7 à R9)

- Configuration des routeurs et activation des interfaces
- Analyse des paquets Hello (intervalle de 10 secondes)
- Détermination des Router-ID
- Tests de connectivité entre routeurs (ping)

### Redistribution de routes RIP ↔ OSPF

- Interconnexion des deux domaines via les routeurs R4 et R7
- Redistribution des routes RIP vers OSPF, puis OSPF vers RIP
- Résolution du problème de métrique par défaut empêchant la propagation des routes
- Validation finale : connectivité complète entre tous les routeurs des deux domaines

## Outils utilisés

- **GNS3** : simulation de la topologie réseau
- **Wireshark** : analyse des échanges de paquets RIP et OSPF
- Routeurs Cisco (simulés via Dynamips)

## Contenu du dépôt

- `RapportRoutageIP.pdf` → Rapport complet avec captures et analyses
- `ProjetRoutageIP/ProjetRoutageIP.gns3` → Fichier projet GNS3 (topologie complète)
- `ProjetRoutageIP/project-files/` → Fichiers de configuration de chaque routeur

## Consulter le projet

Le rapport complet (`RapportRoutageIP.pdf`) détaille toute la démarche, avec les configurations, les tables de routage et les analyses de paquets.

Pour rejouer la simulation, ouvrir `ProjetRoutageIP.gns3` avec GNS3.
