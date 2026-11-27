# Schwerwiegende Vorfälle nach Art. 73 EU AI Act

## Warum das eine eigene Kategorie ist

Ein schwerwiegender Vorfall im Sinne des Art. 73 ist keine schlimmere Störung, sondern eine **eigene Rechtsklasse** mit eigener Meldepflicht gegenüber der Marktüberwachungsbehörde. Wer sie im allgemeinen Incident-Prozess mitlaufen lässt, merkt im Zweifel zu spät, dass eine Meldung fällig war.

Deshalb gilt in diesem Modell: Die Einstufung „schwerwiegender Vorfall" ist ein **eigenes Feld**, das bewusst gesetzt wird – nicht ein hoher Schweregrad, aus dem sich die Meldepflicht ableiten ließe. Ein kritischer Betriebsausfall kann unerheblich sein, ein unscheinbares Fehlverhalten kann meldepflichtig sein.

## Ab wann die Meldepflicht greift

Art. 73 steht in Kapitel IX der Verordnung, das seit dem 2.8.2026 anwendbar ist. Meldepflichtig nach Art. 73 ist der Anbieter eines **Hochrisiko-KI-Systems** (zu den Betreibern siehe unten), und die Einstufungsregeln für Hochrisiko gelten nach dem Digital Omnibus (Verordnung (EU) 2026/1744) für Anhang III erst ab dem **2.12.2027** und für Anhang I ab dem **2.8.2028**. Praktisch wird die Meldepflicht also mit diesen Daten relevant. Wer den Vorfallprozess jetzt aufbaut, hat Zeit, ihn zu üben.

Betreiber, die einen schwerwiegenden Vorfall feststellen, informieren unverzüglich zuerst den Anbieter und dann den Einführer oder Händler und die zuständigen Marktüberwachungsbehörden (Art. 26 Abs. 5). Die Behörde erfährt vom Vorfall also auch dann durch den Betreiber, wenn der Anbieter erreichbar ist. Kann der Betreiber den Anbieter nicht erreichen, gilt Art. 73 für ihn entsprechend (Art. 26 Abs. 5).

## Was einen Vorfall schwerwiegend macht

Art. 3 Nr. 49 definiert den schwerwiegenden Vorfall über die Folge, nicht über die technische Ursache. Erfasst sind Vorfälle, die mittelbar oder unmittelbar führen zu:

- dem Tod oder einer schweren Gesundheitsschädigung einer Person
- einer schweren und unumkehrbaren Störung der Verwaltung oder des Betriebs kritischer Infrastruktur
- einem Verstoß gegen Unionsrecht zum Schutz der Grundrechte
- einem schweren Schaden an Sachen oder Umwelt

Die Prüffrage lautet also nicht „wie schlimm war der Ausfall", sondern **„was ist Menschen, Grundrechten oder kritischer Infrastruktur dadurch geschehen"**.

## Meldung

Die Meldung geht an die Marktüberwachungsbehörde des Mitgliedstaats, in dem der Vorfall eingetreten ist.

**Zur Frist:** Art. 73 kennt drei Höchstfristen, die alle ab Kenntnis des Vorfalls laufen. Gemeldet wird unmittelbar, sobald der Zusammenhang mit dem KI-System feststeht oder wahrscheinlich ist, spätestens aber:

| Fall | Höchstfrist |
|---|---|
| Regelfall (Art. 73 Abs. 2) | 15 Tage |
| Tod einer Person (Art. 73 Abs. 4) | 10 Tage |
| Schwere und unumkehrbare Störung kritischer Infrastruktur (Art. 3 Nr. 49 lit. b) oder weitverbreiteter Verstoß (Art. 73 Abs. 3) | 2 Tage |

**Diese Fristen gehören vor jeder Meldung am aktuellen Verordnungstext geprüft**, nicht aus einer Vorlage übernommen: Änderungsverordnungen können sie verschieben, und eine falsch berechnete Frist ist als Verstoß eigenständig sanktionierbar.

Aus demselben Grund berechnet SimpleAct diese Frist bewusst **nicht** automatisch, sondern verlangt eine bewusste Eingabe. Eine automatisch gesetzte Frist, der jemand vertraut, ist gefährlicher als gar keine.

## Abgrenzung zur Datenschutzverletzung

Beide Pflichten können gleichzeitig greifen, folgen aber unterschiedlicher Logik:

| | Art. 73 EU AI Act | Art. 33 DSGVO |
|---|---|---|
| Auslöser | Folge für Leben, Gesundheit, Grundrechte, kritische Infrastruktur | Verletzung des Schutzes personenbezogener Daten |
| Adressat | Marktüberwachungsbehörde | Datenschutzaufsichtsbehörde |
| Frist | 15, 10 oder 2 Tage ab Kenntnis, je nach Fall | 72 Stunden ab Kenntnis |
| Betroffenenbenachrichtigung | nicht unmittelbar vorgesehen | bei hohem Risiko, Art. 34 |

**Ein Vorfall kann beides sein.** Ein fehlerhaftes Bewerbungs-Screening, das diskriminiert und dabei unbefugt Daten offenlegt, löst beide Wege aus. Die Vorfallakte sollte deshalb beide Einstufungen getrennt führen, damit keine der beiden Fristen an der anderen hängt.

## Was in die Akte gehört

Die Meldung ist der sichtbare Teil; nachgewiesen werden muss das Verfahren dahinter:

- **Zeitpunkte:** Eintritt, Entdeckung, Kenntnisnahme durch die verantwortliche Stelle. Die Frist läuft ab Kenntnis, nicht ab Eintritt – dieser Unterschied muss dokumentiert sein.
- **Einstufung** mit Begründung, auch wenn sie *gegen* eine Meldepflicht ausfällt. Eine begründete Nicht-Meldung ist verteidigbar, eine unbegründete nicht.
- **Betroffenes System** mit Version, Modellstand und Datenstand zum Zeitpunkt des Vorfalls.
- **Sofortmaßnahmen:** Abschaltung, Rückfall auf menschliche Entscheidung, Rollback.
- **Ursachenanalyse** und daraus abgeleitete Korrekturmaßnahme.
- **Entscheider** je Schritt.

## Häufige Fehler

**Die Einstufung wird nachträglich getroffen.** Wer erst bei der Aufarbeitung entscheidet, ob der Vorfall schwerwiegend war, hat die Frist bereits laufen lassen. Die Einstufung gehört an den Anfang, mit dem Recht, sie später begründet zu ändern.

**Der Zeitpunkt der Kenntnis wird nicht festgehalten.** Ohne ihn lässt sich die Fristwahrung nicht belegen – und die Beweislast liegt beim Verantwortlichen.

**Kein Weg für Meldungen von außen.** Vorfälle fallen oft Nutzern auf, nicht dem Betreiber. Wenn es keinen Kanal gibt, über den eine Beschwerde im Vorfallprozess landet, endet sie im Support-Postfach.

**Nur der Anbieter fühlt sich zuständig.** Betreiber haben nach Art. 26 eigene Pflichten, unter anderem die Unterrichtung des Anbieters und die Beobachtung des Betriebs. Wer ein KI-System einkauft, ist nicht aus der Verantwortung.

---

Weiter: [Post-Market-Monitoring](./post-market-monitoring.md) · [Laufzeitsignale](./runtime-signals.md) · [Vorlage: Vorfallakte](../../templates/incident-record.md)

Die Angaben geben den Stand November 2026 wieder und stellen keine Rechtsberatung dar. Primärquelle ist Verordnung (EU) 2024/1689 in der Fassung der Verordnung (EU) 2026/1744.
