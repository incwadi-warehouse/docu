# Changelog

## v53

en

- [catalog] Fix issue in search where translation was missing counter
- [search-api][catalog][EXPERIMENT] New search index 

de

- [catalog] Fehler in der Suche behoben, wodurch der Counter in der Übersetzung nicht sichtbar war
- [search-api][catalog][EXPERIMENT] Neuer Such-Index
- 
## v52

en

- [orders] Print customer details
- [catalog][settings][orders] New profile link, uses now the new accounts service
- [catalog][settings][orders] Redesign navigation panel
- [admincli][EXPERIMENT] CLI in the server for emergencies

de

- [orders] Drucke Kundeninformationen
- [catalog][settings][orders] Neuer Profil-Link, der neue Accounts-Service wird jetzt verwendet.
- [catalog][settings][orders] Navigations-Panel neu gestaltet
- [admincli][EXPERIMENT] CLI auf dem Server für Notfälle

## v51

en

- [conf-api] The config service is now stable
- [catalog][orders][settings][accounts] Snow, Party, Pride and Beach is now available on the internal pages
- [core][catalog] Books can be marked as duplicate
- [catalog] Fix issue where after reset the filter all branches where searched

de 

- [conf-api] Der config-Service ist jetzt stabil
- [catalog][orders][settings][accounts] Schnee, Party, Pride und Strand ist jetzt auf den internen Seiten verfügbar
- [core][catalog] Bücher können als Duplikat markiert werden.
- [catalog] Fehler behoben, wodurch nach dem Zurücksetzen der Filter die Suche über alle Filialen hinweg lief.

## v50

en

- [orders] Sell all products from order
- [orders] Remove product from order
- [conf-api] Improvements
- [core] Field format must not be empty
- [orders] Remove action to remove a book from order

de

- [orders] Alle Produkte aus einer Bestellung verkaufen
- [orders] Produkt von einer Bestellung entfernen
- [conf-api] Verbesserungen
- [core] Feld Typ darf nicht mehr leer bleiben
- [orders] Einzelne Bücher können nicht mehr von der Liste entfernt werden
 
## v49

en

- [orders] Reactoring
- [conf-api][EXPERIMENT] Bugfix and Improvements
- [orders] New list and detail view, old view removed
- [accounts][EXPERIMENT] Accounts service improved

de

- [orders] Reactoring
- [conf-api][EXPERIMENT] Korrektur und Verbesserungen
- [orders] Neue Listen- und Detailansicht, alte Ansicht entfernt
- [accounts][EXPERIMENT] Accounts Service verbessert

## v48

en

- [settings][EXPERIMENT] Rework Detail View
- [orders] Fix allowing blobs in CSP
- [conf-api][EXPERIMENT] New settings service
- [catalog] Fix bug where is was not possible to save a book without release year
- [orders][EXPERIMENT] New orders view is now the default
- [orders][EXPERIMENT] Show snow and party toggle only for authenticated users
- [orders][EXPERIMENT] Rainbow Colors

de

- [settings][EXPERIMENT] Detail View überarbeitet
- [orders] Blobs in CSP sind jetzt erlaubt
- [conf-api][EXPERIMENT] Neuer Settings-Service
- [catalog] Bug behoben, der Speichern von Büchern ohne Erscheinungsjahr verhindert hat
- [orders][EXPERIMENT] Die neue Ansicht in den Bestellungen ist jetzt der Standard
- [orders][EXPERIMENT] Zeige Schnee- und Party-Toggle nur wenn Nutzer authentifiziert sind
- [orders][EXPERIMENT] Rainbow Colors

## v47

en

- [orders][EXPERIMENT] Add snow and confetti
- [orders][EXPERIMENT] New List View and Detail View
- [orders] Refactoring
- [catalog][settings][orders] Remove Footer
- [core] Respect firstname in order by author

de

- [orders][EXPERIMENT] Schnee und Konfetti hinzugefügt
- [orders][EXPERIMENT] Neue Listenansicht und Detailansicht
- [orders] Refactoring
- [catalog][settings][orders] Footer entfernt
- [core] Berücksichtige Vorname in OrderBy Autor*in

## v46

en

- [settings][EXPERIMENT] Tags list is now stable
- [core][settings][EXPERIMENT] Remove announcements
- [settings] Fix issue with white page after login

de

- [settings][EXPERIMENT] Schlagwortübersicht ist jetzt stabil
- [core][settings][EXPERIMENT] Announcements entfernt
- [settings] Fehler behoben wodurch nach dem Login eine weiße Seite gezeigt wurde

