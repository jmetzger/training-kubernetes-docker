#  nano (einrückung für yaml-dateien aktivieren

## Ubuntu (im Unterverzeichnis /etc/nanorc - systemweit) 

### Schritt 1: Wir testen die Version

```
# - Es sollte mindestens die Version 5.9
# - Die kommt mir der Datei für Syntax-Highlightning
nano --version
```

### Schritt 2: Konfigurationen setzen 

```
# 2.1 Syntax Hightlightning 
echo "include /usr/share/nano/yaml.nano" >> /etc/nanorc 
# 2.2 Automatische Einrückung 
echo "set autoindent" >> /etc/nanorc
# 2.3 Einrückung durch Tab 2 Stellen 
echo "set tabsize 2" >> /etc/nanorc
# 2.4 Tabs werden automatisch in Leerzeichen umgewandelt
# - yaml mag keine TAB-Zeichen
echo "set tabstospaces" >> /etc/nanorc 
```

### Schritt 3: Testen 

```
nano test.yml 
```

### Schritt 4: Jetzt im Nano gib' ein:

```
test:
# Wow, es funktioniert, die Farben sind da.
```

### Schritt 5: Verlasse nano 

```
CTRL + x
```

### Schritt 6: Nano fragt Dich:

```
# Save modified buffer ?
# Du drückst die Taste:
n 
```
