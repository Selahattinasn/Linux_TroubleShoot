### how to remove files lder than 7 day by creating a cron job?

### Command zum finden und löschen

_for that we use  *find* coomand_
````
find /var/log/security -type f -mtime +7 -exec rm -rf {} \; 
````

Parameter im Befehl:

    /var/log/security:
        Dies gibt das Verzeichnis an, in dem nach Dateien gesucht werden soll. In diesem Fall ist es das Verzeichnis /var/log/security, das oft sicherheitsbezogene Logs enthält.

    -type f:
        Dieser Parameter gibt an, dass nur nach Dateien (f für "file") gesucht wird. Verzeichnisse werden ignoriert.

    -mtime +7:
        -mtime steht für "modification time", also das Datum der letzten Änderung einer Datei.
        +7 bedeutet, dass nur Dateien berücksichtigt werden, deren letzte Änderung mehr als 7 Tage zurückliegt. Der + bedeutet "älter als". Würde man -7 schreiben, würde es Dateien auswählen, die vor genau 7 Tagen geändert wurden, und 7 würde Dateien wählen, die innerhalb der letzten 7 Tage geändert wurden.

    -exec:
        Dies ist der Teil, der eine Aktion auf die gefundenen Dateien ausführt. In diesem Fall wird der Befehl rm -rf auf jede gefundene Datei angewendet.

    rm -rf {}:
        rm steht für "remove" und löscht Dateien.
        -r (rekursiv) bedeutet, dass das Löschen auch rekursiv für Verzeichnisse und deren Inhalt gilt. Hier wird es jedoch nur für Dateien verwendet, daher spielt das rekursive Löschen keine Rolle.
        -f bedeutet "force", also erzwingt das Löschen ohne Nachfrage oder Warnungen, auch wenn die Datei schreibgeschützt ist.
        {} ist ein Platzhalter, der durch den Pfad der gefundenen Datei ersetzt wird. Jedes Mal, wenn eine Datei gefunden wird, wird ihr Pfad an dieser Stelle eingesetzt.

    \;:
        Dieser Teil markiert das Ende des -exec-Befehls. Der Befehl find verwendet \; als Abschluss des durch -exec ausgeführten Kommandos.



#### Cronjob command 

´´´´

´´´´