## v45

en

- [core][catalog][orders][settings][DEPRECATION] Remove bookmarks
- [extra-bundle][DEPRECATION] Refactor user
- [core][settings][DEPRECATION] Remove "order by" in genre filter
- [api-bundle][DEPRECATION] Reworked `Serializer` is part of `Response` 
- [catalog][orders][settings] Moved to monorepo
- [catalog] Fix show correct error message if book can't be saved
- [catalog][EXPERIMENT] Author Search no longer available
- [core][catalog][shop] Release year can now be empty (in fact its 0), Validation allows values from 0 to 9999

de 

- [core][catalog][orders][settings][DEPRECATION] Bookmarks entfernt
- [extra-bundle][DEPRECATION] User Funktionen überarbeitet
- [core][settings][DEPRECATION] "Sortieren nach" bei den Rubriken Filtern entfernt
- [api-bundle][DEPRECATION] Überarbeiteter `Serializer` ist Teil von `Response` 
- [catalog][orders][settings] In Monorepo verschoben
- [catalog] Sofern ein Buch nicht angelegt werden kann, wird jetzt die korrekte Fehlermeldung ausgegeben.
- [catalog][EXPERIMENT] Suche nach Autor\*innen ist nicht mehr verfügbar
- [core][catalog][shop] Erscheinungsjahr kann leer bleiben (d.h. es wird auf 0 gesetzt), Validator erlaubt Werte von 0 bis 999

## v44

en

- [shop] Decrease font size for genre filter
- [shop] Move to monorepo
- [core][catalog] Show number of open reservations in alert
- [catalog][settings][shop][orders] Update UI library @baldeweg/ui
- [core] Update flex recipes
- [api-bundle][DEPRECATION] Remove response from controller
- [api-bundle][DEPRECATION] Remove transformer from serializer
- [core][catalog][settings][orders][DEPRECATION] Deprecate bookmarks
- [core][catalog][orders] Remove date and time for reservations
- [extra-bundle][DEPRECATION] Deprecate `isUser` and `isAdmin`. No user returned in password controller.
- [extra-bundle] Refactoring User Service
- [settings][EXPERIMENT] List all tags of a branch
- [core][settings][EXPERIMENT] Show Announcements, configurable in settings 
- [core][settings][DEPRECATION] Deprecate order by
- [catalog] Fix reset subtitle after creating a book

de

- [shop] Kleinere Schrift für den Rubriken-Filter
- [shop] In das Monorepo verschoben.
- [core][catalog] Zeige Zahl offener Reservierungen in Benachrichtigung
- [catalog][settings][shop][orders] UI Library @baldeweg/ui aktualisiert
- [core] Flex Recipes aktualisiert
- [api-bundle][DEPRECATION] Response from API Controller entfernt
- [api-bundle][DEPRECATION] Transformer von Serializer entfernt
- [core][catalog][settings][orders][DEPRECATION] Bookmarks werden nicht mehr unterstützt
- [core][vatalog][orders] Datum und Uhrzeit von Reservierungen entfernt
- [extra-bundle][DEPRECATION] Die Methoden `isUser` und `isAdmin` werden bald entfernt. Im Password Controller wird demnächst kein User Array mehr zurückgeliefert.
- [extra-bundle] User-Service überarbeitet
- [settings][EXPERIMENT] Liste alle Schlagworte für eine Filiale auf
- [core][settings][EXPERIMENT] Zeige Ankündigungen, konfigurierbar in den Einstellungen
- [core][settings][DEPRECATION] Sortierreihenfolge wird bald entfernt
- [catalog] Fehler behoben, wodurch Untertitel nach dem Katalogisieren nicht zurückgesetzt wurde.

## v43

en

- [shop] Allow headings for content in shop
- [shop] Rename genre to genres, colored selector for filter
- [core][orders] Status for reservations
- [core][catalog][shop] Add subtitle for books
- [core] Remove Import and Export
- [core] Fix genre in shop respecting global setting for order
- [core][catalog] Directory is now stable
- [catalog][EXPERIMENT] New Search for Authors
- [shop] Bigger font and filter info for filters
- [core][catalog][orders][DEPRECATION] Deprecate Date and Time in Reservation
- [accounts][EXPERIMENT] New Login Service

de

