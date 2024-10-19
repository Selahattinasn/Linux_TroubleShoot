
````
johndoe:x:1000:1000:John Doe:/home/johndoe:/bin/bash
````
#### Bedeutung der Felder in diesem Beispiel:
+ Benutzername: johndoe
+ Passwort: x (Verweis auf /etc/shadow)
+ Benutzer-ID (UID): 1000
+ Gruppen-ID (GID): 1000
+ GECOS: John Doe
+ Home-Verzeichnis: /home/johndoe
+ Shell: /bin/bash


Jede Zeile in der Datei beschreibt einen Benutzer und besteht aus sieben durch Doppelpunkte (:) getrennten Feldern:

    Benutzername (Login-Name):
        Das erste Feld enthält den Namen des Benutzers, mit dem sich der Benutzer am System anmeldet. Dieser Name ist einzigartig für jeden Benutzer und darf keine Leerzeichen enthalten.
        Beispiel: johndoe

    Passwort (Verschlüsselt oder Platzhalter):
        Früher enthielt dieses Feld das verschlüsselte Passwort des Benutzers. Heute ist es meist mit einem Platzhalter x belegt, da die eigentlichen verschlüsselten Passwörter aus Sicherheitsgründen in der Datei /etc/shadow gespeichert werden.
        Beispiel: x

    Benutzer-ID (UID):
        Dies ist die eindeutige numerische Kennung des Benutzers. Jeder Benutzer hat eine eigene UID.
        Beispiel: 1000

    Gruppen-ID (GID):
        Dieses Feld enthält die numerische Kennung der Hauptgruppe, der der Benutzer angehört. Diese Gruppe ist in der Datei /etc/group definiert.
        Beispiel: 1000

    Benutzerinformationen (GECOS):
        Das fünfte Feld enthält optionale Informationen über den Benutzer, wie z. B. den echten Namen, die Telefonnummer oder andere Details. Traditionell wird dieses Feld als „GECOS-Feld“ bezeichnet, das in der Regel durch Kommata getrennt ist. Diese Informationen werden häufig von Programmen wie Mail oder finger verwendet.
        Beispiel: John Doe

    Home-Verzeichnis:
        Dieses Feld gibt das Verzeichnis an, in dem sich das persönliche Verzeichnis des Benutzers befindet. Es ist der Ort, an dem der Benutzer standardmäßig nach der Anmeldung landet.
        Beispiel: /home/johndoe

    Shell:
        Hier wird die Standard-Shell des Benutzers angegeben, also das Programm, das gestartet wird, wenn sich der Benutzer anmeldet. Die am häufigsten verwendeten Shells sind /bin/bash, /bin/sh oder /bin/zsh.
        Beispiel: /bin/bash