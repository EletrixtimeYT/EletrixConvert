<h1>FR Convertir un html en .exe<h1>


`webpage to .exe`

1 
Installer python https://www.python.org/downloads/

2
Créé un dossier avec vos fichier html le fichier principal dans avoir comme nom index.html (Si c sur un site pas besoin mais juste besoin du main.py)
<img src="htmltoexe1.png">

3
Installer les libs suivante (avec la cmd)
`pip install PyQt5`
Et
`pip install auto-py-to-exe`

4 Copier coller le code suivant  (avant ouvrer le fichier main.py dans bloc note)
4.1 Si vous voulez mettre un site vous devez remplacer le index.html par l url du site 
4.2 vous pouvez mettre un nom d app en remplacant le NOM APP en par exemple youtube desktop

from PyQt5.QtCore import *
from PyQt5.QtWidgets import *
from PyQt5.QtGui import *
from PyQt5.QtWebEngineWidgets import *
from PyQt5.QtPrintSupport import *
import os
import sys
class MainScreen(QMainWindow):
    def __init__(self):
        super(MainScreen,self).__init__()
        self.Browser = QWebEngineView()
        self.Browser.setUrl(QUrl('file:///index.html)) 
        self.setCentralWidget(self.Browser)
        self.showMaximized()
Application = QApplication(sys.argv)
QApplication.setApplicationName('NOM APP')
Window = MainScreen()
Application.exec()

5 Sauvegarder et faite  `python -m auto_py_to_exe` dans la CMD ou dans visual studio
5.1 Ca va vous ouvrir une page web
5.2 Mettez votre fichier main.py en cliquer sur browse
5.3 cliquer sur convert !
5.4 Ensuite chercher l endroit d ouput du fichier
**
IMPORTANT SI C EST UN FICHIER HTML METTEZ LE DANS UN DOSSIER AVEC VOTRE .PY CONVERTI .EXE  **

PS : **En cas de souci me ping  et je ferrais peut etre une video ou un site ou un tuto detailler ! si vous voulez je peux le faire pour vous me mp**
Merci