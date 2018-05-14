# `#02` - NPM Package publishen

> Die Vorgangsweise ist bei Linux und Windows gleich.

---

## NPM Account erstellen und einloggen

Zuerst ist es nötig einen [**NPM Account zu erstellen**](https://www.npmjs.com/signup), wenn dies noch nicht erfolgt ist.

Danach muss man sich mit seinen Account Credentials in der Console bei NPM anmelden, um Packages veröffentlichen zu können:

```
$ npm login
```

> Die eingegebene E-Mail-Adresse wird als Kontaktadresse beim publishen eines Packages angegeben, ist also öffentlich einsehbar!

---

## Publishing und Updating

Zuerst muss man in den Root-Ordner des Packages navigieren. In unserem Beispiel:
```
$ cd 01-npmpackages/examplepackage
```

Danach kann man mit folgendem Command das Package publishen:
```
$ npm publish
```

Danach wird das Package unter dem in der `package.js` spezifizierten Namen unter `https://www.npmjs.com/package/<NameDesPackages>` veröffentlicht und kann heruntergeladen werden über
```
$ npm install <NameDesPackages> --save
```

Möchte man sein Package updaten, so ändert man einfach die Version in der `package.json` und re-publisht das Package mit
```
$ npm publish
```

Danach ist die neue Version des Packages auf npmjs.com erreichbar.

---

© 2018 - present  
Ringo Hoffmann (zekro Development)  
zekro.de | contact[at]zekro.de
