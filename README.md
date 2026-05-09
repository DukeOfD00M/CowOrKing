# CowOrKing
An add-on to Streamer.bot and OBS for Co-Working Streams, with ToDo-Lists, Work/Break-Timers etc.

# English version will follow soon

# Einrichtung
- Streamer bot Import
- html-Dateien in ein lokales Verzeichnis
- json und config Ordner in dasselbe Verzeichnis
- MANUELL: im OBS 5 Browser Sourcen in dieselbe Szene hinzufügen, als lokale Datei (wichtig!), je eine für die 5 html files (nicht umbenennen!)
- MANUELL: Im Streamer bot muss eine User-Gruppe "cok_user" angelegt werden (Links unten: Settings -> Groups -> Add Group).
- erst wenn die Objekte in den bot importiert wurden und die Browserquellen im OBS angelegt wurden, die beiden EXE im config Ordner ausführen
- Mit der ...config.exe werden wichtige Parameter, wie die Szene, der Dateipfad, die Dauer der Timer, und ein paar Einstellungen hinterlegt.
- Die meisten der Einstellungen können auch über !-Commands nachträglich geändert werden. In der Regel muss die EXE nur einmal laufen.
- mit der ...theme.exe werden Farben, Größen etc. hinterlegt. In der Regel muss auch diese EXE nur einmal laufen.
- Wenn OBS in der Kategorie Co-Working & Studying gestartet wird, während Streamer bot aktiv ist, wird automatisch eine Startup Action durchlaufen.
- Während des Startups werden alle Parameter aus den beiden EXEs als Globale Variablen hinterlegt, und abhängig davon die Szene vorbereitet.

# Commands für alle User
+ !add (text)[, (text), (text), ...]
+ !print (zeigt alle aktiven ToDos für den User an mit lfd Nr.)
+ !print all (zeigt alle ToDos incl. Status für den User an mit lfd Nr.)
+ !pause (text)|(lfd) (setzt aktives ToDo auf Status pause)
+ !cont (text)|(lfd) (setzt pausiertes ToDo auf Status added)
+ !done (text)|(lfd) (setzt ToDo auf Status ready)
+ !del (text)|(lfd) (löscht einzelnes ToDo)
+ !deldone (löscht alle ToDos die auf Status ready stehen)

# Commands für Stremaer/Mods
+ !setworkminutes (mm) (Setzt die Länge des Arbeitstimers)
+ !setbreakminutes (mm) (Setzt die Länge des Pausentimers)
+ !runworktimer (Setzt Timer auf "work" und startet den Timer)
+ !runbreaktimer (Setzt Timer auf "break" und startet den Timer)
+ !runtimer (Startet den aktuellen Timer)
+ !pausetimer (Pausiert den aktuellen Timer)
+ !resumetimer (Setzt pausierten Timer fort)
+ !stoptimer (Stoppt den aktuellen Timer und setrzt ihn zurück)
+ !setauto (True/False) (Soll Break Timer nach Work Timer automatisch starten und vice versa?)
+ !printdone (True/False) (Sollen erledigte ToDos im Widget erscheinen?)
