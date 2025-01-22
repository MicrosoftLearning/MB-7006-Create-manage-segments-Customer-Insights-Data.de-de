---
lab:
  title: 'Übung 1: Aufnehmen von Datasets'
---

# Übung 1: Aufnehmen von Datasets
In diesem Lab lernen Sie Folgendes:
- Einbinden mehrerer Datasets mithilfe von PowerQuery
- Transformieren von Datasets und Ändern von Spaltentypen
- Überwachen des Importstatus

Um Segmente zu erstellen, müssen wir zuerst die Daten importieren, die wir in unseren Segmenten verwenden. In dieser Übung werden wir einige Datasets als Voraussetzung importieren, um die Daten zu vereinheitlichen und unsere Segmente zu erstellen.

## Übung 1: Aufnehmen von Datenquellen
Für dieses geführte Projekt müssen Sie verschiedene Datenquellen importieren. Diese Datenquellen werden zum Erstellen Ihrer einheitlichen Kundenprofile verwendet.

### Aufgabe 1: Datenerfassung von Kundendaten aus der eCommerce-Plattform
1. Erweitern Sie in **Customer Insights - Data** **Daten** im linken Navigationsmenü und wählen Sie **Datenquellen**.

1. Wählen Sie **+ Datenquelle hinzufügen** aus. Sehen Sie sich die verfügbaren Methoden zur Datenerfassung an. Wählen Sie für dieses Lab **Microsoft Power Query** und benennen Sie die Quelle **eCommerce**. Wählen Sie dann **Weiter**.

1. Sie erhalten eine Ansicht der **Power Query-Datenquellen**, die **Customer Insights** aufnehmen kann. Achten Sie auf die verfügbaren Konnektoren. Wählen Sie den **Text/CSV**-Konnektor aus.

1. Geben Sie `https://aka.ms/CI-ILT/Contacts` für **Dateipfad oder URL** ein und wählen Sie **Weiter**. Es kann einen Moment dauern, bis die Daten hochgeladen wurden.

1. Sie sollten nun die Daten aus der Quelle durch Tabulatorzeichen getrennt sehen. Wählen Sie **Daten transformieren**, um die Datentypen und -formate für die von Ihnen erfassten Daten zu konfigurieren.

1. Sie werden feststellen, dass die Spaltenüberschrift in der ersten Zeile der Daten angezeigt wird. Um dies zu korrigieren, wählen Sie entweder **Transformieren > Erste Zeile als Kopfzeile verwenden** auf der Registerkarte **Startseite** oder wählen Sie die Registerkarte **Transformieren** und dann **Erste Zeile als Kopfzeile verwenden**.

1. Da wir Daten aus einer **Text-/CSV-Quelle** erfasst haben, sind alle Spalten standardmäßig auf den **Datentyp** „Text“ eingestellt. Um die Daten erfolgreich zu erfassen und zu modellieren, können wir den Datentyp für Nicht-Text-Spalten festlegen.

1. Um den Datentyp zu ändern, wählen Sie das **ABC**-Symbol in der jeweiligen Spaltenüberschrift aus. Aktualisieren Sie den Datentyp für die folgenden Spalten:
    - **DateOfBirth**: Datum
    - **CreatedOn:** Datum
    - **Einkommen:** Währung

1. Stellen Sie sicher, dass das Feld **Name** im Bereich **Abfrageeinstellungen** auf **Kontakte** festgelegt ist. Wählen Sie **Weiter** aus.

1. Wählen Sie **Manuell aktualisieren** und wählen Sie dann **Speichern**.

Herzlichen Glückwunsch. Sie haben nun erfolgreich Ihre erste Datenquelle mit einem Dataset erstellt! Wir werden den Import des nächsten Datasets in der nächsten Aufgabe fortsetzen.

### Aufgabe 2: Einlesen von Kundendaten aus dem Treueprogramm
1. Erweitern Sie in **Customer Insights** im linken Menü **Daten** und wählen Sie **Datenquellen**.

1. Wählen Sie **+ Datenquelle hinzufügen** aus und wählen Sie **Microsoft Power Query** als Importmethode aus. Nennen Sie die Quelle **Treue** und wählen Sie dann **Weiter.**.

