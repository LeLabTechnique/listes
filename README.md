# Listes du Lab Technique

Données ouvertes tirées du **pot de miel** de [lelabtechnique.fr](https://lelabtechnique.fr) : un faux serveur, volontairement exposé sur Internet, qui imite une petite entreprise mal protégée et enregistre ce que font les attaquants. Mises à jour **chaque jour, automatiquement**.

| Fichier | Contenu |
|---|---|
| `blocage/lelab-blocage.txt` | Adresses IP qui ont **attaqué** le pot de miel ces 7 derniers jours (commande tapée, exploit, vol de secrets, action sur une fausse base, ou au moins 5 essais de mot de passe). Un simple balayage ne suffit pas. |
| `blocage/lelab-blocage.nft` | La même liste en jeu **nftables** : `nft -f lelab-blocage.nft` |
| `blocage/lelab-blocage.csv` | Détail : nombre d'événements, premier et dernier jour vus, catégories. |
| `mots-de-passe/mots-de-passe-robots.txt` | Mots de passe réellement essayés par les robots sur le faux SSH/Telnet, vus depuis **au moins 3 machines différentes**, du plus au moins répandu. |
| `mots-de-passe/mots-de-passe-interdits-entra.txt` | 1 000 termes prêts pour la liste de mots de passe interdits de **Microsoft Entra ID** (4 à 16 caractères). |

Outils en ligne : [liste de blocage](https://lelabtechnique.fr/outils/liste-de-blocage/) · [votre mot de passe est-il connu des robots ?](https://lelabtechnique.fr/outils/mot-de-passe/)

## Précautions

- Fournies **telles quelles**, sans garantie. Gardez toujours vos propres adresses d'administration en exception.
- Une adresse partagée (box, VPN, nuage) peut passer à un utilisateur légitime : la liste de blocage ne garde que 7 jours.
- Les appâts du pot de miel (faux identifiants qu'il distribue) sont **exclus** des listes de mots de passe ; un mot de passe vu depuis une seule machine n'est jamais publié (ce pourrait être le vrai mot de passe d'une personne).
- Erreur à signaler : https://lelabtechnique.fr/contact/

## Licence

Données sous licence [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.fr) : réutilisation libre, y compris commerciale, en citant « Le Lab Technique (lelabtechnique.fr) ».

---

*English: daily-updated open data from the lelabtechnique.fr honeypot. `blocage/` = IPs that actually attacked it in the last 7 days (txt, nftables, csv); `mots-de-passe/` = passwords tried by bots (seen from at least 3 sources) and a 1,000-term Microsoft Entra ID banned-password list. CC BY 4.0.*
