# MC-Server

Was ist MC?
Ausgeschrieben bedeutet dies Minecraft und ist ein Computerspiel woman mit freunden auf der ganzen Welt spielen kann.

Hier wird ganz kurz beschrieben wie dies Funktioniert und wie die DATEN lokal gesichert sind.

### Einleitung

Am einfachsten ist wenn wir das Image von der Cloud via pull herunterladen. Anschliessend können wir mit docker run den container
so konfigurieren wie wir möchten bzw. benötigen.

Image von der Cloud herunterladen:

$ docker pull itzg/minecraft-server


Container starten mit verschiedene Parameter und Sicherheitsaspekte wurden berüchtsichtigt:

$ docker run -e EULA=true -p 25565:25565 -v /home/ubuntu/Desktop/docker/mc:/data itzg/minecraft-server:latest

-e : Wenn mann den Server Starten möchte, verlangt der Server das man seine Allgemeinbedieniungen bestätigt werden mittels
"EULA=true" können wir dies erreichen

-p : Wird definiert auf welchen Port der Server höhren muss, beim MC Server ist der Port 255655 der Standard Port

-v : Möchte man die Daten auf unseren Ubuntu Server (Host) die Daten der den MC Server erstellt, speichern kann man den Speicherport angeben und die Daten werden lokal gespeichert. (WIRD DER CONTAINER GELÖSCHT DANN BLEIBEN DIESE DATEN VOM HOST BESTEHEN!!!!)
