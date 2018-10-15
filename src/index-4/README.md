# Docker

![IMAGE](https://github.com/district01-drupal/d01_documentation/tree/3615f736dc3b8890a8f10f786fdfe51b44f1d915/src/docs/docker/assets/images/docker-logo.png)

In de oude traditionele opzet heb je zelf op je computer een apache, php, solr, varnish, … staan om zo te ontwikkelen. Hierbij vormt zich vaak het probleem dat deze versies verschillen voor de verschillende sites waarop je ontwikkeld. Wat dus wil zeggen dat hetgeen je lokaal hebt staan niet altijd overeenkomt met wat er op de live site staat en dit zorgt voor problemen.

Hier brengt Docker een oplossing. Docker gebruikt het concept van containers, dit wil zeggen dat in plaats van alles \(php, solr, …\) op één plaats te installeren \(je eigen computer\), gaat docker voor alles wat je nodig hebt een aparte container maken. Deze containers kunnen op elk moment verwijderd worden en terug op exact dezelfde manier gebouwd worden. Concreet wil dit zeggen dat je lokaal niets meer nodig heb om te kunnen werken op een project. Als je een project start kan je gewoon de containers builden en beginnen werken. Ben je klaar kan je de containers verwijderen en volgende keer je terug op het project moet werken terug herbouwen.

De containers worden opgebouwd via een configuratie file **docker-compose.yml** hierin staat gedefineerd hoe de containers eruit moeten zien. Deze file steekt bij in de repo zodat elke developer steeds de laatste versie van de containers heeft. Zo zijn we zeker dat elke developer op dezelfde php versie werkt, dezelfde solr heeft draaien, … . Indien een developer een container toevoegd en configureerd heeft ineens heel het team dat op de site werkt ook deze container beschikbaar.

Meer over de configuratie van de docker-compose.yml volgt later in het document.

