https://chatgpt.com/share/6713c6c1-c4f0-8013-b876-1b5c6e5a9bda

````
benutzername:verschlüsseltes-passwort:last-password-change:min-age:max-age:warn:inactive:expire:
````

Die Datei /etc/shadow ist eine zentrale Konfigurationsdatei in Unix- und Linux-Systemen, in der Passwörter und weitere sicherheitsrelevante Informationen über Benutzerkonten gespeichert werden. Sie ist nur für den Systemadministrator (root) lesbar und enthält verschlüsselte Passwörter sowie Informationen zu Passwortrichtlinien, wie z.B. Ablaufdaten.

Erklärung der Felder:

+ Benutzername: Der Name des Benutzers.
+ Verschlüsseltes Passwort: Das verschlüsselte Passwort des Benutzers. Wenn hier ein ! oder * steht, ist das Konto gesperrt oder das Passwort wurde nicht gesetzt.
+ Last Password Change: Das Datum der letzten Passwortänderung, gespeichert als Anzahl der Tage seit dem 1. Januar 1970.
 +   Min Age: Mindestanzahl von Tagen, die ein Benutzer warten muss, bevor er sein Passwort erneut ändern kann.
+  Max Age: Maximale Anzahl von Tagen, bevor der Benutzer sein Passwort ändern muss.
 +   Warn: Anzahl der Tage, bevor der Benutzer eine Warnung erhält, dass sein Passwort abläuft.
+  Inactive: Anzahl der Tage, an denen das Konto inaktiv wird, wenn das Passwort abgelaufen ist.
+   Expire: Datum, an dem das Benutzerkonto abläuft (in Tagen seit dem 1. Januar 1970).




## Verwaltung von Passwörtern

Passwörter können über den Befehl **passwd** verwaltet werden. Mit **passwd**  kann ein Benutzer sein Passwort ändern oder ein Administrator kann das Passwort eines anderen Benutzers setzen oder ändern. Häufige **passwd** Befehle:

+ Eigenes Passwort ändern:

```
passwd
```
+ Passwort eines anderen Benutzers ändern (nur als root möglich):

```
sudo passwd benutzername
```

+ Passwort eines Benutzers sperren (kein Login mehr möglich):
```
sudo passwd -l benutzername
```

+ Passwort eines Benutzers entsperren:
```
sudo passwd -u benutzername
```


```

```