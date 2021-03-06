Changelog
=========

Version 2.4.0 – XX.XX.2017
--------------------------

### Neu

* Unterstützung webp (@Hirbod)
* Neue globale Einstellung zu Webp-Qualität, PNG-Kompression und Interlace/Progressive-Modus (@Hirbod, @gharlan)
* JPG- und Webp-Qualität, PNG-Kompression, Interlace/Progressive-Modus können über Effekte gesetzt werden (@gharlan)
* Neue Effekte:
    - image_properties (JPG- und Webp-Qualität, PNG-Kompression, Interlace/Progressive-Modus) (@Hirbod, @gharlan)
    - brightness (@Hirbod)
    - contrast (@Hirbod)
* Angepasste Effekte:
    - flip: Spiegelung an X- und Y-Achse gleichzeitig möglich (@Hirbod)
* Sprechende (übersetzte) Namen für Effekte (@gharlan)

### Bugfixes

* `setSourcePath()` konnte nicht in Effekten richtig genutzt werden (@gharlan)
* Bildtyperkennung schlug teilweise fehl (@gharlan)
* Effekte:
    - flip: Native gd-Methode, 1px-Versatz, Transparenz-Erhaltung (@Hirbod)
    - greyscale: Native gd-Methode, Transparenz-Erhaltung (@Hirbod)
    - sepia: Native gd-Methode, Transparenz-Erhaltung (@Hirbod)
    - sharpen: Warf teilweise Warnings (@gharlan)
    - mediapath: Teilweise kam bei eigentlich existierenden Bildern trotzdem das Error-Bild (@gharlan)
    - header: Korrektur no_cache-Header (@gharlan)

Version 2.3.0 – 21.02.2017
--------------------------

### Neu

* Einfache Methode um an die generierte Cache-Datei zu kommen und so die Bildmaße etc. auszulesen (`rex_media_manager::create($type, $file)->getMedia()`)

### Bugfixes

* Mit PHP 5.5 wurden die Medien nicht mehr ausgeliefert


Version 2.2.0 – 14.02.2017
--------------------------

### Neu

* Neuer Effekt rotate zum Drehen der Bilder (@alexplusde)
* Medientypen können dupliziert werden (@phoebusryan)
* Ggf. geöffnete Sessions werden frühzeitig abgebrochen, um Session Locking zu mindern

### Bugfixes

* „Cache löschen“ führte auf Anleitung statt auf Typen-Page (@ynamite)


Version 2.1.0 – 15.07.2016
--------------------------

### Neu

* Neue Effekte: colorize (@phoebusryan), convert2image

### Bugfixes

* Effekte insert_image, filter_blur und rounded_corners repariert
* crop-Filter schneidet nun auch zu, wenn nur eine Seite größer als Zielgröße ist
* fileinfo-Extension war nicht als Abhängigkeit hinterlegt
* Bei gecachten Bildern wurde bei der Auslieferung nicht der Output Buffer geleert


Version 2.0.2 – 24.03.2016
--------------------------

### Bugfixes

* Fehler im png/alpha Handling beseitigt
