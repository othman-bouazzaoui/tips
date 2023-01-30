<b>une expression cron</b> : c'est une manière de définir la fréquence d'exécution d'une tâche(script, traitement ...)<br>
astuce de préference qu'on la lire de droit vers la gauche :)

Se compose de 6 arguments spéarer par un espace :
- arg 1 : seconde(0 or 1-59) (exemple (*) * * * * * => execution chaque seconde)
- arg 2 : minute(0 or 1-59) (exemple 0 (*) * * * * => chaque minute)
- arg 3 : hour(0 or 1-23) (0 0 (*) * * * => chaque heure)
- arg 4 : day of month(1-31) (0 0 0 (*) * * => chaque jour à minuit)
- arg 5 : month (0 0 0 1 (*) * => chaque premier jour du mois) <br>
      day of week (0 0 0 1 1 * => chaque premier jour du premier mois(janvier) à minuit)
- arg 6 : day of week (0 0 0 1 1 (1) => chaque lundi du premier jour du mois(janvier) à minuit)

NB : pour les cas du 2 à 6 on peut enlever le premier arg des secondes, si on a pas besoin de spécifier à quelle seconde on doit executer notre traitement (exemple 10 0 0 * * * => chaque jour à 00:00:10)

[crontab](https://crontab.cronhub.io/)
>> tableau cron :
<table style="border: 1px solid rgb(233, 228, 247);border-collapse: collapse; border-spacing: 0px; font-size: 12px;"><thead><tr><th>*</th><th>*</th><th>*</th><th>*</th><th>*</th></tr></thead><tbody><tr><td>minute (0-59)</td><td>hour (0 - 23)</td><td>day of the month (1 - 31)</td><td>month (1 - 12)</td><td>day of the week (0 - 6)</td></tr></tbody></table>


>> exemples :
<table><thead><tr><th>Cron expression</th><th>Schedule</th></tr></thead><tbody><tr><td>* * * * *</td><td>Every minute</td></tr><tr><td>0 * * * *</td><td>Every hour</td></tr><tr><td>0 0 * * *	</td><td>Every day at 12:00 AM</td></tr><tr><td>0 0 * * FRI</td><td>At 12:00 AM, only on Friday</td></tr><tr><td>0 0 1 * *</td><td>At 12:00 AM, on day 1 of the month</td></tr></tbody></table>