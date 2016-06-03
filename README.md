# Ellis
Ellis ist eine browserbasierte Software zur Verwaltung von Startern, Ausschreibungen und Nennungen von Wettkämpfen beim Motorbootslalom bzw. Schlauchbootslalom (International: UIM Formula Future)

Inspiriert durch [das Nennungstool](http://nennung.lv-mbs.de/) und [Statistiktool](http://statistik.lv-mbs.de/) von Volker

## Warum der Name Ellis?
Die Software ist das Gegenstück zu [Alcatraz](https://github.com/Motorbootslalom/alcatraz), deshalb sollte sie auch einen Namen bekommen, welcher der Bezeichnung Alcatraz entgegen steht. [Ellis Island](https://de.wikipedia.org/wiki/Ellis_Island) ist eine Insel im Hafengebiet vor New York und war lange Zeit Sitz der Einreisebehörde und über 30 Jahre die zentrale Sammelstelle für Immigranten in die USA.


## Was soll das ganze Kosten?
Nichts...

Das Programm wird hier mit dem gesamten Quelltext als [freie Software](http://fsfe.org/about/basics/freesoftware.de.html) veröffentlicht.

In den meisten Landesverbänden wurden von fleißigen Helfern Programme für die Auswertung geschrieben und gehütet wie ein Staatsgeheimnis. Ich glaube nicht, dass das der richtige Weg ist. Ich glaube, es bringt mehr, wenn jeder seine Erfahrung mit einbringen kann um ein Stück Software zu schaffen,was jeder nutzen kann und auch nutzen möchte.
Gemeinsam kann man oft mehr erreichen.

## Worin soll Ellis geschrieben werden?
Das Backend soll in [go](https://golang.org/) und [swagger](https://swagger.io), das Frontend in [Angular](https://angular.io/) (nicht AngularJS) entstehen.

## Was soll Ellis alles können?
Hier nur eine grob sortierte Auflistung der meisten Ideen:


- [ ] Mindestens alles was aktuell schon mit beiden Seiten von Volker möglich ist 
- [ ] Nur via HTTPS erreichbar
- [ ] Jeder kann einen Zugang beantragen
  - [ ] Rechtemodel ist hierarchisch
    - Benutzer auf Bundesebene (vom DMYV) darf Mitglieder/Jugendwarte vom Landesverband, Benutzer auf Landesverband darf Mitglieder/Jugendwarte von Vereinen im jeweiligen Landesverband und Benutzer/Jugendwarte von Vereinen darf andere Mitglieder für den Verein freigeben.
    - [ ] Benutzer muss anhand der E-Mail von einem Dritten verifiziert werden
  - [ ] Es werden keine Benutzerdaten und Passwörter gespeichert
    - Es soll das [Identity Toolkit von Google](https://developers.google.com/identity/toolkit/) bzw. dessen Nachfolger [Firebase Authentication](https://firebase.google.com/docs/auth/) für die Authentifizierung verwendet werden
  - [ ] Wenn zu den Startern eine E-Mail-Adresse hinterlegt wurde, dann werden die Starter beim Antrag automatisch freigeschaltet und können Ihre eigenen Daten sehen und bearbeiten
  - [ ] Der Einstieg auf dieser Plattform muss so einfach wie möglich sein. Jeder neue Verein, der seine Nennung darüber machen möchte, sollte es können
- [ ] Mobilefirst - Alles muss auch via Handy problemlos möglich sein
- [ ] Benutzer können mehreren Vereinen bzw. Verbandsebenen angehören
  - Wechsel via Drop-Down-Auswahl
- [ ] Ausschreibungen können für verschiedene Vereine/Verbände freigegeben werden
  - [ ] E-Mail-Einladung zur Ausschreibung/Nennung mit E-Mail-Template
  - [ ] Favoriten, Gruppen für Vereinsauswahl?
- [ ] Kontaktliste von und für alle Jugendwarte
  - [ ] Jeder Jugendwart kann seine Daten selbst pflegen und entscheiden, was wie freigegeben wird
- [ ] Kontaktliste von und für alle Vereine
  - Name, Kurzform, Postanschrift, Vereinsanschrift, Vorsitz (Name, E-Mail und Telefonnummer), Jugendwart (Name, E-Mail und Telefonnummer)
- [ ] Ausschreibung/Nennung auch für Clubmeisterschaften
- [ ] Auswertungen können für die Statistik und Landesmeisterschaft importiert werden
  - [ ] Unbekannte Auswertungen werden zurückgestellt und an die Entwickler geschickt um einen Importer zu entwickeln
  - [ ] Alcatraz kann die Auswertung direkt zu Ellis exportieren
  - [ ] Ergebnisse werden möglichst lange archiviert
  - [ ] JavaScript-[Snippet](https://de.wikipedia.org/wiki/Snippet) für Ergebnisseiten auf der eigenen Homepage [altes Beispiel einer manuell gepflegten Seite](https://www.xn--mwejugend-07a.de/ergebnisse/)
    - [ ] Jeder Verein kann sich ein API Token generieren lassen und konfigurieren, wie die Ergebnisse dargestellt werden sollen
      - Nur Vorname, voller Name, abgekürzt, mit oder ohne inaktiven Starter, mit oder ohne Punkte usw.