- [shop] Überschriften sind für den Infotext im Shop zulässig
- [shop] "Rubrik" umbenannt in "Rubriken", Farbiger Selektor für den Filter
- [core][orders] Status für Reservierungen
- [core][catalog][shop] Untertitel für Bücher hinzugefügt
- [core] Import und Export entfernt
- [core] Rubriken im Shop korrigiert, sodass die globalen Einstellungen zum Sortieren berücksichtigt werden
- [core][catalog] Directory ist jetzt stabil
- [catalog][EXPERIMENT] Neue Suche nach Autor*innen
- [shop] Größere Schrift und Filter Label für Filter
- [core][catalog][orders][DEPRECATION] Datum und Uhrzeit bei Reservierungen sind jetzt veraltet
- [accounts][EXPERIMENT] Neuer Login Service

## v42

en

- [orders][settings] Upgrade @baldeweg/ui
- [orders][settings][deprecation] Env var VUE_APP_I18N_FALLBACK_LOCALE removed
- [catalog] Modal can be closed with esc key
- [shop] Filter by genre
- [core] Spaces before and after search term are ignored
- [orders] Rename created_at to reserved_on
- [settings] Save settings with empty content
- [orders] Customer details will appear after click
- [order] Change style to better differentiate between reservations

de

- [orders][settings] Upgrade @baldeweg/ui
- [orders][settings][deprecation] Env var VUE_APP_I18N_FALLBACK_LOCALE entfernt
- [catalog] Modal kann mit ESC geschlossen werden
- [shop] Filtern nach Rubrik
- [core] Leerzeichen vor und nach dem Suchbegriff werden ignoriert
- [orders] Angelegt am umbenannt in Reserviert am
- [settings] Einstellungen können gespeichert werden wenn Content leer ist
- [orders] Kundeninformationen sind erst nach einem Klick sichtbar
- [orders] Design angepasst, um besser zwischen Reservierungen unterscheiden zu können.

## v41

- [deprecation] Staff list removed
- [deprecation] Reservation without books not possible anymore
- [shop] Hyphens instead of word break for book titles
- [catalog] Option in directory to use the description
- [catalog] Add reset button for catalogue
- [catalog][orders][settings] Version and changelog in footer
- [shop] Behaviour of content changed. HTML won't get removed beforehand.
Instead, HTML will get sanitized after Markdown was parsed. Only a few HTML tags
are allowed. In fact it's now possible to write HTML and Markdown.

## v40

- New UI library
- Improvements and Fixes
- [catalog] Modal for catalogue won't get closed if clicked outside, only buttons will work.
- [catalog] Fix search using the latest term
- [catalog] Fix branch id in search
- [shop] Fix presentation issues of pagination for mobile devices
- [core] Restrict deleting of objects in directory to admins
- [deprecation] staff list
- [deprecation] reservation without books

## v39

- Now you can add your own content to the shop's homepage. The settings can be found under branch settings.
- [catalog][EXPERIMENT] docx files are allowed in the directory; Image-Preview
- More input fields for reservations.
- [settings][orders][catalog] Add new env var `VUE_APP_CATALOG` with the url to catalog
- [settings][orders][catalog] Add new env var `VUE_APP_SETTINGS` with the url to settings
- [settings][orders][catalog] Add new env var `VUE_APP_ORDERS` with the url to orders
- [catalog] Catalogue modal won't forget the input after closing, as long as the user stays on the search view.
- [catalog] Added more test cases
- [catalog][settings][orders] Changed navigation structure
- [orders] Mark reservations older than 14 days
- [shop] Reworked checkout process
- Improvements and Bugfixes

## v38

- [shop] Filiale nicht mehr auswählbar (ID ist jetzt in Environment Variable)
- [shop]  Code verbessert; Änderungen in URL Struktur (Unterverzeichnis, "book" heisst jetzt "article")
- [shop] Das "find" Projekt heißt jetzt "shop". Der Name beschreibt den Zweck besser.
- [docu] Dokumentation überarbeitet https://github.com/incwadi-warehouse/docu/tree/38
- [catalog] EXPERIMENT Design im Verzeichnis verbessert, Objekte können gelöscht werden, Ordner können angelegt werden, Bilder lassen sich hochladen. Jede Filiale hat ein eigenes Unterverzeichnis, nur dort dürfen Nutzer Änderungen vornehmen.
- [shop] Sortierung der Bücher in Suche geändert. Die Neuesten werden immer als erstes gezeigt.
- [catalog] Die Benachrichtigung über aktuelle Reservierungen befindet sich jetzt oben rechts.
