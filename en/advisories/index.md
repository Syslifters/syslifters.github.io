# Avisories

## Jedox 2023

- **Vendor:** [Jedox GmbH](https://www.jedox.com/de/)

- **Product:** Jedox / Jedox Cloud

- **Version:** Jedox 2020.2.5+

- **CVE Number:** CVE-2022-47874, CVE-2022-47875, CVE-2022-47876, CVE-2022-47877, CVE-2022-47878, CVE-2022-4779, CVE-2022-4780

- **2022-12-20:** Initial contact to the vendor via two managers

- **2022-12-27:** Contact with vendor via public mail address

- **2023-01-11:** Vendor provides encrypted channel for vulnerbility information

- **2023-01-18:** Reporting of vulnerability details

- **2023-04-28:** Planned public disclosure

**CVE-2022-47879: Code Execution via RPC Interfaces**

A Remote Code Execution (RCE) vulnerability in */be/rpc.php* and */be/erpc.php* in Jedox Cloud and Jedox 2020.2.5 allows remote authenticated users to load arbitrary PHP classes from the *rtn* directory and to execute its methods. To exploit this vulnerability, the attacker needs knowledge about loadable classes, their methods and arguments.

**CVE-2022-47875: Remote Code Execution via Directory Traversal**

A Directory Traversal vulnerability in */be/erpc.php* in Jedox Cloud and Jedox 2020.2.5 allows remote authenticated users to execute arbitrary code. To exploit the vulnerability, the attacker must have the permissions to upload files.

**CVE-2022-47877: Stored Cross-Site Scripting in Log-Module**

A Stored cross-site scripting vulnerability in Jedox 2020.2.5 allows remote authenticated users to inject arbitrary web scripts or HTML in the logs page via the log module. To exploit the vulnerability, the attacker must append an XSS payload to the log message.

**CVE-2022-47878: Remote Code Execution via Configurable Storage Path**

Incorrect input validation for the default-storage-path in the settings page in Jedox 2020.2.5 allows remote, authenticated users to specify the location as web root directory. Consecutive file uploads can lead to the execution of arbitrary code. To exploit the vulnerability, the attacker sets the default storage path to the web root.

**CVE-2022-47876: Remote Code Execution via Executable Groovy-Scripts**

Integrator in Jedox 2020.2.5 allows remote authenticated users to create Jobs to execute arbitrary code via Groovy-scripts. To exploit the vulnerability, the attacker must be able to create a Groovy-Job in Integrator.

**CVE-2022-47874: Disclosure of Database Credentials via Improper Access Controls**

Improper access controls in */tc/rpc* in Jedox Cloud and Jedox 2020.2.5 allows remote authenticated users to view details of database connections via the class *com.jedox.etl.mngr.Connections* and the method *getGlobalConnection*. To exploit the vulnerability, the attacker must know the name of the database connection.

**CVE-2022-47880: Disclosure of Database Credentials via Connection Checks**

An information disclosure vulnerability in `/be/rpc.php` in Jedox Cloud and Jedox 2020.2.5 allows remote authenticated users with the appropriate permissions to modify database connections to disclose the clear text credentials via the `test connection`function. To exploit the vulnerability, the attacker must set the host of the database connection to a server under his control.
