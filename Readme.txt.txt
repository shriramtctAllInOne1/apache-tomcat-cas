
----------------------------Generate key ----------------------------------


keytool -genkey -alias mkyong -keyalg RSA -keystore c:\mkyongkeystore

---------------------------------------------------------------------------
check certificate details :

keytool -list -keystore c:\mkyongkeystore

----------------------------------------server.xml--------------------------------

<Connector port="8080" protocol="HTTP/1.1" SSLEnabled="true"
               maxThreads="150" scheme="https" secure="true"
               clientAuth="false" sslProtocol="TLS" 
	       keystoreFile="c:\mkyongkeystore"
	       keystorePass="password" />
---------------------------------------------------------------------------------
https://localhost:8080/