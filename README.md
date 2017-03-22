# Vaadin 8 Unofficial migration guide

Below you’ll find list of Vaadin (UI server) components and changed API that I found (most of them aren’t described in changelogs). I plan to update the list during my exercise to upgrade a project to Vaadin version 8 from previous one (to be precised I migrate to 8.0.3 from 7.7.6).

### TextField
7 | 8
------------ | -------------
setRequired() | setRequiredIndicatorVisible()
setColumns(x) | setWidth(x, Unit.REM)
setInputPrompt() | setPlaceholder()
