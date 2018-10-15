# Nieuwe site toevoegen

Om een nieuwe website toe te voegen zijn enkele stappen nodig :

## Project folder aanmaken.

Deze stap gebeurt als **district01** gebruiker. De code word vanuit een git repo uitgecheckt. Hiervoor moet wel eerst eenmalig de SSH public key van de server worden toegevoegd aan de deployment keys van de repository. Dit moet worden gevraagd aan een District01 BitBucket administrator. Deze kunnen deze kopiëren van een ander project of geef de uitvoer van `cat ~/.ssh/id_rsa.pub` door.

Zodra toegevoegd kan een project worden uitgecheckt vanop de server

```text
cd /var/www/district01
git clone git@bitbucket.org:district01/myproject.git myproject
```

Updates kunnen nadien dan eveneens als district01 gebruiker zonder wachtwoord gebeuren vanuit git \(pull, checkout, ...\).

## vhost aanmaken

Deze stap gebeurt als d01admin gebruiker. Maak een nieuwe vhost aan aan de hand van een template of bestaand project :

```text
sudo cp /etc/apache2/sites-available/template.conf
/etc/apache2/sites-available/myproject.conf
```

Vervang myproject door de echte projectnaam. Als ServerName mogen enkel subdomeinen worden gebruikt van d01-lindev.be of d01- lin-staging.be.

