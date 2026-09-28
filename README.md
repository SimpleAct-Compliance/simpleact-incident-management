# Incident Management für KI-Systeme

**Betriebsmodell für Vorfälle, Post-Market-Monitoring und Korrekturmaßnahmen nach EU AI Act** — von der Laufzeitbeobachtung über den Vorfall bis zur Neubewertung.

*An operating model for AI incident handling under the EU AI Act: runtime signals, incident records, corrective actions and reassessment.*

---

## Worum es geht

Die meisten Organisationen haben ein Incident-Verfahren für IT-Störungen. Für KI-Systeme reicht das nicht: Ein Modell fällt nicht aus, es wird langsam schlechter. Drift, Verzerrung und veränderte Datenlage erzeugen keine Fehlermeldung, sondern schleichend falsche Ergebnisse — und genau darauf zielen die Beobachtungspflichten nach Art. 72 und die Meldepflicht für schwerwiegende Vorfälle nach Art. 73.

Dieses Repository beschreibt ein Verfahren, das beides zusammenbringt: technische Beobachtung und regulatorische Nachweispflicht.

## Für wen

| Rolle | Was hier nützt |
|---|---|
| **Compliance und Recht** | Abgrenzung schwerwiegender Vorfälle, Meldewege, Nachweisführung |
| **Datenschutzbeauftragte** | Abgrenzung zur Datenschutzverletzung nach Art. 33 DSGVO |
| **Engineering und MLOps** | Signal-Kategorien, Schwellenwerte, Änderungsregister, Rollback-Kriterien |
| **Geschäftsführung** | Wer entscheidet über Stopp, Rückruf und Meldung |

## Das Modell in vier Stufen

```
Laufzeitsignal  →  Vorfall  →  Korrekturmaßnahme  →  Neubewertung
(Signal)           (Incident)   (CAPA)                (Reassessment)
```

Jede Stufe ist eigenständig dokumentiert und mit der nächsten verknüpft. Ein Signal muss nicht zum Vorfall werden; ein Vorfall muss nicht meldepflichtig sein. Entscheidend ist, dass die Einstufung bewusst getroffen und begründet festgehalten wird — das ist der Teil, den eine Prüfung sehen will.

**Signalkategorien:** Drift · Verzerrung · Leistung · Sicherheit · Betrieb
**Schweregrade:** Hinweis · Warnung · Hoch · Kritisch
**Vorfallstatus:** offen · anerkannt · eingedämmt · geschlossen

## Inhalt

| Dokument | Inhalt |
|---|---|
| [Post-Market-Monitoring](./knowledge-base/eu-ai-act/post-market-monitoring.md) | Beobachtungspflicht nach Art. 72, was ein Plan enthalten muss |
| [Schwerwiegende Vorfälle](./knowledge-base/eu-ai-act/serious-incidents.md) | Abgrenzung nach Art. 73, Meldeweg, Abgrenzung zur DSGVO |
| [Laufzeitsignale und Eskalation](./knowledge-base/eu-ai-act/runtime-signals.md) | Kategorien, Schwellenwerte, wann ein Signal zum Vorfall wird |
| [Änderungen und Neubewertung](./knowledge-base/eu-ai-act/change-and-reassessment.md) | Wesentliche Änderung, Testfreigabe, Auslöser für Neubewertung |
| [Vorlage: Vorfallakte](./templates/incident-record.md) | Zum Ausfüllen |
| [Vorlage: Korrekturmaßnahme](./templates/capa-action.md) | Zum Ausfüllen |

## In Software umsetzen

Das Verfahren lässt sich in Tabellen führen. Wer es nicht will, findet es in [SimpleAct](https://simpleact.de) umgesetzt — Signale, Vorfälle, Korrekturmaßnahmen und Änderungsregister verknüpft, mit durchgängigem Audit-Trail: **[Incident Management](https://simpleact.de/incident-management)**

## Mitwirken

Korrekturen und Ergänzungen sind willkommen, siehe [CONTRIBUTING.md](./CONTRIBUTING.md). Besonders hilfreich sind Erfahrungen aus echten Vorfällen und Prüfungen.

## Stand und Lizenz

Zuletzt aktualisiert: 2026-09-28

MIT — frei nutzbar, auch kommerziell. Die Inhalte stellen keine Rechtsberatung dar und ersetzen keine Prüfung des Einzelfalls.
