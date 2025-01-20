---
lab:
  title: 'Lab 5: Generieren von Erkenntnissen'
---

# Lab 5: Generieren von Erkenntnissen 

In diesem Lab lernen Sie Folgendes:
- Generieren von Erkenntnissen zu Ihren Segmenten 
- Anzeigen von Unterscheidungsmerkmalen und Überlappungen zwischen Segmenten 
- Erstellen vorgeschlagener Segmente basierend auf einem Segment 

## Übung 1: Generieren von Erkenntnissen in Ihre Segmente
### Übung 1: Segment-Unterscheidungsmerkmale
Oft haben Sie Kundschaft, die in mehreren Segmenten vertreten ist. Es kann hilfreich sein zu verstehen, wann es zu Überlappungen zwischen ihnen kommen kann. Versuchen wir, gemeinsame Kundschaft zu finden, die sowohl zur **Kundschaft aus Texas** als auch zu den **Herbst-Schlussverkaufsaktion**-Segmenten gehört, und versuchen wir auch herauszufinden, was diese beiden Segmente in Bezug auf **Belohnungspunkte** und **LifetimeSpend** unterscheidet.

1. Wählen Sie **Erkenntnisse > Segmente** aus dem linken Navigationsmenü. Wählen Sie die Registerkarte **Erkenntnisse (Vorschau)** aus und klicken Sie in der Befehlsleiste auf **+ Neu**, oder klicken Sie auf die Schaltfläche **+ Neue Erkenntnis**.

1. Nun werden zwei Optionen angezeigt. Lassen Sie uns mit der Verwendung von **Unterscheidungsmerkmalen** beginnen, um zu sehen, was die beiden Segmente unterscheidet. Wählen Sie **Unterscheidungsmerkmale** aus.

1. Wählen Sie **Herbstausverkaufsaktion** als primäres Segment. Wählen Sie **Weiter** aus.

1. Wählen Sie **Kundschaft aus Texas** als weiteres Segment, und wählen Sie dann **Weiter**.

1. Wählen Sie nun **Belohnungspunkte** unter **Kundenfelder** und **LifetimeSpend** unter **Measurefelder**, um zu sehen, wie sich die oben genannten Segmente in Bezug auf **Belohnungspunkte** und **LifetimeSpend** voneinander unterscheiden. Löschen Sie alle anderen Kunden- und Measurefelder.

1. Wählen Sie **Weiter** und benennen Sie die Erkenntnis **Herbstaktion vs. Kundschaft aus Texas**.

1. Überprüfen Sie, ob der **Name der Ausgabeeinheit** auf **FallPromotionvsCustomersfromTexas** festgelegt ist. Wählen Sie **Speichern**.

1. Nachdem die Erkenntnis aktualisiert wurde, öffnen Sie die erstellte Erkenntnis. Wählen Sie die Registerkarten **Attribute** oder **Measures** aus, um zu sehen, wie sich die Segmente in Bezug auf die von Ihnen ausgewählten Felder voneinander unterscheiden. Beachten Sie die **Differenzbewertung**, die den Grad der Differenz angibt. Je höher die Punktzahl ist, desto unterschiedlicher sind sie.

1. Wählen Sie jedes Measure und Attribut aus, um tiefere Einblicke zu erhalten.

### Aufgabe 2: Segmentüberlappung
Nachdem wir nun erfolgreich eine Segment-Erkenntnis mit **Unterscheidungsmerkmalen** erstellt haben, erstellen wir nun eine Erkenntnis mit **Überlappungen**.

1. Vergewissern Sie sich, dass Sie sich noch auf der Registerkarte **Segmente > Erkenntnisse (Vorschau)** befinden, und wählen Sie **+ Neu** aus der Befehlsleiste aus. Wählen Sie **Überlappung** aus.

1. Wählen Sie die beiden Segmente **Herbstausverkaufsaktion** und **Kundschaft aus Texas**, um deren gemeinsame Kundschaft zu ermitteln.

1. Wählen Sie **Weiter** aus.

1. Nennen Sie das Segment **Herbstaktion-Kundschaft überlappt mit Kundschaft aus Texas** und stellen Sie sicher, dass der **Output-Tabellenname** auf **FallPromotionCustomersOverlappedwithTexasCustomers** festgelegt ist. Wählen Sie **Speichern**.

1. Nachdem die Aktualisierung der Erkenntnisse abgeschlossen ist, öffnen Sie die erstellten Erkenntnisse, um das Venn-Diagramm zu sehen, das die Gesamtzahl und den Prozentsatz der gemeinsamen Kundschaft dieser beiden Segmente anzeigt.

