# Installation
Um das Projekt lokal auszuführen, müssen Sie zunächst sicherstellen, dass Sie Node.js und npm installiert haben.

1. Klonen Sie dieses Repository auf Ihren lokalen Computer.
2. Navigieren Sie zum Verzeichnis ClientApp: `cd ClientApp`
3. Führen Sie den Befehl `npm install` aus, um die erforderlichen npm-Pakete zu installieren.

**Hinweis**: Zur Ausführung von ASP.NET-Anwendungen auf Windows muss das Windows-Feature "Internet Information Services (IIS)" aktiviert sein. Bitte folgen Sie den nachstehenden Anweisungen, um es zu aktivieren:

1. Öffnen Sie die Windows-Systemsteuerung.
2. Navigieren Sie zu "Programme" und wählen Sie "Programme und Features" aus.
3. Klicken Sie auf "Windows-Funktionen ein- oder ausschalten".
4. Suchen Sie nach "Internet Information Services (IIS)" in der Liste der Funktionen.
5. Aktivieren Sie das Kontrollkästchen neben "Internet Information Services (IIS)".
6. Klicken Sie auf "OK", um die Änderungen zu übernehmen. Windows wird den Internet Information Services (IIS) installieren und konfigurieren.

# Ausführung des Projekts
Nach Abschluss der Installation können Sie das Projekt wie folgt ausführen:

1. Starten Sie Ihre bevorzugte IDE (Integrated Development Environment).
2. Wählen Sie IIS Express als Ihr Ausführungsumgebung. ![Untitled](https://github.com/Baris-Kacar/ASPDotNetAngularTemplate/assets/73958902/6d3df261-dde8-4ecc-820a-8f245583ae4e)
3. Warten Sie, bis der Frontend Server vollständig gestartet ist. ![NPM](https://github.com/Baris-Kacar/ASPDotNetAngularTemplate/assets/73958902/14ffb1b8-1718-4637-853e-599bb2442984)  ![SPAProxy](https://github.com/Baris-Kacar/ASPDotNetAngularTemplate/assets/73958902/522d8ef5-ae79-4e68-9c89-f3e455266567)
4. Sie werden automatisch zur Angular-Seite weitergeleitet. ![Capture](https://github.com/Baris-Kacar/ASPDotNetAngularTemplate/assets/73958902/ff6e2520-4270-4d2e-b507-8baf1a337588)


## Was ist ein SPA-Proxy?
Ein SPA-Proxy ist ein Zwischenglied zwischen Ihrem Backend-Server und Ihrem Frontend-Framework. Es fungiert als Vermittler, der Anfragen von Ihrem Backend-Server entgegennimmt und sie an Ihren Frontend-Entwicklungsserver weiterleitet. Der Proxy wartet geduldig, bis der Frontend-Entwicklungsserver vollständig gestartet ist, bevor er Anfragen weiterleitet.

Ein SPA-Proxy (Single Page Application Proxy) ist ein Mechanismus, der verwendet wird, um Anfragen von einem Webserver an eine Single Page Application (SPA) weiterzuleiten, die separat von einem Backend-Server gehostet wird. Dies ist besonders nützlich, wenn die SPA und das Backend auf unterschiedlichen Servern oder Ports gehostet werden.

Im Kontext von ASP.NET Core und Angular könnte der SPA-Proxy beispielsweise wie folgt funktionieren:

Der Backend-Server, der ASP.NET Core verwendet, wird auf einem bestimmten Port (44345) ausgeführt.
Die Angular-SPA wird separat auf einem anderen Port (44422) mithilfe des Angular CLI-Servers (mit ng serve) ausgeführt.
Da beide Server separat ausgeführt werden, kann der SPA-Proxy auf dem Backend-Server konfiguriert werden, um Anfragen an die Angular-SPA weiterzuleiten, wenn sie auf einem anderen Port läuft.
