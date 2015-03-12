# mwk-helper-state
## Bundesländer aus einer Lang-Datei laden (DE, AT, CH)
===============================

### Dokumentation
-----------------------------

**Anleitung:**

In deiner DCA-Datei oberhalb von ```$GLOBALS ['TL_DCA]...``` wird der Pfad zur Lang-Datei ```\System::loadLanguageFile('state');``` eingefügt:


z.B Bei einem **SELECT Menü** im DCA-File unter Fields bei ```'options' ```
wird als Wert ```&$GLOBALS['TL_LANG']['STATE'],``` (alle Bundesländer werden geladen) oder
```&$GLOBALS['TL_LANG']['STATE']['DE'],``` (Bundesländer von Deutschland werden geladen) oder
```&$GLOBALS['TL_LANG']['STATE']['AT'],``` (Bundesländer von Österreich werden geladen) oder
```&$GLOBALS['TL_LANG']['STATE']['CH'],``` (Kanton von der Schweiz werden geladen) eingebunden,
die Bundesländer werden jetzt über die Lang-Datei geladen.


BEISPIEL:
```
'name' => array
		(
			'label'                 => &$GLOBALS['TL_LANG']['tabellenname']['name'],
			'inputType'             => 'select',
			'options'               => &$GLOBALS['TL_LANG']['STATE'],
			'eval'                  => array
			(
				'includeBlankOption'=>true,
				'mandatory'=>true,
				'chosen'=>true,
				'tl_class'=>'w50',
			),
			'sql'                   => "varchar(3) NOT NULL default ''",
		),
```

-----------------------------

### Systeminformationen
-----------------------------

Contao 3.2.x oder höher.

-----------------------------

Lizenz: LGPL