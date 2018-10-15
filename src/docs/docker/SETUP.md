# Setup

- Iedereen Docker voor Desktop laten installeren.
https://docs.docker.com/engine/installation/#supported-platforms
- Specificaties van project opzoeken
Php versie
	Solr / Elastic / Geen
	Nginx / Apache
- docker-compose.yml file in de root aan het project toevoegen.
	https://github.com/wodby/docker4drupal
	https://docker4drupal.readthedocs.io/en/latest/
	Standaard steeds phpmyadmin en mailhog containers toevoegen.
phpmyadmin : Web interface voor database.
mailhog: Web interface om uitgestuurde mails te bekijken.
- docker-compose.yml moet mee in git komen.
deze moet steeds up-to-date gehouden worden met de live omgeving. Als hier een update gebeurd moet dit ook in de docker files gebeuren.
