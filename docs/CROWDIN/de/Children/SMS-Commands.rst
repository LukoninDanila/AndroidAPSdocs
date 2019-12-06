SMS-Befehle
*****
Sicherheitshinweise
======
* AndroidAPS erlaubt es Dir, das Smartphone eines Kindes über SMS-Nachricht aus der Ferne zu steuern. Wenn Du diesen SMS-Kommunikator aktivierst, denke immer daran, dass das Telefon, das für Remote-Befehle eingerichtet ist, gestohlen werden kann. Schütze dieses mit einem zumindest mit einem sicheren PIN-Code.
* AndroidAPS gibt Rückmeldung per SMS, wenn Deine Remote-Befehle, wie z.B. ein Bolus oder eine Profiländerung, ausgeführt wurden. Es ist ratsam, dies so einzustellen, dass Bestätigungstexte an mindestens zwei verschiedene Telefonnummern gesendet werden, falls eines der Empfangstelefone gestohlen wird.
* **Wenn Du einen Bolus über  SMS-Befehle abgibst, musst Du die Kohlenhydrate über Nightscout (NSClient, Webseite...) eingeben!** Wenn Du das unterlässt, ist zwar das IOB korrekt, aber die COB sind zu gering. Dies kann dazu führen, dass notwendige Korrekturboli nicht abgegeben werden, da AAPS davon ausgeht, dass Du zu viel aktives Insulin hast.

Funktionsweise
=====
* Die meisten Anpassungen der temporären Ziele, AAPS folgen etc. können über die `NSclient App <../Children/Children.html>`_ auf einem Android Smartphone durchgeführt werden.
* Boli können nicht über Nightscout abgegeben werden, aber Du kannst dafür SMS-Befehle verwenden.
* Falls Du als Follower ein iPhone verwendest und daher NSclient nicht nutzen kannst, gibt es weitere SMS-Befehle.

* Gehe dazu in den Systemeinstellungen deines Android-Telefons zu Apps > AndroidAPS > Berechtigungen und aktiviere dort SMS.
* In AndroidAPS gehst du zu Einstellungen > SMS-Kommunikator und trägst die Telefonnummer(n) ein, die dazu berechtigt werden soll(en), Kommandos an AndroidAPS zu senden, mehrere Nummern werden dabei durch Semikolon ohne Leerzeichen getrennt (z.B.  +4912345678;+4912345679). ‘Erlaube externe Befehle per SMS’ muss außerdem aktiviert werden.
* Wenn Du mehr als eine Nummer verwenden möchtest:

  * Gib nur eine der Telefonnummern ein.
  * Führe einen SMS-Befehl aus um sicher zu stellen, dass die Kommandos mit dieser Telefonnummer funktionieren.
  * Gib die zusätzliche(n) Telefonnummer(n) getrennt durch Semikolon ohne Leerzeichen ein.
  
    .. image:: ../images/SMSCommandsSetupSpace.png
      :alt: SMS-Befehle einrichten


* Sende von einer deiner zugelassenen Telefonnummern eine SMS auf das Handy, auf dem AndroidAPS läuft. Du kannst jeden der unten IN GROSSBUCHSTABEN aufgeführten Befehle verwenden. Das AndroidAPS-Handy bestätigt die erfolgreiche Ausführung des Befehls oder gibt den angefragten Status zurück. Bestätige gegebenenfalls das Kommando indem Du den vom AndroidAPS Smartphone per SMS übermittelten Code zurücksendest.

**Hinweis:** Eine SMS-Flat auf beiden Telefonen kann nützlich sein, da u.U. viele SMS hin und her gesandt werden.

Befehle
=====

Groß- und Kleinschreibung müssen beim Senden der Befehle nicht berücksichtigt werden.

Befehle müssen in Englisch gesendet werden, die Antwort erhältst Du in Deiner lokalen Sprache, wenn die Zeichenfolge bereits ` übersetzt ist <../translations.html##texte-fur-die-androidaps-app-ubersetzen> ` _.

.. image:: ../images/SMSCommands.png
  :alt: Beispiele für SMS-Befehle

Loop
-----
* LOOP STOP/DISABLE
   * Antwort: Loop wurde deaktiviert.
* LOOP START/ENABLE
   * Antwort: Loop wurde aktiviert
* LOOP-STATUS
   * Antwort hängt vom aktuellen Status ab
      * Loop ist deaktiviert.
      * Loop ist aktiviert.
      * Pausiert (%1$d min)
* LOOP SUSPEND 20
   * Antwort: Loop unterbrochen für 20 Minuten
* LOOP RESUME
   * Antwort: Loop wurde fortgesetzt

CGM-Daten
-----
* BZ
   * Antwort: Letzter BZ: 5.6 4min her, Delta: -0,2 mmol, IOB: 0.20U (Bolus: 0.10U Basal: 0.10U)
