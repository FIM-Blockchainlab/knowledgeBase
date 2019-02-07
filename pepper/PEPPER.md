# Pepper
Um eigene Programme zu erstellen
Choregraphe Software:
```
http://doc.aldebaran.com/2-8/dev/community_software.html#retrieving-software
```
Alles Mögliche nachschauen über *NAOqi*(Betriebssystem) und Pepper:
```
http://doc.aldebaran.com/2-8/index_dev_guide.html
```
Um zu sehen was Pepper sieht, links in der Mitte von *Robot view* auf *Video monitor* umstellen.

Um Choregraphe mit Pepper zu Verbinden, einfach oben links auf Connection: Connect to...
und dort die jeweilige IP-Adresse eingeben, die man von Pepper bekommt indem man kurz auf den On/Off Button drückt.

Damit Pepper beim programmieren nicht ständig auf die Umgebung reagiert während man Programme testet, einfach Autonomous Life deaktivieren. (Oben rechts: Knopf mit Herz, dann Knopf mit Sonne)

Wenn man von unten links Blöcke in die Mitte gezogen hat, sieht man eine Beschreibung sowie Einstellungen des Angeklickten Bausteins im *Inspector* unten rechts

Mit einem Doppelklick auf die Blöcke öffnet man _meistens_ das Fenster, in dem der Python-Code des Bausteins steht.

Um Bewegungsabläufe zu erstellen gibt es den *Animation Mode*. Dazu benutzt man den *Timeline* Block.
Wenn man Doppelklick auf _diesen_ Block macht öffnet sich ein neues Modul, welches in Frames eingeteilt ist. Dort ist es möglich jeden Frame (jede 25stel Sekunde) die Position der Gelenke anzupassen.

Die Körperteile kann man entweder in der *Robot view* rechts oben anklicken und bewegen, oder in dem Modul darunter (*Inspector*), wo sich bei anklicken ein Fenster mit Schiebeschaltern öffnet.

Pepper bewegt sich nicht wenn sich ein potenzielles Hindernis in ihrer Nähe befindet. Auch wenn die verschiedenen Positionen zu schnell aufeinander folgen (*Timeline*), kann das zu inkorrekter Ausführung der Bewegung führen.

Um eine selbstprogrammierte Website auf dem Tablet anzuzeigen, folgende Applikation herunterladen und mit Choregraphe ausführen:
```
https://github.com/kokorobot/pepper_samples
```

Man kann Choregraphe auch zweimal auf dem gleichen PC öffnen und dann beide Peppers mit einem Computer steuern.

Auf der Rückseite des Tabletts sind Knöpfe. 

Die Lautstärke kann man auf verschiedene Arten steuern:
1. Zu Pepper sagen: "launch settings"
2. Zu Pepper sagen: "Speak softer" ---> Tablet
3. Zu Pepper sagen: "Speak louder" ---> Tablet
4. Im Browser Peppers IP eingeben.
5. In Choregraphe oben rechts neben *autonoumus life* Button etc.

Um Programme aufzurufen oben links auf file ---> open project.
Bisherige Programme befinden sich auf dem Blockchain Laptop 2 ---> Pepper ---> Dokumente ---> Pepper Programme 
dort dann die .pml datei des Ordners des Programms welches man öffnen möchte auswählen.
Programme:
1. *AnimationMode*:
Programm welches Pepper den Arm ausstrecken lässt (ursprünglich für Geldscheinübergabe)
2. Animations1:
Gegenstück zu *AnimationMode* ---> muss einmal ausgeführt werden für richtige Ausgangsposition
3. Follow1.0:
Pepper versucht Menschen zu tracken und bewegt sich dann in Richtung der getrackten Person
4. tablet_sample:
Tablet von Pepper zeigt Website an, welche sich im Programm Ordner befindet (html ---> Index.html).
5. TheoryOfEverything:
Ein Programm welches mithilfe des choice-Blockes je nach Sprachbefehl Pepper etwas anderes machen lässt.

Um diesen choice-Block so verwenden zu können, muss man folgendes machen:
1. choice-Block ins Programm ziehen
2. Doppelklick auf Block machen
3. Dort den *Localized Text* Block löschen
4. OnStart von *Choice* mit Programm onStart oben links verbinden
5. In die Zeilen von *Choice* pro Zeile einen Sprachbefehl schreiben. (Der Block wird automatisch größer)
6. Dann alle Verbindungen zwischen der rechten Seite des Blockes und der linken Seite des Programms löschen
7. An der rechten Seite des Blockes sind nun unter dem Output mit dem Pfeil, genauso viele Outputs wie Befehle in den Zeilen. Bei 4 Befehlen also vier Outputs ohne Zeichen darauf und grau umrandet. Der erste ohne Pfeil ist auch der erste Befehl usw. Nun muss jeder dieser Outputs ohne Pfeil neu eingestellt werden: Rechtsklick auf Output ---> *Edit output*
8. In dem Fenster welches sich jetzt geöffnet hat unten den *Type* von *Dynamic* auf *"Bang"* umstellen und ok drücken. Der Output sollte nun nichtmehr Grau, sondern Schwarz sein. Dies mit allen Outputs wiederholen.
9. Nun rechts vom Fenster auf das blaue *+* drücken. Dort gibt man als Namen am besten den ersten Befehl ein und drückt ok. Dies für jeden Befehl wiederholen.
10. Nun *output 1* mit dem ersten Befehl rechts verbinden usw. So, dass der Output des ersten Befehls auch mit dem Output "erster Befehl" verbunden ist. 
11. Wenn alle Outputs richtig verbunden sind, mit einem Doppelklick irgendwo neben dem Block wieder in Hauptprogramm zurückkehren.
12. Dort kannst nun jeden Output des choice-Blockes mit dem Block verbinden, der aufgerufen werden soll, wenn der jeweilige Befehl wahrgenommen wurde.
13. Den choice-Block muss man natürlich noch mit dem Startpunkt des Programmes verbinden.
