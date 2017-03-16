# kata-invoice-reminder
kata sur la relance de facture. Inspiré du "birthday greetings" kata

# But
Vous devez implémenter un programme servant à notifier les débiteur qu'ils ont une facture à payer.

# Description des données

Chaque ligne correspond à une facture à payer.

les dates sont au format: D12M08Y2017 = le 12 Aout 2017
le "due date" correspond à la date d'échéance de la facture: date à laquelle elle doit avoir été payée
le "payment date" correspond à la date à laquelle la facture a été payée
le contact est la personne à contacter concernant cette facture.
le "price" est le prix, en centime d'euros.

# Règles métier

* 10 jours avanrt la date d'échéance d'une facture, le débiteur est notifié par un mail pour le prévenir de la date d'échéance.
* une fois la date d'échéance passée, si la facture n'est toujours pas payée, on le relance chaque mois au même jours.
* Règle spéciale: Si le même jours n'existe pas (ex: le 31 pour certains mois), on notifie le dernier jours du mois (par exemples le 30, ou le 28/29 pour février).

