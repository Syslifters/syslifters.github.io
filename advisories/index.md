# Advisories

## Jedox 2023

- **Hersteller:** [Jedox GmbH](https://www.jedox.com/de/)

- **Produkt:** Jedox / Jedox Cloud

- **Version:** Jedox 2020.2.5+

- **CVE Nummer:** CVE-2022-47874, CVE-2022-47875, CVE-2022-47876, CVE-2022-47877, CVE-2022-47878, CVE-2022-4779, CVE-2022-4780

- **2022-12-20:** Erstkontakt mit dem Hersteller über zwei Manager

- **2022-12-27:** Kontakt mit dem Hersteller über eine öffentliche Mailadresse

- **2023-01-11:** Zur Verfügungstellung eines verschlüsselten Kanals durch den Hersteller

- **2023-01-18:** Meldung der Schwachstellendetails

- **2023-04-28:** Veröffentlichung der Schwachstellendetails

**CVE-2022-47879: Code Execution über RPC Interfaces**

Eine Remote Code Execution (RCE) Schwachstelle in */be/rpc.php* und */be/erpc.php* in Jedox Cloud und Jedox 2020.2.5 erlaubt authentifizierten Benutzern, beliebige PHP-Klassen aus dem Verzeichnis *rtn* zu laden und deren Methoden auszuführen. Um diese Schwachstelle auszunutzen, benötigt der Angreifer Kenntnis über ladbare Klassen, ihre Methoden und Argumente.

**CVE-2022-47875: Remote Code Execution über Directory Traversal**

Eine Directory Traversal Schwachstelle in */be/erpc.php* in Jedox Cloud und Jedox 2020.2.5 erlaubt authentifizierten Benutzern die Ausführung von beliebigem Code. Um die Schwachstelle auszunutzen, benötigt ein Angreifer Berechtigungen Dateien hochzuladen.

**CVE-2022-47877: Stored Cross-Site Scripting im Log-Modul**

Eine Stord Cross-Site-Scripting-Schwachstelle in Jedox 2020.2.5 erlaubt es authentifizierten Benutzern, beliebige Skripte oder HTML in die Log-Seite über das Log-Modul einzuschleusen. Um die Schwachstelle auszunutzen, muss der Angreifer eine XSS-Payload an die Protokollnachricht anhängen.

**CVE-2022-47878: Remote Code Execution über konfigurierbaren Storage Path**

Eine fehlerhafte Eingabevalidierung zur Konfiguration des Storage Paths in Jedox 2020.2.5 erlaubt es authentifizierten Benutzern, den Speicherort als Web-Root-Verzeichnis anzugeben. Nachfolgende Datei-Uploads können zur Ausführung von beliebigem Code führen. Um die Schwachstelle auszunutzen, setzt der Angreifer den Standard-Speicherpfad auf das Web-Root des Webservers.

**CVE-2022-47876: Remote Code Execution über ausführbare Groovy-Scripts**

Integrator in Jedox 2020.2.5 erlaubt authentifizierten Benutzern, Jobs zu erstellen, um beliebigen Code über Groovy-Skripte auszuführen. Um die Sicherheitslücke auszunutzen, muss der Angreifer in der Lage sein, einen Groovy-Job in Integrator zu erstellen.

**CVE-2022-47874: Offenbarung von Databankzugangsdaten aufgrund unzureichender Zugriffskontrollen**

Unzureichende Zugriffskontrollen in */tc/rpc* in Jedox Cloud und Jedox 2020.2.5 ermöglichen es authentifizierten Benutzern, Details von Datenbankverbindungen über die Klasse *com.jedox.etl.mngr.Connections* und die Methode *getGlobalConnection* einzusehen. Um die Sicherheitslücke auszunutzen, muss der Angreifer den Namen der Datenbankverbindung kennen.

**CVE-2022-47880: Offenlegung von Datenbankverbindungen über Verbindungstests**

Eine Information Disclosure Schwachstelle in `/be/rpc.php` in Jedox Cloud und Jedox 2020.2.5 ermöglicht es authentifizierten Benutzern mit entsprechenden Berechtigungen, Datenbankverbindungen zu ändern, um die Zugangsdaten über die Funktion `test connection` offenzulegen. Um die Sicherheitslücke auszunutzen, muss der Angreifer den Host der Datenbankverbindung auf einen unter seiner Kontrolle stehenden Server setzen.
