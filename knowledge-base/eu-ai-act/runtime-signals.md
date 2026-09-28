# Laufzeitsignale und Eskalation

## Warum KI-Systeme eigene Beobachtung brauchen

Klassische Überwachung fragt: Läuft der Dienst? Antwortet er schnell genug? Ein KI-System kann beide Fragen mit Ja beantworten und trotzdem seit Wochen falsch liegen. Die Verschlechterung zeigt sich nicht in der Verfügbarkeit, sondern in der Qualität der Ergebnisse — und die misst niemand, der nur die Infrastruktur beobachtet.

Ein Laufzeitsignal ist deshalb kein Alarm, sondern eine **dokumentierte Beobachtung**: Ein Messwert hat einen vorher festgelegten Schwellenwert über- oder unterschritten.

## Fünf Kategorien

| Kategorie | Was beobachtet wird | Typischer Auslöser |
|---|---|---|
| **Drift** | Verschiebung der Eingabedaten gegenüber den Trainingsdaten | Verteilung weicht messbar ab |
| **Verzerrung** | Ungleiche Ergebnisse über Gruppen hinweg | Kennzahl je Gruppe überschreitet Toleranz |
| **Leistung** | Trefferquote, Fehlerrate, Konfidenz | Genauigkeit fällt unter Schwelle |
| **Sicherheit** | Angriffe auf das Modell | Prompt Injection, Extraktionsversuche, auffällige Zugriffsmuster |
| **Betrieb** | Verfügbarkeit, Latenz, Kosten | Zeitüberschreitungen, Ausfall eines Anbieters |

Die ersten drei Kategorien sind die, die ohne bewusste Messung unsichtbar bleiben. Die letzten beiden fallen meist ohnehin auf.

## Vier Schweregrade

| Grad | Bedeutung | Erwartete Reaktion |
|---|---|---|
| **Hinweis** | auffällig, unterhalb der Handlungsschwelle | festhalten, beobachten |
| **Warnung** | Schwelle überschritten, Wirkung unklar | binnen Frist prüfen, Zuständigen benennen |
| **Hoch** | Wirkung wahrscheinlich | Vorfall anlegen, Neubewertung auslösen |
| **Kritisch** | Wirkung eingetreten oder unmittelbar | sofort eindämmen, Stopp prüfen |

Bei **hoch** und **kritisch** entsteht im Modell automatisch ein Auslöser für die Neubewertung mit einer Frist von sieben Tagen, sofern nicht bereits ein gleichwertiger offener Auslöser besteht. Das verhindert, dass ein gravierendes Signal zwar behoben, die Risikoeinstufung des Systems aber nie überprüft wird.

## Lebenszyklus eines Signals

```
offen  →  anerkannt  →  eingedämmt  →  erledigt
```

- **offen** — erfasst, noch niemandem zugeordnet
- **anerkannt** — jemand hat die Verantwortung übernommen; ab hier läuft die Bearbeitungszeit
- **eingedämmt** — die Wirkung ist begrenzt, die Ursache noch nicht beseitigt
- **erledigt** — Ursache behoben, Wirksamkeit bestätigt

Der Schritt von *eingedämmt* zu *erledigt* ist der, den Organisationen am häufigsten überspringen. Er verlangt die Bestätigung, dass die Maßnahme gewirkt hat — nicht nur, dass sie ergriffen wurde.

## Wann ein Signal zum Vorfall wird

Nicht jedes Signal ist ein Vorfall. Die Schwelle liegt dort, wo eine der folgenden Fragen mit Ja beantwortet wird:

- Sind daraus bereits **Entscheidungen über Menschen** getroffen worden?
- Ist die **dokumentierte Zweckbestimmung** des Systems nicht mehr erfüllt?
- Wird eine **Zusage an Kunden oder Aufsicht** verletzt?
- Ist die Ursache **außerhalb der normalen Schwankung** des Systems?

Bleibt es bei Nein, genügt die Dokumentation des Signals. Wichtig ist, dass die Entscheidung festgehalten wird — auch die gegen einen Vorfall.

## Schwellenwerte festlegen

Ein Signal ohne vorher festgelegten Schwellenwert ist eine Meinung. Für jede beobachtete Kennzahl gehört dokumentiert:

- der Messwert und wie er erhoben wird
- die Schwelle und **warum sie dort liegt**
- wer sie festgelegt hat und wann sie zuletzt geprüft wurde
- was bei Überschreitung geschieht

Die Begründung der Schwelle ist der Teil, nach dem in einer Prüfung gefragt wird. „So war es voreingestellt" ist keine.

## Verknüpfung

Jedes Signal kann auf einen Vorfall, eine Korrekturmaßnahme und einen Auslöser zur Neubewertung verweisen. Diese Verknüpfung ist der eigentliche Nachweis: Sie zeigt, dass aus einer Beobachtung eine Handlung wurde und dass diese Handlung ein Ende hatte.

Ein Bestand aus Signalen ohne Verknüpfungen belegt, dass beobachtet wurde — nicht, dass reagiert wurde.

---

Weiter: [Schwerwiegende Vorfälle](./serious-incidents.md) · [Änderungen und Neubewertung](./change-and-reassessment.md)

Die Angaben stellen keine Rechtsberatung dar. Primärquelle ist Verordnung (EU) 2024/1689 in der jeweils geltenden Fassung.
