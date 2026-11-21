# TP 4 – Du CSPM au CWPP

## Q1
Microsoft Defender for Storage a été activé sur le compte cwppmg2026 avec l'analyse des maliciels au chargement. La limite utilisée était de 10 Go/mois au lieu de 1 Go demandé.

## Q2
Activer la protection sur une seule ressource permet de contrôler les coûts et d'éviter la facturation des autres comptes. Dans une PME, une protection au niveau de l'abonnement peut être envisagée après une évaluation des besoins et du budget.

## Q3
Le fichier facture-fournisseur.txt contenant le test EICAR a été détecté comme Malicious dans les balises du blob. Le résultat du fichier sain n'a pas été confirmé.

## Q4 – Alerte de sécurité
- Titre : non relevé
- Gravité : non relevée
- Ressource : cwppmg2026 (compte analysé)
- Heure : non relevée
- Tactique MITRE : non relevée
- Actions recommandées : non relevées

## Q5
L'analyse du fichier a été effectuée rapidement. Le délai exact entre le téléversement et l'alerte n'a pas été relevé. Pour une PME, une détection rapide est importante afin de limiter l'exposition des employés.

## Q6
Je contacterais le fournisseur pour lui demander de vérifier son ordinateur et je mettrais en place une procédure automatique de quarantaine et de notification.

## Q7
MITRE ATT&CK T1080 – Taint Shared Content. Cette technique consiste à placer ou modifier du contenu dans un espace partagé pour compromettre les personnes qui l'utilisent. Elle correspond au dépôt d'un fichier malveillant dans le conteneur partagé.

Source : https://attack.mitre.org/techniques/T1080/

## Q8
Les fichiers malveillants transmis par courriel ou par des services de partage peuvent menacer les entreprises. Les employés qui reçoivent des documents externes sont particulièrement exposés. Defender for Storage peut analyser les fichiers déposés dans Azure, mais ne protège pas directement les boîtes courriel.

Source de référence : https://www.cyber.gc.ca/en/guidance/spotting-malicious-email-messages-itsap00100

## Q9
La détection par signature peut manquer les nouveaux maliciels ou ceux qui ont été modifiés pour éviter les signatures connues.

## Q10 – Comparaison

| Critère | Defender for Storage | ClamAV |
|---|---|---|
| Protection | Stockage Azure | Fichiers analysés |
| Détection | Analyse au chargement, alertes | Signatures antivirus |
| Coût | Payant | Logiciel libre |
| Entretien | Faible | Mises à jour et configuration |
| Azure | Intégration native | Intégration personnalisée |
| Compétences | Azure et sécurité | Administration système et scripts |

## Q11 – Recommandation

À la direction,

Je recommande d'utiliser Microsoft Defender for Storage pour protéger le compte Azure dans lequel les fournisseurs déposent leurs factures.

Notre PME compte 25 employés et dispose d'un seul technicien informatique. Il est donc important de choisir une solution simple à gérer, qui demande peu d'entretien et qui permet de détecter rapidement les fichiers suspects. Defender for Storage répond à ces besoins grâce à son intégration native avec Azure.

Lors de notre expérience, le fichier de test EICAR a été détecté comme malveillant. Ce résultat montre que le service peut identifier un fichier connu comme dangereux lors de son dépôt dans le stockage.

Je recommande d'activer cette protection uniquement sur les comptes qui reçoivent des documents externes. Il faudra aussi définir un budget et surveiller les frais de protection.

ClamAV constitue une solution libre intéressante, mais son intégration avec Azure nécessite davantage de configuration, de maintenance et de compétences techniques. Avec un seul technicien, cette charge supplémentaire pourrait être difficile à gérer.

Enfin, Defender for Storage ne garantit pas la détection de toutes les menaces. Il faudra également contrôler les accès, prévoir une procédure de quarantaine et sensibiliser les fournisseurs aux risques.

## Q12
Le groupe de ressources rg-cwpp-mg a été supprimé avec succès dans Azure. Cette suppression a également retiré le compte de stockage utilisé pour le TP.

## Captures
Les captures Q1, Q3 et Q12 doivent être ajoutées dans ce dossier GitHub.

## Sources
- Microsoft Learn : https://learn.microsoft.com/azure/defender-for-cloud/defender-for-storage-introduction
- ClamAV : https://docs.clamav.net/
- MITRE ATT&CK : https://attack.mitre.org/techniques/T1080/
- Centre canadien pour la cybersécurité : https://www.cyber.gc.ca/en/guidance/spotting-malicious-email-messages-itsap00100

Consultation : 20 novembre 2026.
