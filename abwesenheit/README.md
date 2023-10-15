<p align="center"><a href="https://github.com/dawidjach/java/blob/master/abwesenheit/startdialog.png" target="_blank"><img src="startdialog.png" width="400" alt="dawidjach"></a></p>

## Automatische Konfiguration der Sieve-Anwendung zur Steuerung der OutOfOfficeMails

Das Ziel des Projekts ist die automatische Beantwortung von E-Mails bei Abwesenheit eines Mitarbeiters. Zur Erreichung dieses Ziels sind sowohl der Client "Abwesenheit" als auch das Programm "Sieve-Datei-Updater" erforderlich. Der Client "Abwesenheit" ist eine Desktop-Anwendung (Swing), die es dem Mitarbeiter ermöglicht, seine Abwesenheit (aufgrund von Urlaub oder Krankheit) sowie den Zeitraum der Abwesenheit zu erfassen und diese Informationen in der Datenbank zu speichern. Um das Projekt zu vereinfachen, sollte der Client ohne Anmeldeverwaltung entwickelt werden. Daher wird er nur auf dem PC der Personalabteilung installiert.

Das Programm "Sieve-Datei-Updater" soll auf dem Mailserver eingesetzt werden und in der Datenbank nach Datensätzen suchen, bei denen das heutige Datum innerhalb des Abwesenheitszeitraums liegt. Anschließend werden die Datensätze aus der Datenbank ausgelesen, und eine Sieve-Datei mit dem Abwesenheitstext bzw. Sieve-Skript wird erstellt. Die Ausführung des Programms wird zeitgesteuert durchgeführt, sodass der "Sieve-Datei-Updater" automatisch zu bestimmten Uhrzeiten ausgeführt wird (Cron-Datei). Diese Sieve-Skripte werden in den Mailservernutzernamen-Ordner (home/mailservenutzername) als Sieve-Dateien (dovecot.sieve) gespeichert.

![startdialogfenster](startdialogfenste.png)