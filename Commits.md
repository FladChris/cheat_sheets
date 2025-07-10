# Conventional Commits Cheat Sheet

## Format

    <type>(<scope>): <short description>

- type: Art der Änderung (z. B. feat, fix, refactor …)  
- scope: Betroffene Komponente oder Modul (z. B. backend, db, api …)  
- short description: Prägnante Gegenwartsform, kein Punkt am Ende  

## Types

| Type      | Beschreibung                                                |
|-----------|-------------------------------------------------------------|
| `feat`      | Für neue Features, die das Verhalten erweitern.             |
| `fix`       | Für Bugfixes, die Fehler im bestehenden Verhalten beheben.  |
| `refactor`  | Für Code-Umstrukturierungen ohne Verhaltensänderung.        |
| `perf`      | Für Performance-Verbesserungen ohne neue Features.          |
| `docs`      | Für Änderungen an der Dokumentation.                        |
| `style`     | Für reine Formatierungs- oder Style-Anpassungen (Linting).  |
| `test`      | Für Hinzufügen oder Anpassen von Tests.                     |
| `build`     | Für Änderungen am Build-System oder an Abhängigkeiten.      |
| `ci`        | Für CI/CD-Konfigurationsänderungen.                         |
| `chore`     | Für sonstige Maintenance-Aufgaben, die in keine andere Kategorie passen. |

## Scopes

| Scope       | Beschreibung                                           |
|-------------|--------------------------------------------------------|
| `backend`     | Server-seitige Logik, Business-Layer, Services         |
| `db`          | Datenbankschema, Migrationen, SQL-Skripte              |
| `api`         | REST- oder GraphQL-Endpunkte                           |
| `auth`        | Authentifizierungs- und Autorisierungslogik            |
| `ui / frontend` | Benutzeroberfläche, CSS, JavaScript im Browser      |
| `config`      | Konfigurationsdateien (z. B. .env, YAML, JSON)         |
| `scripts`     | Hilfsskripte, Code-Generatoren, Automatisierungen      |
| `tests`       | Test-Skripte, Unit-Tests, Integrationstests            |



## Beispiele

- feat(db): add migration for user_roles table  
- fix(backend): correct null pointer in OrderService  
- refactor(api): split UserController into smaller modules  
- perf(db): optimize index usage on transactions  
- docs: update README with deployment steps  
- style(ui): apply Prettier formatting  
- test(auth): add unit tests for login flow  
- build: upgrade webpack to v5  
- ci: add GitHub Actions workflow for tests  
- chore(scripts): remove deprecated codegen script  

## Kurze Faustregeln

- Immer fix, wenn ein tatsächlicher Fehler behoben wird.  
- Immer feat, wenn ein neues, sichtbares Feature hinzugefügt wird.  
- refactor, wenn nur die Struktur verbessert wird.  
- chore, wenn es keine andere passende Kategorie gibt.  
- Kombiniere Type und Scope, um den Commit sofort verständlich zu machen.  
