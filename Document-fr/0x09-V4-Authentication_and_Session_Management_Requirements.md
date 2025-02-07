# V4: Exigences Concernant l'Authentification et la Gestion des Sessions

## Objectif de Contrôle

Dans la plupart des cas, la connexion des utilisateurs à un service distant doit être appréhendée au niveau de l'architecture générale des applications mobiles. Même si la majorité de la logique se passe sur le point terminal, le MASVS définit des exigences de base concernant la manière de gérer les comptes et les sessions des utilisateurs.

## Exigences pour la Validation de la Sécurité

| # | MSTG-ID | Description || L2 |
| --- | --- | --- | --- | --- |
| **4.1** | MSTG‑AUTH‑1 | Si l'application donne accès aux utilisateurs à un service distant, un certain niveau d'authentification, tel que l'authentification par nom d'utilisateur / mot de passe, est faite sur le point terminal distant. | ✓ | ✓ |
| **4.2** | MSTG‑AUTH‑2 | Si des sessions avec état sont utilisées, le point terminal distant utilise des identifiants de session aléatoirement générés pour authentifier les requêtes des clients sans avoir à envoyer les références des utilisateurs.  | ✓ | ✓ |
| **4.3** | MSTG‑AUTH‑3 | Si l'authentification sans état basée sur des jetons est utilisée, le serveur fournit des jetons qui ont été signés par un algorithme à la sécurité éprouvée. | ✓ | ✓ |
| **4.4** | MSTG‑AUTH‑4 | Le point terminal distant met fin à la session existante lorsque l'utilisateur se déconnecte. | ✓ | ✓ |
| **4.5** | MSTG‑AUTH‑5 | Une politique de mot de passe existe et est appliquée sur le point terminal distant. | ✓ | ✓ |
| **4.6** | MSTG‑AUTH‑6 | Le point terminal distant implémente un mécanisme permettant la protection contre les essais répétés de références utilisateurs. | ✓ | ✓ |
| **4.7** | MSTG‑AUTH‑7 | Les sessions sont dévalidées sur le point terminal distant après une période d'inactivité donnée et les jetons d'accès associés expirent. | ✓ | ✓ |
| **4.8** | MSTG‑AUTH‑8 | L'authentification biométrique, lorsqu'elle est utilisée, n'est pas basée sur des évènements (c'est-à-dire l'utilisation d'une API qui retourne simplement "vrai" ou "faux"). A la place, son utilisation est basée sur le déverrouillage du trousseau d'accès / du magasin de clé (keychain / keystore). |   | ✓ |
| **4.9** | MSTG‑AUTH‑9 | Un second facteur d'authentification est disponible sur le point terminal distant et l'exigence d'authentification à deux facteurs est mise en application de façon systématique.  |   | ✓ |
| **4.10** | MSTG‑AUTH‑10 | Les transactions sensibles requièrent une authentification améliorée.  |   | ✓ |
| **4.11** | MSTG‑AUTH‑11 | L'application informe les utilisateurs de toutes les connexions sur leurs comptes. Les utilisateurs ont accès à la liste des appareils utilisés pour accéder à leurs comptes et peuvent en bloquer. |  | ✓ |

<br/>

## Références

Le Mobile Security Testing Guide de l'OWASP (guide de test de la Sécurité mobile) fournit des instructions détaillées pour valider les exigences listées dans cette section.

- General - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x04e-Testing-Authentication-and-Session-Management.md>
- Pour Android - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05f-Testing-Local-Authentication.md>
- Pour iOS - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06f-Testing-Local-Authentication.md>

Pour de plus amples informations, il est possible de consulter aussi :

- OWASP Mobile Top 10: M4 (Authentification Non-Sécurisée) - <https://www.owasp.org/index.php/Mobile_Top_10_2016-M4-Insecure_Authentication>
- OWASP Mobile Top 10: M6 (Autorisation Non-Sécurisée) - <https://www.owasp.org/index.php/Mobile_Top_10_2016-M6-Insecure_Authorization>
- CWE 287 (Improper Authentication)- <https://cwe.mitre.org/data/definitions/287.html>
