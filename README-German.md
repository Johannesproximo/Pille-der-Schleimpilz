README: German/[English](README.md)

#Pille der Schleimpilz

Hier sieht man einen Wachstumsverlauf des Pilzes Pille

![Pille G](Pictures/pille.jpg)

###Allgemein:
Pille der Schleimpilz (Physarum polycephalum)ist ein Projekt in dem wir versuchen das Wachstum (Form, Farbe) des Pilzes zu beeinflussen und somit Zeichen entstehen zu lassen und dies in einem Zeitraffer festzuhalten. Danach bearbeiten wir diese Video mit Processing, OpenCV und bereiten die Entstehung visuel auf.


**1. Erste Experimentiere mit Pille dem Schleimpilz:**
	
- Der Pilz wächst in Warmen Temperaturen von über 20 grad und dunkler Umgebung gut.  
(Er soll ja bei optimalen bedingungen 1cm pro Stunden wachsen können.)  
- Versuch wachstum zu Steuern.  
(Ich habe ihn mit Haverflocken gelockt allerdings ist die Richtung bis jetzt nicht vorhersehbar und gezieltes wachsen nicht möglich. Vielleicht ist der Närboden schon ein starker einfluss für den Pilz)
-  Versuch den Pilz zu färben
(Er hat die Farbe der Roten bette leider nicht angenommen)  
-  Habe hin und wieder destiliertes Wasser zugegeben um ihn vor dem Ausdrocknen zu schützen.

![Erste Versuche](Pictures/first_try.jpg)

**2. Pille Bekommt einen Bruder und wird Shootingstar:**

-  Es werden Gläser mit destilierten Wasser abgekocht und versucht den Pilz erneut anzusetzten.  
(In bis zu 3 Gläsern)
- Erste Versuche mit dem Rassberry Pi (super Cool) werden unternommen und versucht die Camera zu installieren.
- Nach großen problemen entstehen erste unscharfe Bilder.
- Der Focus der Pi Camera muss Händisch eingestellt werden.
- Die Pille Brothers wurden mit unterschiedlichem Licht beleuchtet (RGB LED)

![Erste Versuche](Pictures/pille-brothers.jpg)

**3. Pille kommt ins Fotolabor, versuch einer Spiegelfreien Aufnahme mit DSLR CANON 500D**

- Mein Kamerablitz wird eine 60 Watt Lampe. Geschaltet wird die Lampe mit einem Relay und dem Raspberry Pi.
- Eine Kiste wird zum Aufnahmestudio. Der Ort ist eine Dunkle Warme stelle unter der Decke in unserer Abstellkammer.
- Das Einstellen ist äußerst umständlich da ich schlecht an die DSLR Herankomme. (Daher sollte man von anfang an an einer Kompackten gut zugänglichen Lösung arbeiten...)
- Unentliche Spiegelungen durch die Lampe erschwären die Aufnahme und ich versuche die mit Schwarzen Karton diese zu reduzieren. Dafür wurde auch der Dekel der Pedrischahle entfernt welches den Nährboden ausdrocknen läst ...  
 (es empielt sich die Beleuchtung von der Seite einzubauen so werden reflektionen reduziert)
- Es kam nie zu einem dauerhaften soliden Aufnahme.

![Versuchsaufbau und Spiegelung](Pictures/Box-DSLR.jpg)

###Benötigt:

