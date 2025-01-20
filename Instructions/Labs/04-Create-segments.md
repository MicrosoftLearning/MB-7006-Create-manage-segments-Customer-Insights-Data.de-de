---
lab:
  title: 'Lab 4: Erstellen von Segmenten'
---

# Lab 4: Erstellen von Segmenten

In diesem Lab lernen Sie Folgendes:
- Erstellen eines Segments aus einem Profil
- Erstellen eines Segments mithilfe von Measures
- Erstellen eines Segments von Grund auf

## Übung 1: Erstellen von Segmenten aus mehreren Quellen 
### Aufgabe 1: Erstellen von Segmenten aus einem Profil
In dieser ersten Aufgabe erstellen wir ein Segment basierend auf dem Kundenprofil. Wir werden alle Kundschaften identifizieren, die im Bundesstaat Texas ansässig sind. 

1. Erweitern Sie **Erkenntnisse** und wählen Sie **Segmente** aus dem linken Navigationsmenü.

1. Wählen Sie **+ Neu > Aus Profilen erstellen**.

1. Für **Feld** wählen Sie **Staat** und für **Wert** wählen Sie **Texas**.

1. Wählen Sie **Review** (Überprüfen) aus.

1. Nennen Sie das Segment **Kundschaft aus Texas** und vergewissern Sie sich, dass der **Ausgabetabellen-Name** automatisch mit **CustomersFromTexas** gefüllt wurde.

1. Wählen Sie **Speichern**.

### Aufgabe 2: Erstellen eines Segments mithilfe von Measures 
Contoso Coffee Marketing möchte eine neue Werbeaktion durchführen. Basierend auf historischen Daten hat das Marketing festgestellt, dass sie brew-at-home-Kundschaft mit einem höheren als durchschnittlichen Onlinekaufwert ansprechen möchten. Dieses Mal erstellen wir das Segment mit der Option **Aus Measures erstellen**. 

1. Wählen Sie **Erkenntnisse > Segmente** aus dem linken Navigationsmenü.

1. Wählen Sie **+ Neu > Aus Measures erstellen**.

1. Wählen Sie das Attribut **Durchschnittlicher Ladenkauf ($)**.

1. Legen Sie den **Operator** auf **Größer als** fest.

1. Legen Sie den **Wert** auf **100** fest. Das Diagramm sollte mit **Durchschnittlicher Webkauf ($)** nach Perzentil aufgefüllt werden.

1. Wählen Sie **Review** (Überprüfen) aus.

1. Nennen Sie das Segment **Premium-Kundschaft** und stellen Sie sicher, dass der **Ausgabetabellen-Name** automatisch mit **PremiereCustomers** ausgefüllt wurde.

1. Wählen Sie **Speichern**.

### Aufgabe 3: Erstellen eines Segments von Grund auf neu
Jede Saison führt Contoso Coffee verschiedene Werbeaktionen aus. Dieses Jahr wollen sie eine Herbst-Schlussverkaufsaktion durchführen, bei der die restlichen Modelle zum Jahresende verkauft werden sollen. Mit ihrem neu auf den Markt gebrachten Cold Brew Coffee wollen sie die Generation X ansprechen, die überdurchschnittlich viel im Laden einkauft. Da für dieses Segment mehrere Kriterien erforderlich sind, erstellen wir es von Grund auf neu.

1. Wählen Sie **Erkenntnisse > Segmente** aus dem linken Navigationsmenü. Wählen Sie **+ Neu > Eigenes erstellen**.

1. Wählen Sie neben dem Kopftext **Unbetiteltes Segment** die Option **Details bearbeiten** und ändern Sie den **Namen** in **Herbst-Schlussverkaufsaktion**.

1. Vergewissern Sie sich, dass der **Name der Ausgabeeinheit** automatisch mit **FallCloseoutPromotion** ausgefüllt wurde und wählen Sie **Erledigt**.

1. Erweitern Sie über den Bereich **Zu Regel 1 hinzufügen** auf der rechten Seite des Bildschirms den Bereich **Kunde : CustomerInsights** und wählen Sie **DateofBitrh**. 

1. Wählen Sie **ist** und, **am oder nach** und geben Sie das Datum als **01.01.1965** ein.

1. Fügen Sie eine weitere Bedingung mit einem **und** Qualifizierer hinzu.

1. Legen Sie diese Bedingung als **Geburtsdatum** ist **am oder vor dem 31.12.1979** fest.

1. Fügen Sie eine weitere Bedingung mit einem **und** Qualifizierer hinzu. 

1. Erweitern Sie **Customer_Measure: CustomerInsights**.

1. Wählen Sie die Kennzahl **Durchschnittlicher Webkauf ($)** aus und fügen Sie sie zu **Regel 1** hinzu. 

1. Wählen Sie **ist** und **größer als oder gleich 125**.

1. Fügen Sie eine weitere Bedingung mit einem **und** Qualifizierer hinzu. 

1. Geben Sie im Feld **Attributname eingeben oder aus Bedienfeld hinzufügen** **Geschlecht** ein und wählen Sie es aus der angezeigten Liste aus. 

1. Wählen Sie **ist** und, **gleich männlich**.

1. Markieren Sie das Kontrollkästchen **Groß-/Kleinschreibung ignorieren**.

1. Wählen Sie unter **Regel 1** die Option **+ Regel hinzufügen**. 

1. Markieren Sie das Feld **Union** und ändern Sie es in **Ausnahme**.

1. Erweitern Sie im Bereich **Zu Regel 2 hinzufügen** **Kunde : CustomerInsights** und wählen Sie **Staat**. 

1. Wählen Sie **ist** und **gleich Florida**.

1. Wählen Sie **Speichern** aus.

1. Klicken Sie auf **Run** (Ausführen).
