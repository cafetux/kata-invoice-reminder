# kata-invoice-reminder
kata sur la relance de facture. Inspiré du "birthday greetings" kata

# But
Vous devez implémenter un programme permettant de charger les données de facturation, et qui pourra notifier les débiteur qu'ils ont une facture à payer.


# Description des données

Chaque ligne correspond à une facture à payer.

les dates sont au format: D12M08Y2017 = le 12 Aout 2017

le "due date" correspond à la date d'échéance de la facture: date à laquelle elle doit avoir été payée

le "payment date" correspond à la date à laquelle la facture a été payée

le contact est la personne à contacter.

le "price" est le prix, en centime d'euros.

# Règles métier

* 10 jours avanrt la date d'échéance d'une facture, le débiteur est notifié par un mail pour le prévenir de la date d'échéance.
* une fois la date d'échéance passée, si la facture n'est toujours pas payée, on le relance chaque mois au même jours.
* Règle spéciale: Si le même jours n'existe pas (ex: le 31 pour certains mois), on notifie le dernier jours du mois (par exemples le 30, ou le 28/29 pour février).


# Format de l'email
le mail pré-échéance sera au format:

```
Subject: Votre Facture n° 12EDF432
Bonjour Doe John,
Nous attendons votre réglement de 23.00€ pour le 12/02/2017

Cordialement,
Le Service Facturation
```

le mail de relance sera au format:

```
Subject: Relance pour votre Facture n° 12EDF432
Bonjour Doe John,
Sauf erreur ou omission de notre part, le paiement de la facture n° 12EDF432 datée du 12/02/2017 pour un montant de 23.00 euros, et arrivée à échéance le 12/02/2017, ne nous est pas parvenu. 

Vous remerciant de faire le nécessaire,
Le Service Juridique
```






