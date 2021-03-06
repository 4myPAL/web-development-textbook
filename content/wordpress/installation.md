---
title: Kurz-Installation von Wordpress
order: 30
---

Voraussetzung ist, dass in Ihrem Webspace PHP und MySQL möglich sind, Dauer ca. 30 Minuten: 

1. Finden Sie heraus wie der Zugang zur Datenbank funktioniert: Datenbankname, Username, Passwort
2. Laden Sie die aktuelle Version von Wordpress von als zip-Datei auf Ihren Desktop-Computer herunter. Packen Sie die zip-Datei aus, dabei muss die Ordner-Struktur erhalten bleiben.
3. Schritt Laden Sie das Gesamtpaket (allen Dateien und Unterordner) auf Ihren Webspace hoch. Damit ist der Aufwändige teil erledigt, weiter geht es (fast) nur mit dem Browser weiter.
4. Öffnen Sie die Seite über den Webbrowser, folgen Sie den weiteren Anweisungen um einen ersten Account anzulegen.

Sie werden in Schritt vier nach den Zugangsdaten für die Datenbank gefragt. Es geht hier um vier Angaben:

* Datenbankname
* Username (für den Datenbank-Zugriff)
* Passwort (für den Datenbank-Zugriff)
* Datenbank Host (das ist immer „localhost“)

Diese Daten werden am Ende in der Datei wp-config.php gespeichert, und zwar in folgender Form:

      define('DB_NAME',     'datenbank');            // The name of the database
      define('DB_USER',     'username');                  // Your MySQL username
      define('DB_PASSWORD', 'passwort');                  // ...and password
      define('DB_HOST',     'localhost');    
                           // 99% chance you won't need to change this value

Wenn Sie mehrere Wordpresse mit nur einer Datenbank betreiben gibt es eine weitere Frage: den Tabellen Prefix – die verschiedenen Wordpresse legen jeweils ca. 12 Tabellen an, damit diese Tabellen nicht alle den gleichen Namen haben wird der Prefix verwendet: z.B. beim ersten Wordpress beginnt der Tabellenname immer mit wp_ beim zweiten mit devblog_.

      // You can have multiple installations in one database
      // if you give each a unique prefix
      $table_prefix  = 'devblog_';      // Only numbers, letters, and underscores 

Nach der Installation von Wordpress finden Sie das Backend im Ordner wp-admin (also z.B. http://meinblog.at/wp-admin/). Dieser Bereich ist nur mit Login zugänglich. Im Rahmen der Installation wurde ein Account angelegt den Sie verwenden können. 

