# Labor Kommunikationsnetze 1

## Aufsetzen der Umgebung
* Sie benötigen zur Bearbeitung [Visual Studio Code (VS Code)](https://code.visualstudio.com) mit der Erweiterung [Remote SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh). 
* Nachdem Sie die IDE mit der entsprechenden Erweiterung eingerichtet haben, benötigen Sie noch folgende Programme in Abhängigkeit von Ihrem Betriebssystem:
  * Windows(AMD-Architektur): Die Programme [Virtualbox](https://www.virtualbox.org/wiki/Downloads) und [git](https://git-scm.com/install/windows).
  * Windows(ARM-Architektur): Das Programm [Qemu](https://www.qemu.org/download/#windows) und [git](https://git-scm.com/install/windows).
  * Linux: Das Programm [Virtualbox](https://www.virtualbox.org/wiki/Downloads) und [GenIsoImage](https://wiki.ubuntuusers.de/genisoimage/).
  * Mac(Silicon): Den Paket-Manager [Homebrew](https://brew.sh/), um damit die Pakete `qemu`, `wget` und `cdrtools` zu instalieren.
  * Mac(Intel): Den Paket-Manager [Homebrew](https://brew.sh/), um damit die Pakete `virtualbox`,`wget` und `cdrtools` zu instalieren.
* `Wichtig`: Bei Windows müssen Sie das Programm `Virtualbox` im Standardverzeichnis, welches Ihnen bei der Installation vorgeschlagen wird, installieren.
* Außerdem benötigen Sie die in diesem Repo befindliche Datei `kn1lab-install.sh`.
* Führen Sie unter Linux und Mac noch den Befehl `chmod +x kn1lab-install.sh` im entsprechenden Verzeichnis aus, um das Skript ausführbar zu machen.
* Mit dem folgenden Befehl können Sie darufhin in einem Terminal eine Virtuelle Ubuntu Maschine aufsetzen `(unter Windows müssen Sie für die Ausführung des Skripts Git Bash verwenden, da das Skript in Powershell oder der Eingabeaufforderung nicht ausgeführt werden kann)`: 

```bash
./kn1lab-install.sh
```

* Anschließend können Sie sich mit der Maschine über ssh verbinden, indem Sie diese als Host in Visual Studio Code anlegen. Dafür können Sie über den blauen Remote-Window-Knopf im linken unteren Eck mit der Option `Connect to Host` und der darauffolgenden Option `Add new SSH Host` unter Angabe von `ssh -p 2222 labrat@localhost` die Einrichtung durchführen.
* Nach der Einrichtung können Sie sich mit der Maschine über deren Auswahl in der Option `Connect to Host` verbinden.
* Sobald Sie mit der Maschine verbunden sind, müssen Sie durch die Option `Open Folder` das Verzeichnis des Labor-Repos (`kn1lab`) öffnen und das Skript `setup.sh` ausführen.
* Dafür müssen Sie in Visual Studio Code ein Terminal öffnen und das Skript mit `./setup.sh` ausführen.
* Dieses Skript setzt Ihre Umgebung final auf und installiert auch alle benötigten Erweiterungen für Visual Studio Code, sodass Sie danach alle Versuche bearbeiten können.

## Anmerkungen zur weiteren Verwendung der virtuellen Maschine im Laufe des Semesters

* Sie müssen die virtuelle Maschine nach jedem Neustart Ihres Computers ebenfalls erneut starten, damit Sie sich mit dieser verbinden können.
* Bei der Verwendung von Virtualbox können Sie die VM innerhalb der Anwendung VirtualBox starten.
* Bei Qemu müssen Sie das Skript `kn1lab-install.sh` erneut ausführen, das Ausführen des Setup-Skripts ist nicht notwendig.
* Bei der Verwendung von Qemu gibt es außerdem die Möglichkeit, mit dem Skript `stop-vm.sh` die Virtuelle Maschine in einem Terminal außerhalb der virtuellen Maschine anzuhalten. Unter Umständen müssen Sie das Skript mit dem Befehl `chmod +x stop-vm.sh` zuvor ausführbar machen.


## Aufgabenstellungen

### [Versuch 1 - Anwendungsschicht](versuch1/aufgabenstellung.md)
### [Versuch 2 - Transportschicht](versuch2/aufgabenstellung.md)
### [Versuch 3 - Vermittlungsschicht](versuch3/aufgabenstellung.md)
### [Versuch 4 - Leistungsmessung](versuch4/aufgabenstellung.md)