* CAL 5.6
   * Antwort: Um die Kalibrierung 5.6 zu senden, antworte mit dem Code Rrt.
   * Antwort, nachdem der korrekte Code von AAPS empfangen wurde: Kalibrierung gesendet (**Falls xDrip installiert ist. In xDrip+ muss "Kalibrierungen akzeptieren" aktiviert sein.)

Basal
-----
* BASAL STOP/CANCEL
   * Antwort: Antworte mit dem Code EmF, um die temporäre Basalrate zu beenden
* BASAL 0.3
   * Antwort: Um eine Basalrate von 0.3IE/h für 30 Minuten zu setzen, antworte mit dem Swe
* BASAL 0.3 20
   * Antwort: Um eine Basalrate von 0.3IE/h für 20 Minuten zu setzen, antworte mit dem Swe
* BASAL 30%
   * Antwort: Um die Basalrate von 30% für 30 Minuten zu setzen, antworte mit dem Code Swe
* BASAL 30% 50
   * Antwort: Um die Basalrate von 30% für 50 Minuten zu setzen, antworte mit dem Code Swe

Bolus
-----
Ein Bolus via SMS ist innerhalb von 15 Minuten nach der letzten Bolusgabe in AAPS oder nach dem letzten SMS-Befehl nicht möglich. Den Wert kannst Du nur anpassen, wenn mind. zwei Rufnummern eingetragen sind. Die Antwort hängt daher davon ab, wann der letzte Bolus abgegeben wurde.

* BOLUS 1.2
   * Antwort A: Um einen Bolus von 1,2 IE abzugeben, antworte mit dem Code Rrt
   * Antwort B: Bolusabgabe aus der Ferne nicht verfügbar. Versuch es später nochmal.
* BOLUS 0.60 MEAL
   * Mit dem optionalen Parameter MEAL wird ein Mahlzeiten TT gesetzt (Standardwerte sind 90 mg/dL / 5.0 mmol/L für 45 Minuten).
   * Antwort A: Um einen Bolus von 0,6 IE abzugeben, antworte mit dem Code Rrt
   * Antwort B: Bolusabgabe aus der Ferne nicht verfügbar. 
* CARBS 5
   * Antwort: Um 5g Kohlenhydrate um 12:45 einzugeben, antworte mit dem Code EmF
* CARBS 5 17:35/5:35PM
   * Antwort: Um 5g Kohlenhydrate um 17:35 einzugeben, antworte mit dem Code EmF
* EXTENDED STOP/CANCEL
   * Antwort: Antworte mit dem Code EmF, um den erweiterten Bolus zu beenden
* EXTENDED 2 120
   * Antwort: Um den erweiterten Bolus2 IE für 120 Minuten abzugeben, antworte mit dem Code EmF

Profile
-----
* PROFILE STATUS
   * Antwort: Profil1
* PROFILE LIST
   * Antwort: 1. ` Profil1 ` 2. ` Profil2 `
* PROFILE 1
   * Antwort: Um zum Profil 1 mit 100% zu wechseln, antworte mit Code Any
* PROFILE 2 30
   * Antwort: Um zum Profil 2 mit 30% zu wechseln, antworte mit Code Any

Andere
-----
* TREATMENTS REFRESH
   * Antwort: Behandlungen von NS aktualisieren
* NSCLIENT RESTART
   * Antwort: NSCLIENT RESTART 1 receivers
* PUMP
   * Antwort: Letzte Verbindung: vor 1 Min. Temp: 0.00E/h @11:38 5/30min IOB: 0.5E Reserv: 34E Batt: 100
* SMS DISABLE/STOP
   * Antwort: Um den SMS Remote Service zu deaktivieren, antworte mit dem Code Any. Beachte, dass Du die Fernsteuerung nur am AAPS Master-Smartphone wieder aktivieren kannst.
* TARGET MEAL/ACTIVITY/HYPO   
   * Antwort: Um ein MEAL/ACTIVITY/HYPO TT zu setzen, antworte mit dem Code Any.
* TARGET STOP/CANCEL   
   * Antwort: Um das temporäre Ziel zu stoppen, antworte mit dem Code Any
* HELP
   * Antwort: BG, LOOP, TREATMENTS, .....
* HELP BOLUS
   * Antwort: BOLUS 1.2 BOLUS 1.2 MEAL

Problembehandlung
=====
Es gab einen Hinweis, dass nach einem Update die SMS Kommandos auf einem Galaxy S10 nicht mehr funktioniert haben. Dies konnte durch Abschalten der Option 'als chat message senden' behoben werden.

.. image:: ../images/SMSdisableChat.png
  :alt: SMS als Chatnachricht deaktivieren
