# Unveränderlichkeit in C#: `const` und `readonly`

| Merkmal                        | `const`                                                                              | `readonly`                                                                                            |
| ------------------------------ | ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| **Bedeutung**                  | Kompilezeit-Konstante: Wert steht zur Compilezeit fest und kann sich nie ändern.     | Laufzeit-Konstante: Wert wird zur Laufzeit festgelegt, danach nicht mehr änderbar.                    |
| **Initialisierung**            | Muss sofort beim Deklarieren festgelegt werden.                                      | Kann im Konstruktor oder bei der Deklaration festgelegt werden.                                       |
| **Zeitpunkt der Bindung**      | Compile-Time (fester Wert im Code eingebettet).                                      | Run-Time (Wert erst beim Erzeugen des Objekts bekannt).                                               |
| **Gültig für**                 | Nur statische (class-level) Werte.                                                   | Kann instanzbezogen oder statisch sein.                                                               |
| **Zulässige Typen**            | Nur einfache Typen (z. B. `int`, `double`, `bool`, `string`, `enum`).                | Alle Typen (auch komplexe Objekte).                                                                   |
| **Verwendung**                 | Für feste Werte, die sich nie ändern (z. B. `PI`, `DaysInWeek`).                     | Für Werte, die beim Start oder im Konstruktor bestimmt werden (z. B. Seriennummer, Erstellungsdatum). |
| **Änderbar nach Zuweisung**    | Nein, nie.                                                                           | Nein, nach Zuweisung im Konstruktor ebenfalls nicht.                                                  |
| **Beispiel**                   | `public const double Pi = 3.14159;`                                                  | `public readonly DateTime Created = DateTime.Now;`                                                    |
| **Statisch / Instanzabhängig** | Immer implizit `static`.                                                             | Kann `static` oder instanzbasiert sein.                                                               |
| **Typische Verwendung**        | Mathematische Konstanten, feste Werte.                                               | Werte, die pro Objekt unterschiedlich, aber unveränderlich sind.                                      |
