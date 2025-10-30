# `struct` vs. `class`

| Merkmal                 | `class`                                | `struct`                                                       |
| ----------------------- | -------------------------------------- | -------------------------------------------------------------- |
| **Typkategorie**        | Referenztyp                            | Werttyp                                                        |
| **Speicherort**         | Heap                                   | Stack                                                          |
| **Zuweisung**           | Kopiert Referenz                       | Kopiert gesamten Wert                                          |
| **Vererbung**           | Erlaubt (außer `sealed`)               | Nicht erlaubt                                                  |
| **Null-Wert**           | Kann `null` sein                       | Nur als `Nullable<T>` (`Point?`)                               |
| **Default-Konstruktor** | Erlaubt (kann selbst definiert werden) | Automatisch vorhanden, darf nicht selbst definiert werden      |
| **Lebensdauer**         | Vom Garbage Collector verwaltet        | Automatisch beim Verlassen des Scopes                          |
| **Beispielverwendung**  | Komplexe Objekte mit Verhalten         | Kleine, unveränderliche Datentypen (z. B. `Point`, `DateTime`) |
