# Supprimer le logo Pays de la Loire sur les pc HP Probook de la région

Comment supprimer le logo de la région Pays de la Loire au démarrage du PC fourni par la région


## Sommaire

- Prérequis

- Procédure de suppression
## Prérequis

- Avoir fait la procédure de désenrôlement fournie par la région en fin de scolarité
- Avoir accès au BIOS
- Avoir réinitialiser l'appareil afin d'avoir une session administrateur utilisable
## Procédure de suppression

Commencez par installer [Powershell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.4) sur votre appareil

Une fois l'installation faite, télécharger [HP Client Management Script Library (HP CMSL)](https://hpia.hpcloud.hp.com/downloads/cmsl/hp-cmsl-1.7.1.exe), lancer l'installeur et sélectionner bien l'emplacement Powershell s'il ne le choisit pas automatiquement

Lancez Powershell en mode administrateur et utilisez la commande suivante

```bash
  Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
```
Si un message vous prévenant d'une modification apparaît, tapez T et appuyez sur ENTRÉE

Enfin, utilisez ces commandes
```bash
  import-module hp.firmware
  Clear-HPFirmwareBootLogo
```
Redémarrez votre appareil et vous devriez voir le logo HP à la place de celui de la région Pays de la Loire
