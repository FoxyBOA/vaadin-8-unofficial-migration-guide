# Vaadin 8 Unofficial migration guide

## What it's all about
Below you’ll find list of Vaadin version 8 (UI server) components changed API that I found (most of them aren’t described in changelogs). Purpose of the document is not to duppliate Vaadin team effort (i.e. I don't plan to put here info regarding changed data binding API), but to add missing parts.
I plan to update the document during my exercise to upgrade a project to Vaadin version 8 from previous one (to be precised from 7.7.6 to 8.0.3 ).

### TextField
7 | 8
------------ | -------------
setRequired() | setRequiredIndicatorVisible()
setColumns(x) | setWidth(x, Unit.REM)
setInputPrompt() | setPlaceholder()

### PasswordField
changed parent class ```AbstractTextField``` -> ```TextField```

### ComboBox
7 | 8
------------ | -------------
setNullSelectionAllowed() | setEmptySelectionAllowed()

### DateField
```getDate()``` return ```LocalDate``` instead of ```java.util.Date```. The simplest way to convert is ```java.sql.Date.valueOf(dateField.getValue())```

### VerticalLayout
7 | 8
------------ | -------------
```marging``` is false by default | true
