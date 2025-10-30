# Vererbung in C#

| Keyword                           | Bedeutung / Verwendung                                                                               | Beispiel                                                                    |
| --------------------------------- | ---------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `class`                           | Deklariert eine Klasse. Kann Basis- oder abgeleitete Klasse sein.                                    | `class Car : Vehicle { }`                                                   |
| `:` (Doppelpunkt)                 | Leitet eine Klasse von einer anderen Klasse oder Interfaces ab.                                      | `class Car : Vehicle, IDrivable { }`                                        |
| `base`                            | Zugriff auf Member oder Konstruktor der Basisklasse.                                                 | `base.StartEngine()`, `: base(speed)`                                       |
| `this`                            | Verweis auf die aktuelle Instanz (nicht spezifisch für Vererbung, aber oft im Kontext).              | `this.Model = model;`                                                       |
| `virtual`                         | Markiert eine Methode als überschreibbar (ermöglicht Polymorphismus).                                | `public virtual void Drive() { }`                                           |
| `override`                        | Überschreibt eine `virtual` oder `abstract` Methode aus der Basisklasse.                             | `public override void Drive() { Console.WriteLine("Car drives"); }`         |
| `new`                             | Verdeckt (versteckt) eine geerbte Methode (keine echte Überschreibung).                              | `public new void Drive() { Console.WriteLine("New drive method"); }`        |
| `sealed`                          | Verhindert weitere Vererbung (bei Klassen) oder weiteres Überschreiben (bei Methoden).               | `sealed class SportsCar { }` oder `public sealed override void Drive() { }` |
| `abstract`                        | Erzwingt, dass abgeleitete Klassen die Methode überschreiben (keine Implementierung in Basisklasse). | `public abstract void Refuel();`                                            |
| `interface`                       | Definiert einen Vertrag (Signaturen ohne Implementierung).                                           | `interface IDrivable { void Drive(); }`                                     |
| `protected`                       | Zugriffsschutz: sichtbar in der Klasse und ihren Unterklassen.                                       | `protected int Speed;`                                                      |
| `public` / `private` / `internal` | Steuern Sichtbarkeit über Klassen- und Assemblygrenzen hinweg.                                       | `private void StartEngine();`                                               |
| `sealed override`                 | Kombi: Methode wird überschrieben, aber darf nicht mehr weiter überschrieben werden.                 | `public sealed override void Drive() { }`                                   |
| `abstract class`                  | Klasse, die nicht instanziierbar ist, aber Vererbung vorgibt.                                        | `abstract class Vehicle { public abstract void Drive(); }`                  |
| `partial`                         | Nicht direkt Vererbung, aber erlaubt Klassendefinition über mehrere Dateien.                         | `partial class Vehicle { }`                                                 |
| `object`                          | Oberste Basisklasse aller Typen in C#.                                                               | `class Car { } // implicitly inherits from object`                          |