1. Wählen Sie den **Text/CSV**-Konnektor aus.

1. Geben Sie `https://aka.ms/CI-ILT/LoyaltySchemeCustomers` für **Dateipfad oder URL** ein, wählen Sie **Weiter** und wählen Sie dann **Daten umwandeln**.

1. Wählen Sie wie zuvor **Transformieren,** dann **Die erste Zeile als Überschrift verwenden**.

1. Aktualisieren Sie den Datentyp für die folgenden Spalten:
    - **DateOfBirth**: Datum
    - **RewardsPoints**: Ganze Zahl
    - **CreatedOn:** Datum

1. Benennen Sie diese Abfrage in **Kundschaft** im Bereich **Abfrageeinstellungen** um und wählen Sie **Weiter**.

1. Wählen Sie **Manuell aktualisieren** und wählen Sie dann **Speichern**.

### Aufgabe 3: Erfassen von Kundendaten aus den Point-of-Sale-Käufen
1. Erweitern Sie in **Customer Insights** **Daten** im linken Navigationsmenü und wählen Sie **Datenquellen** aus.

1. Wählen Sie **+ Datenquelle hinzufügen**, wählen Sie **Microsoft Power Query** und benennen Sie die Quelle **PoS**, dann wählen Sie anschließend **Weiter**.

1. Wählen Sie den **Text/CSV**-Konnektor aus.

1. Geben Sie `https://aka.ms/CI-ILT/POSPurchases` für **Dateipfad oder URL** ein. Wählen Sie **Weiter** und dann **Daten transformieren**.

1. Wählen Sie wie zuvor **Transformieren,** dann **Die erste Zeile als Überschrift verwenden**.

1. Aktualisieren Sie den Datentyp für die folgenden Spalten:
    - **PurchasedOn**: Datum
    - **TotalPrice**: Währung
    - **RewardsPointsAdded:** Ganze Zahl

1. Benennen Sie im Feld **Name** im Bereich **Abfrageeinstellungen** die Abfrage in **Einkäufe** um.

1. Wählen Sie **Weiter** aus.

1. Wählen Sie **Manuell aktualisieren** und wählen Sie **Speichern**.

### Aufgabe 4: Erfassen von Daten zu Online-Einkäufen
1. In dieser Aufgabe erfassen wir **Online-Käufe**, die über die **Contoso Coffee**-Website getätigt wurden.

1. Erweitern Sie in **Customer Insights** im linken Menü **Daten** und wählen Sie **Datenquellen**. (Stellen Sie sicher, dass der Status der **eCommerce**-Datenquelle **Erfolgreich** lautet.)

1. Wählen Sie den Datensatz **eCommerce**, den Sie in der ersten Aufgabe festgelegt haben, und wählen Sie **Bearbeiten**. (Wenn Ihre Daten noch aktualisiert werden, müssen Sie warten, bis die Aktualisierung abgeschlossen ist, bevor Sie sie bearbeiten können).

1. Wählen Sie **Weiter** aus. 

1. Sie sollten die **Power Query**-Ansicht der Daten **eCommerce-Kontakten** sehen, die Sie in Aufgabe 1 übernommen haben. Wählen Sie auf der Registerkarte **Startseite** die Option **Daten abrufen** aus.

1. Sie erhalten eine Ansicht der Connectors der Datenquellen, die **Customer Insights** erfassen kann. Wählen Sie **Text/CSV** aus.

1. Geben Sie `https://aka.ms/CI-ILT/OnlinePurchases` für **Dateipfad oder URL** ein und wählen Sie **Weiter**. Klicken Sie auf **Erstellen**.

1. Wie zuvor wählen Sie **Transformieren**, dann **Erste Zeile als Überschrift verwenden**.

1. Aktualisieren Sie die Datentypen für die folgenden Spalten:
    - **PurchasedOn**: Datum
    - **TotalPrice**: Währung

1. Nennen Sie diese Abfrage **Einkäufe** und wählen Sie **Speichern.**

**Wichtig:** Sie müssen warten, bis der Status aller Ihrer Datenquellen **Erfolgreich** ist, bevor Sie mit der nächsten Übung fortfahren können.
