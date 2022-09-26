# Changelog

## v44

en

- [core][catalog] Show number of open reservations in alert
- [catalog][settings][shop][orders] Update UI library @baldeweg/ui
- [core] Update flex recipes
- [api-bundle][DEPRECATION] Remove response from controller
- [api-bundle][DEPRECATION] Remove transformer from serializer

de

- [core][catalog] Zeige Zahl offener Reservierungen in Benachrichtigung
- [catalog][settings][shop][orders] UI Library @baldeweg/ui aktualisiert
- [core] Flex Recipes aktualisiert
- [api-bundle][DEPRECATION] Response from API Controller entfernt
- [api-bundle][DEPRECATION] Transformer von Serializer entfernt

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
