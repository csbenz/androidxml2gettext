# androidxml2pot
Simple Perl scripts to convert android xml strings to pot format and vice-versa

### Convert from android xml to pot gettext
`./xml2pot strings.xml output.pot`

strings.xml is the android string xml and should be formatted as follows:

```
<?xml version="1.0" encoding="utf-8"?>
<resources>

    <string name="app_name">Lucidity</string>
    <string name="title_activity_display_dream">My Dreams</string>
    <string name="title_activity_new_dream">New dream</string>
<resources>
```

! Every string tag should be on a single line

### Convert from gettext to android xml
`./pot2xml input.pot strings-ko.xml`

The pot file is a gettext file formatted as follows:
```
msgctxt "app_name"
msgid "Lucidity"
msgstr ""

msgctxt "title_activity_display_dream"
msgid "My Dreams"
msgstr ""

msgctxt "title_activity_new_dream"
msgid "New dream"
msgstr ""
```
where 'msgstr' contains the translated string.
