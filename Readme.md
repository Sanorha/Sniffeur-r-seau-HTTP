# Sniffeur HTTP (Python)

Ce projet est un **sniffeur réseau HTTP** développé en Python à l'aide de la bibliothèque **Scapy**. Il permet d'intercepter et d'afficher les requêtes HTTP en clair circulant sur une interface réseau donnée.

## 🎯 **Objectif du projet**  
- Apprendre à utiliser Scapy pour capturer et analyser le trafic réseau.
- Comprendre comment fonctionnent les requêtes HTTP non chiffrées.
- Développer un outil de base en cybersécurité pour l'analyse réseau.

Ce script est destiné à des fins pédagogiques et ne doit être utilisé que dans un environnement réseau personnel ou autorisé.

## 📜 **Description du script**  
Le sniffeur fonctionne de la manière suivante :  
1. Il prend en argument une interface réseau (par exemple `eth0`, `wlan0`, etc.).  
2. Il capture les paquets HTTP transitant sur cette interface.  
3. Lorsqu'un paquet HTTP contenant des données est intercepté, l'outil affiche l'URL visée ainsi que le contenu brut de la requête.

### Fonctionnalités
- **Sniffing en temps réel** du trafic HTTP.
- **Affichage de l'URL** complète (host + path).
- **Affichage du contenu brut** transmis dans la requête (formulaires, cookies, etc. si transmis en clair).

## ▶️ **Exemple d'utilisation**
```bash
$ sudo python3 sniff_http.py -iface wlan0
b'www.example.com/index.html' : b'username=admin&password=1234'
```
## 🧠 Pourquoi ce projet ?
Ce projet m’a permis de découvrir :

- La capture de paquets en temps réel avec Scapy.

- La manipulation de protocoles réseau comme HTTP.

- Les risques liés à la transmission de données sensibles en HTTP non sécurisé.

Améliorations possibles :
- Ajouter un filtrage plus précis (GET/POST, ports, etc.).

- Sauvegarder les données interceptées dans un fichier log.

- Étendre le support à d'autres protocoles (FTP, DNS...).

- Détection automatique des interfaces actives.

## ⚠️ Avertissement

> Ce script est **strictement éducatif**. Il ne doit en aucun cas être utilisé pour tenter de déchiffrer des mots de passe réels ou accéder à des systèmes sans autorisation.

---

📁 Projet réalisé dans le cadre de ma candidature à une formation en cybersécurité.  
