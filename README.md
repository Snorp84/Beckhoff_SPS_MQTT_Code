# Beckhoff MQTT Bibliothek
 Diese Libraty enthält 2 Funktionen mit denen man sich zu einem MQTT Broker verbinden und kommunizieren (publish/subscribe) kann.

Dieses Git Repository wird von  Ing. Armin Fischer, M.Sc. (fia@htlwrn.ac.at) gewartet.

Dieses Git Repository untersteht der GNU GPL v3 Lizenz.

# Verwendung des Git Repositories

Alle 3 Komponenten müssen in das gewünschte Beckhoff Projekt importiert werden.:
Rechtsklick auf GVL/POU --> PLCOpenXML importieren

# Einstellungen

In der GVL_MQTT müssen folgende Parameter eingestellt werden: 
	mqtt_port --> Port des Brokers zur MQTT Kommunikation
	mqtt_broker --> Broker IP-Adresse
	username --> Benutzername des Brokers
	password --> Passwort für den benutzernamen
	mqtt_interval --> Sendeintervall der Nachrichten

# BEFEHL PrgMqttPublish
Aufruf:
PrgMqttPublish(sTopicPub :='Hier kommt das Topic rein', mqtt_payload := hier Zahl [REAL]);

Es wird jede mqtt_interval (im GVL einstellen) eine Nachricht geschickt.

# BEFEHL PrgMqttSubscribe
Aufruf:
PrgMqttSubscribe(sTopicSub := 'Hier kommt das Topic rein');

Das empfangene Topic wird in PrgMqttSubscribe.sTopicRcv und die empfangene Nachricht in PrgMqttSubscribe.sPayloadRcv gespeichert.
