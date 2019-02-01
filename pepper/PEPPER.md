# Pepper
Um eigene Programme zu erstellen
Choregraphe Software:
```
http://doc.aldebaran.com/2-8/dev/community_software.html#retrieving-software
```
Alles Mögliche nachschauen über *NAOqi*(Betriebssystem) und Pepper:
```
http://doc.aldebaran.com/2-8/index_dev_guide.html
```#
Um zu sehen was Pepper sieht, links in der Mitte von *Robot view* auf *Video monitor* umstellen.

Um Choregraphe mit Pepper zu Verbinden, einfach oben links auf Connection: Connect to...
und dort die jeweilige IP-Adresse eingeben, die man von Pepper bekommt indem man kurz auf den On/Off Button drückt.

Damit Pepper beim programmieren nicht ständig auf die Umgebung reagiert während man Programme testet, einfach Autonomous Life deaktivieren. (Oben rechts: Knopf mit Herz, dann Knopf mit Sonne)

Wenn man von unten links Blöcke in die Mitte gezogen hat, sieht man eine Beschreibung sowie Einstellungen des Angeklickten Bausteins im *Inspector* unten rechts

Mit einem Doppelklick auf die Blöcke öffnet man _meistens_ das Fenster, in dem der Python-Code des Bausteins steht.

Um Bewegungsabläufe zu erstellen gibt es den *Animation Mode*. Dazu benutzt man den *Timeline* Block.
Wenn man Doppelklick auf _diesen_ Block macht öffnet sich ein neues Modul, welches in frames geteilt ist. Dort ist es möglich jeden Frame (jede 25stel Sekunde) die Position der Gelenke anzupassen.

Die Körperteile kann man entweder in der *Robot view* rechts oben anklicken und bewegen, oder in dem Modul darunter (*Inspector*), wo sich bei anklicken ein Fenster mit Schiebeschaltern öffnet.

Pepper bewegt sich nicht wenn sich ein potenzielles Hindernis in ihrer Nähe befindet. Auch wenn die verschiedenen Positionen zu schnell aufeinander folgen (*Timeline*), kann das zu inkorrekter Ausführung der Bewegung führen.

Um eine selbstprogrammierte Website auf dem Tablet anzuzeigen, folgende Applikation herunterladen und mit Choregraphe ausführen:
```
https://github.com/kokorobot/pepper_samples
```

Man kann Choregraphe auch zweimal auf dem gleichen PC öffnen und dann beide Peppers mit einem Computer steuern.

Auf der Rückseite des Tabletts sind Knöpfe. 