[Raspberry Pi](https://www.tinkersoup.de/raspberry-pi/):

-	Raspberry Pi (Ich hatte einen Raspberry Pi 2 Modell B 1GB)
-	Micro SDHC Karte für Pi(für das Betriebsystem)  
-	USB Stromversorgung 5V (Handy Ladekabel bzw. Ladenetzteil)
-	Pi Cobbler (Adafruit Pi T-Cobbler Plus)
-	[Breadboard](http://www.exp-tech.de/komponenten-zubehoer/breadboards/breadboard-830-630-200) und [Jumper Wires](http://www.exp-tech.de/komponenten-zubehoer/kabel/75-pcs-breadboard-jumper-wires-with-m-m-connectors) 
-	HDMI Kabel (damit du auch deinen Pi direkt an Bildschirm anschliesen kannst und mit Maus und Tastatur ohne Umwege bedienen)  
-	Patchkabel (Empfehle aber Wifi Dongel. Damit kannst du dann auch über deinen Laptop den Pi Bedienen)  

Cameras

-	Pi Cam
-	DSLR CANON NIKON SONY (Ich hatte eine CANON 500D)

Relai & Lampe 60w

-	[Relais & Co ](http://www.glacialwanderer.com/hobbyrobotics/?p=9) Hier für werden weitere Materialien Benötigt siehe Link(Damit kannst du die 60w Lampe Schalten. Die Anleitung ist fur Arduino funktionerit aber genausogut mit dem Pi)

Schleimpilz

-	Schleimpilz (Physarum polycephalum)
-	Petrischale mit Närboden
-	Destiliertes Wasser
-	Haferflocken oder andere Nahrungsquellen

###Installation:

Raspberry Pi

1. Installation des Raspberry Pi. Folge dafür der [Anleitung im Video](https://www.raspberrypi.org/help/noobs-setup/)

2. Verbinde deinen Raspberry mit einem Laptop über eine [Remote Desktop controll](https://github.com/Johannesproximo/Remote-Desktop-too-Raspberry-Pi/blob/master/README.md)

3. Installiere die Raspberry Camp. [Folge dafür der Anleitung](https://www.youtube.com/watch?t=65&v=8xWy3g2QAZ8) , mit Timelaps beispiel. Diese Pi Camp unsere Pilzaufnahmen weniger geeignet, da sie nur sehr schwer auf eine bestimmte Entfernung scharfzustellen ist.(Dafür benötigst du eine [Zange und viel Gefühl](https://www.youtube.com/watch?v=u6VhRVH3Z6Y)).
4. Installation einer DSLR. Wird gut [In diesem Repository erklärt](https://github.com/topada/DSLR-Timelapse-gphoto-RPI). Bei meiner Canon 500D trat dabei ein Fehler auf den ich in Folgenden Link [erklärt und Gelöst](https://github.com/Johannesproximo/Pille-der-Schleimpilz/blob/master/DSLR-Timelapse-gphoto-RPI-Zusatz.md) habe.
2. Zeit für die Beleuchtung:
	3. falls du nicht deinen Blitzt(DSLR) verwendst oder du etwa doch mit der Raspberry Camp fotographierst, kannst du dir eine Beleuchtung bauen. [Relais & 60w Lampe ](http://www.glacialwanderer.com/hobbyrobotics/?p=9) 
	4. oder mit LEDs genügent lich für eine Aufnahme mit der Raspberry Camp erzeugen.(++++fehlt noch++++)

3. Nun muss die Beleuchtung und die Camera zusammen geschaltet werden dafür schaut euch am besten [dieses repository an](https://github.com/FH-Potsdam/slime-mold-recording-setup)

4. Versuche erst Testbilder zu schießen, um zu sehen ob die Bilder scharf werden. (ACHTUNG DSLR ACCU muss bei längerer aufnahme gewechselst werden, dies sollte möglichsein ohne die DSLR zu verrutschen.
5. Nun kannst du den Pilz versuchen in deiner Petrischale zu zücketen und geziehlt wachsen zu lasse. Durch die Aufnahme kannst du den Vorgang direkt verfolgen.

6. Mein versuch hat sich an an einer 7 Segments bzw. 15 Segments Anzeige ausgerichtet. Der Pillz sollte jeweils durch Haferfocken die Jeweiligen Segmente verbinden.

![15 Segments](Pictures/seven.jpg)

7. Hast du genügen Bilder geschossen kannst du z.B. mit hilfe von Adobie aftereffects daraus ein Zeitraffer video erstellen.  
VIDEO >>
[![ScreenShot](http://img.youtube.com/vi/K0P-oIHyvpc/0.jpg)](https://youtu.be/K0P-oIHyvpc)

8. Hast du ein Qalitativ hochwertiges Video kannst du nun mit [Processing](https://processing.org/) verbunden mit [OpenCV](https://github.com/FH-Potsdam/hello-processing-py-cv-world) das Wachstum tracken und somit visuel darzustellen.


###Anwenden/Benutzen

- Aufnahmeeinstellungen mit Pi camp
- Aufnahmeeinstellungen mit Pi und DSLR
- Verwendung von Adobie after
- Verwendung von [Processing(Anleitung und Beispiele)](https://processing.org/) mit [OpenCV (Anleitung und Beispiele)](https://github.com/FH-Potsdam/hello-processing-py-cv-world)

###Anmerkungen:
Ich persönlich hatte es nur zu einen halbwegs brauchbaren Aufnahme des Pilzes geschaft und konnte das Video leider nicht mehr mit Open CV verarbeiten.

###Verwandte Arbeiten:


###Dank:
Dank geht an alle meine Kommilitonen des Eingabe Ausgabe Kurses des Sommersemester 2015. Gans besonders natürlich Fabiantheblind unseren JEDI Meister.

###Kontakt:
Falls etwas unklar ist und ihr Fragen habt schreibt mir einfach Johannes.Leick@gmx.de
Viel Spaß

##Public License
Copyright (C) 2015 Johannes Leick aka JohannesProximo Everyone is permitted to copy and distribute verbatim or modified copies of this license document, and changing it is allowed as long as the name is changed.  
