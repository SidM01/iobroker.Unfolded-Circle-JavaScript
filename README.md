# iobroker.Unfolded-Circle-JavaScript

Dies ist ist ein kleines Javascript für die Kommunikation zwischen der Unfolded Circle Remote 2 und IoBroker.

Es ruft über die Rest API verschiendene Information der Remote 2 ab und schreibt sie in eigene Datenpunkte.
Aktuell ist es nur möglich Informationen wie z.b. Ladezustand, Speicherauslastung etc. abzurufen, aber nicht z.B. Aktivitäten zu starten.


Bevor das Script verwendet werden kann, ist es notwendig ein "Bearer Token" auf der Remote zu generieren.
Dazu müsst ihr über einem Webbrowser die folgende Url eingeben: http://"RemoteIP/doc/core-rest/
Scrollt dann zum Punkt POST /auth/api_keys  Create an API key for the UCR APIs.
Ändert das "My integration" z.B. in "IoBroker" und klickt danach auf "Execute"

Anschließend erhaltet ihr in der Ausgabe unter dem Eintrag "api_key" den Bearer token.
Diesen notiert ihr euch irgendwo sicher auf, denn dieser wird euch nur einmalig angezeigt.

Nun könnt ihr das JavaScript in IoBroker einfügen, die IP und den Bearer Token ändern und das Script starten.
Die Datenpunkte werden dabei unter "javascript.0.Unfolded-Circle" erstellt.
