# Beckhoff MQTT Bibliothek
 Diese Library enthält 2 Funktionen mit denen man sich zu einem MQTT Broker verbinden und kommunizieren (publish/subscribe) kann.

Dieses Git Repository wird von  Ing. Armin Fischer, M.Sc. (fia@htlwrn.ac.at) gewartet.

Die Hauptfunktionen wurden von der Beckhoff Homepage runtergeladen :
Link Programm: https://infosys.beckhoff.de/index.php?content=../content/1031/tf6701_tc3_iot_communication_mqtt/36028800537505163.html&id=
Link Beschreibung MQTT: https://infosys.beckhoff.de/index.php?content=../content/1031/tf6701_tc3_iot_communication_mqtt/36028800537505163.html&id=

Dieses Git Repository untersteht der GNU GPL v3 Lizenz.

# Verwendung des Git Repositories und Einstellungen

Siehe Word Datei Einstellungen_Beckhoff

# Einstellungen

In der GVL_MQTT müssen folgende Parameter eingestellt werden: 
	mqtt_port --> Port des Brokers zur MQTT Kommunikation
	mqtt_broker --> Broker IP-Adresse
	username --> Benutzername des Brokers
	password --> Passwort für den benutzernamen
	mqtt_interval --> Sendeintervall der Nachrichten

# BEFEHL PrgMqttPublish

PrgMqttPublish(sTopicPub :='Hier kommt das Topic rein', mqtt_payload := hier Zahl [REAL]);

Es wird jede mqtt_interval (im GVL einstellen) eine Nachricht geschickt.

# BEFEHL PrgMqttSubscribe

PrgMqttSubscribe(sTopicSub := 'Hier kommt das Topic rein');

Das empfangene Topic wird in PrgMqttSubscribe.sTopicRcv und die empfangene Nachricht in PrgMqttSubscribe.sPayloadRcv gespeichert.
