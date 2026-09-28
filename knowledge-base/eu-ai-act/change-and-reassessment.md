# Änderungen und Neubewertung

## Warum Änderungen eine eigene Akte brauchen

Ein KI-System ist selten dasselbe wie vor sechs Monaten. Modelle werden ausgetauscht, Schwellen justiert, Datenquellen ergänzt, Anbieter aktualisieren ihre Dienste ohne Rückfrage. Jede dieser Änderungen kann die Grundlage entwerten, auf der das System einmal bewertet und freigegeben wurde.

Deshalb gehört neben die Vorfallakte ein **Änderungsregister**: Es hält fest, was sich wann geändert hat, ob es geprüft wurde und ob daraus eine Neubewertung folgt.

## Der Ablauf

```
erkannt  →  in Prüfung  →  freigegeben  →  ausgerollt
                      ↘  abgelehnt
```

Zu jeder Änderung gehören:

- **Art der Änderung** — Modell, Daten, Schwellenwert, Zweck, Anbieter, Konfiguration
- **Risikoeinstufung** der Änderung selbst — niedrig bis kritisch
- **Teststatus** — nicht geprüft, bestanden, gescheitert
- **Versionen** — Modell, Datenstand, Release
- **Zwei Kennzeichen:** löst diese Änderung eine Neubewertung aus, und braucht sie eine Korrekturmaßnahme

Die beiden Kennzeichen sind der Kern. Sie zwingen zu einer bewussten Antwort auf die Frage, ob eine Änderung folgenlos bleibt — statt sie stillschweigend zu unterstellen.

## Wesentliche Änderung

Nicht jede Änderung ist rechtlich erheblich. Erheblich wird sie, wenn sie die Zweckbestimmung berührt oder die Konformität beeinflusst. Als Prüffragen taugen:

- Ändert sich der **Zweck** oder der Anwendungsbereich?
- Ändert sich die **Personengruppe**, über die entschieden wird?
- Ändert sich die **Eingriffstiefe** — etwa von Vorschlag zu automatischer Entscheidung?
- Ändert sich das **zugrundeliegende Modell** oder dessen Trainingsdatenbasis wesentlich?
- Wird eine **Annahme** verletzt, auf der die ursprüngliche Risikoeinstufung beruhte?

Ein Ja bei einer dieser Fragen ist ein starkes Signal für eine Neubewertung — und bei Hochrisiko-Systemen gegebenenfalls für eine erneute Konformitätsbewertung.

## Der Sonderfall, der am häufigsten übersehen wird

**Der Anbieter ändert etwas, nicht Sie.** Ein zugekauftes Sprachmodell bekommt eine neue Version, ein Dienst ändert sein Verhalten, eine Schnittstelle wird abgekündigt. Für den Betreiber sieht das nach nichts aus — es gibt kein Ticket, keinen Release, keine Entscheidung.

Praktisch hilft nur:

- **Modell- und Dienstversion mitprotokollieren**, damit ein Wechsel überhaupt sichtbar wird
- **Änderungshinweise des Anbieters abonnieren** und in dasselbe Register einspeisen
- **Eine Kennzahl beobachten**, die auf Verhaltensänderung reagiert, nicht nur auf Verfügbarkeit

Wer die Anbieterversion nicht festhält, kann nach einem Vorfall nicht belegen, mit welchem Stand das System gearbeitet hat. Das ist der Punkt, an dem Aufarbeitung scheitert.

## Auslöser für eine Neubewertung

Eine Neubewertung wird fällig bei:

- einer wesentlichen Änderung wie oben
- einem Vorfall mit Schweregrad **hoch** oder **kritisch**
- einem Laufzeitsignal, das eine Annahme der Bewertung widerlegt
- Ablauf des regulären Prüfzyklus
- geänderter Rechtslage oder neuen Leitlinien

In diesem Modell erzeugt ein Vorfall der Stufe hoch oder kritisch den Auslöser automatisch, mit einer Frist von sieben Tagen. Die Frist ist bewusst kurz: Sie soll erzwingen, dass jemand hinsieht, nicht dass in einer Woche alles neu bewertet ist.

## Testfreigabe vor dem Ausrollen

Eine Änderung mit Teststatus *nicht geprüft* oder *gescheitert* sollte nicht in den Status *ausgerollt* wechseln können. Das ist die einfachste wirksame Sperre im ganzen Verfahren — und die, die am ehesten umgangen wird, wenn es eilt.

Wenn sie umgangen wird, gehört das dokumentiert: wer entschieden hat, mit welcher Begründung, und wann nachgeprüft wird.

---

Weiter: [Post-Market-Monitoring](./post-market-monitoring.md) · [Vorlage: Korrekturmaßnahme](../../templates/capa-action.md)

Die Angaben stellen keine Rechtsberatung dar. Primärquelle ist Verordnung (EU) 2024/1689 in der jeweils geltenden Fassung.