## Übung 2: Segmenterweiterung und vorgeschlagene Segmente
### Vorgang 1: Segmenterweiterung
Die Segmenterweiterung kann verwendet werden, um ähnliche Kundschaft wie Ihre Segmentkundenbasis mit künstlicher Intelligenz zu finden. Zuvor haben wir ein Segment mit dem Namen **Herbstaktion-Kundschaft** erstellt, das Kundschaft der Generation Y mit überdurchschnittlich hohen Einkäufen im Geschäft enthält. Nun wollen wir dieses Segment erweitern und Kundschaft finden, die uns ähnlich ist, um unseren neu eingeführten Cold Brew Coffee zu vermarkten.

1. Wählen Sie **Erkenntnisse > Segmente** aus dem linken Navigationsmenü und wählen Sie die Registerkarte **Alle Segmente**.

1. Wählen Sie das Segment **Herbstaktion-Kundschaft** aus. Dies wird zu unserem Quellsegment.

1. Wählen Sie **Ähnliche Kundschaft suchen** in der Befehlsleiste aus.

1. Benennen Sie Ihr Segment **FallPromoExpansion**.

1. Wählen Sie im nächsten Schritt **Felder hinzufügen**, um Attribute und Kennzahlen auszuwählen, die zum Finden ähnlicher Kundschaften verwendet werden. Wir zielen auf eine Kundschaft mit ähnlichem Standort und durchschnittlichem Einkauf im Geschäft ab, also wählen Sie **PostCode** und **AverageStorePurchase**. Wählen Sie **Übernehmen**.

1. Als Nächstes müssen Sie auswählen, wer berücksichtigt werden soll. Wählen Sie zunächst **Alle Kunden außer Quellsegment**.

1. Nun müssen Sie die maximale Anzahl der einzubeziehenden Kundschaften auswählen. Lassen Sie uns bei **20 %** bleiben.

1. Wenn Sie auch Mitglieder aus dem Quellsegment einschließen möchten, aktivieren Sie die letzte Option. Andernfalls lassen Sie es deaktiviert. Für unsere Zwecke können wir es deaktiviert lassen.

1. Klicken Sie auf **Ausführen**.

1. Nachdem die Aktualisierung des Segments abgeschlossen ist, öffnen Sie das Segment, um die **Ähnlichkeitsbewertungen** zu finden und die **Segmentmitglieder-Vorschau** zu erkunden.

### Aufgabe 2: Empfangen von Segmentvorschlägen 
Verwenden Sie „Vorgeschlagene Segmente“, um interessante Segmente basierend auf einem Kundenattribut oder einer Kennzahl von Interesse zu entdecken.

1. Wählen Sie **Erkenntnisse > Segmente** aus dem linken Navigationsmenü, und wählen Sie die Registerkarte **Vorschläge (Vorschau)** aus.

1. Wählen Sie **Vorschläge erhalten**, um die Konfiguration zu beginnen.

1. Wählen Sie **Measure/Metrik verbessern** und wählen Sie **Start**.

1. Wählen Sie unter **Measurefelder** als Zielattribut **LifetimeSpend** aus. Wählen Sie **Weiter** aus.

1. Als Nächstes wählen Sie die Attribute aus, die das Zielattribut (**LifetimeSpend**) beeinflussen könnten, damit das KI-Modell interessante Muster zwischen dem beeinflussenden und dem Zielattribut finden kann. Das Modell schlägt Segmente basierend auf diesen Mustern vor. Wählen Sie **E-Mail-Abonnent**, **Einkommen**, **Treuestufe**, **Beruf** und **Bundesland** als beeinflussende Attribute.

1. Klicken Sie auf **Ausführen**. Das KI-Modell beginnt mit der Suche nach Mustern zwischen den ausgewählten Einflussattributen und Zielattributen für Oberflächensegmentvorschläge. Warten Sie einige Minuten, bis das Modell die Analyse abgeschlossen hat.

1. Sobald das Modell seinen Lauf beendet hat und wenn es in der Lage ist, Muster zwischen den beeinflussenden Attributen und dem Zielattribut aufzudecken, werden Segmentvorschläge auf der Registerkarte **Vorschläge (Vorschau)** angezeigt.

1. Um das Segment zu speichern, wählen Sie **Als Segment speichern** im Bedienfeld **Vorgeschlagene Segmentdetails**. Wählen Sie **Speichern**.

1. Das gespeicherte Segment kann dann auf der Registerkarte **Alle Segmente** eingesehen werden und kann wie jedes andere dynamische Segment für nachgelagerte Prozesse verwendet werden. Wenn Sie sich die Regeln ansehen möchten, die das Modell nach dem Speichern eines Segments erfahren hat, können Sie dies tun, indem Sie **Bearbeiten** auf der Registerkarte **Alle Segmente** wählen.
