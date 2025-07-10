# Pytest Cheat Sheet

### Installation & Setup

| Befehl                   | Beschreibung                 |
| ------------------------ | ---------------------------- |
| `pip install pytest`     | pytest installieren          |
| `pip install pytest-cov` | Coverage-Plugin installieren |

### Test-Ausführung

| Befehl                        | Beschreibung                            |
| ----------------------------- | --------------------------------------- |
| `pytest`                      | Alle Tests im Projekt ausführen         |
| `pytest -v`                   | Tests mit ausführlicher Ausgabe         |
| `pytest -q`                   | Tests mit kompaktem Bericht             |
| `pytest -x`                   | Nach erstem Fehler abbrechen            |
| `pytest --maxfail=3`          | Abbruch nach drei Fehlern               |
| `pytest -k "<expression>"`    | Tests nach Namensfragment filtern       |
| `pytest -m "<marker>"`        | Tests mit spezifischem Marker ausführen |
| `pytest tests/test_module.py` | Tests in bestimmter Datei ausführen     |
| `pytest tests/unit/`          | Tests in einem Verzeichnis ausführen    |

### Assertions

| Befehl                           | Beschreibung                        |
| -------------------------------- | ----------------------------------- |
| `assert expr`                    | Ausdruck prüfen                     |
| `with pytest.raises(Exception):` | Erwartetes Auslösen einer Exception |

### Fixtures

| Befehl                   | Beschreibung                                     |
| ------------------------ | ------------------------------------------------ |
| `@pytest.fixture`        | Fixture definieren                               |
| `def fixture_name(...):` | Fixture-Funktion deklarieren                     |
| `autouse=True`           | Automatische Anwendung der Fixture               |
| `scope="module"`         | Fixture-Scope (function, module, class, session) |

### Parametrisierung

| Befehl                                            | Beschreibung                       |
| ------------------------------------------------- | ---------------------------------- |
| `@pytest.mark.parametrize("arg,expected", [...])` | Parameterisierte Tests definieren  |
| `params=[...]`                                    | Indirekte Fixture-Parametrisierung |

### Marker & Skip/Xfail

| Befehl                             | Beschreibung                   |
| ---------------------------------- | ------------------------------ |
| `@pytest.mark.skip(reason="...")`  | Test überspringen              |
| `@pytest.mark.xfail(reason="...")` | Erwartetes Scheitern markieren |

### Reports & Coverage

| Befehl                                     | Beschreibung                   |
| ------------------------------------------ | ------------------------------ |
| `pytest --cov=<package>`                   | Coverage messen                |
| `pytest --cov=<package> --cov-report=html` | HTML-Coverage-Bericht erzeugen |
| `pytest --junitxml=report.xml`             | JUnit-XML-Report erstellen     |
