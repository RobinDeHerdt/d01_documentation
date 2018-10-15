# SSH Key toevoegen

Om niet telkens het wachtwoord te moeten ingeven kan elke ontwikkelaar zijn eigen SSH key toevoegen aan de district01 gebruiker. Hierdoor kan automatisch op basis van deze key worden aangemeld zonder wachtwoord.

## Kijk of er lokaal al een SSH key is gegenereerd en de public key bestaat.

```text
  ls -al ~/.ssh
```

Dit is het geval indien er al een bestand bestaat met een .pub extensie, standaard id\_rsa.pub, id\_dsa.pub, id\_ecdsa.pub of id\_ed25519.pub. Indien niet het geval moet een key worden aangemaakt.

```text
  ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Gebruik de standaard voorstellen voor locatie van de keys. Bij voorkeur ook een degelijk wachtwoord. Op linux en Mac zal ssh-agent deze onthouden.

## Kopieer de public key naar de server.

Dit kan manueel door op de remote server ~/.ssh/authorized keys te bewerken of eenvoudiger via ssh-copy-id.

```text
  ssh-copy-id district01@89.106.241.154
```

Geef dan éénmalig het wachtwoord op van de district01 gebruiker \(zie drive\). Op Mac is het mogelijk dat dit programma eerst moet worden geïnstalleerd.

```text
  brew install ssh-copy-id
```

## Test of je kan aanmelden zonder wachtwoord.

```text
  ssh district01@89.106.241.154
```

Herhaal eventueel voor d01admin.

