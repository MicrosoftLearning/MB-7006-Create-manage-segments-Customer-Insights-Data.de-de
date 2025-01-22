---
lab:
  title: "Lab 2:\_Erstellen einheitlicher Kundenprofile"
---

# Lab 2: Erstellen einheitlicher Kundenprofile
In diesem Lab lernen Sie Folgendes:
- Zusammenführen von Daten aus Ihren rohen Datenquellen in ein Kundenprofil
- Auswählen eines Primärschlüssels 
- Erstellen von Übereinstimmungsregeln
- Definieren von Such- und Filterindizes und -aktivitäten

Ihr Ziel ist es, herauszufinden, wie viele eindeutige Profile von Kundinnen und Kunden **Contoso Retail** in verschiedenen Datenquellen hat.

## Übung 1: Vereinheitlichen Ihrer Daten
### Aufgabe 1: Zuordnen von Kontakten zu allgemeinen Datentypen
1. Melden Sie sich bei **Customer Insights - Data** an.

1. Erweitern Sie im linken Navigationsmenü **Daten** und wählen Sie **Vereinheitlichen** aus. Wählen Sie **Erste Schritte** aus.

1. Wählen Sie **Tabellen und Spalten auswählen** aus.

1. Wählen Sie die Tabellen, die das Kundenprofil darstellen – **Kontakte (eCommerce)** und **Kunden (Loyalty)**. Wählen Sie **Übernehmen**.

1. Ihnen werden nun die Zuordnungen Ihrer Quelltabelle zu den Standardmodelltypen angezeigt. Sehen Sie sich die Typen in der Tabelle an.

1. Sie müssen für jede aufgenommene Entität einen **„Primärschlüssel“** auswählen. Der Primärschlüssel muss eine eindeutige Referenz sein. Wählen Sie für **eCommerce-Kontakte** **ContactId** als Primärschlüssel aus.

1. Die Daten **eCommerce-Kontakte** enthalten eine Spalte mit dem Namen **E-Mail-Abonnent**, die aufgrund des Namens dem falschen Typ **Identity.Service.Email** zugeordnet wird. Öffnen Sie die Dropdownliste für diese Spalte, und wählen Sie die leere Option („nichts/leer“) aus. Wenn wir dies nicht tun, wird dieses Feld standardmäßig mit dem Feld **E-Mail** zusammengeführt, was wir nicht möchten.

1. Wählen Sie die Option **Loyalty Customers** unter **Tabellen** aus und legen Sie **LoyaltyId** als Primärschlüssel fest.

1. Wählen Sie oben links **Quellspalten speichern** aus.

1. Wählen Sie **Weiter** und dann erneut **Weiter** aus, um die doppelte Überprüfung zu überspringen und mit dem Schritt **Übereinstimmungsregeln** fortzufahren.

### Aufgabe 2: Angeben der Übereinstimmungsreihenfolge
Für den nächsten Schritt müssen wir die Reihenfolge festlegen, in der die Profile zusammengeführt werden sollen. Sie können Attribute zusammenführen, um sicherzustellen, dass die vereinheitlichten Profile vollständig sind, und festlegen, welche Quellen für diese Attribute vorrangig verwendet werden sollen.

1. Sie sollten die vollständigste oder genaueste Profilquelle als **Primäre (erste) Quelle** auswählen. Überprüfen Sie, ob **Contacts: eCommerce** die primäre (erste) Quelle ist.

1. Überprüfen Sie, ob **Customers: Loyalty** die zweite Quelle in der Liste ist. 

1. Überprüfen Sie, ob **Alle Datensätze einschließen** für beide Datenquellen aktiviert ist.

### Aufgabe 3 – Erstellen einer Abgleichregel
1. Es gibt einen Warnindikator für die Zeile **Customers: Loyalty**. Wählen Sie **+ Regel hinzufügen** aus.

1. Fügen Sie die erste Bedingung mit **FullName** hinzu:
    - Wählen Sie in der Tabelle **Contacts: eCommerce** das Feld **FullName** aus.
    - Wählen Sie in der Tabelle **Customers: Loyalty** das Feld **FullName** aus.
    - Lassen Sie das Dropdown-Menü **Normalisieren** leer.
    - Setzen Sie die **Präzisionsstufe** auf **Basic**.
    - Stellen Sie den **Präzisionswert** mit dem Schieberegler auf **Genau** ein.
    - Geben Sie den Namen **FullName, E-Mail** für den **Regelnamen** ein.

1. Fügen Sie eine zweite Bedingung für die E-Mail-Adresse hinzu, indem Sie **+ Hinzufügen** und dann **Bedingung hinzufügen** wählen.
    - Wählen Sie in der Tabelle **Contacts: eCommerce** das Feld **E-Mail** aus.
    - In der Tabelle **Customers : Loyalty** wählen Sie das Feld **E-Mail** aus.
    - Lassen Sie das Dropdown-Menü **Normalisieren** leer.
    - Setzen Sie die **Präzisionsstufe** auf **Basic**.
    - Setzen Sie den **Präzisionswert** auf **Genau**.

1. Wählen Sie **Fertig** aus.

1. Wählen Sie **Weiter** aus.

1. Auf dem Bildschirm **Einheitliche Datenansicht** werden keine Änderungen vorgenommen. Wählen Sie **Weiter** aus, um zum Bildschirm „Überprüfen“ zu wechseln.

1. Wählen Sie auf dem Bildschirm **Überprüfung** die Option **Kundenprofile erstellen** aus. Customer Insights gleicht jetzt Kundendaten aus all Ihren Kundeninformationsquellen ab, um zu ermitteln, wie viele eindeutige Kundenprofile Sie auf der Grundlage Ihrer Regeln haben würden. Es kann einige Zeit dauern, um die Profile zu erstellen.

Herzlichen Glückwunsch! Sie haben erfolgreich Daten aus verschiedenen Quellen in **Customer Insights** vereinheitlicht, um ein **Vereinheitlichtes Kundenprofil** zu erstellen, mit dem Sie Einblicke in Ihren gesamten Kundenstamm gewinnen können.

## Übung 2: Konfigurieren von Such- und Filterindizes und -aktivitäten
In dieser Übung richten wir **Such- und Filterkriterien** ein, damit Customer Insights-Benutzende nach einheitlichen Kundenprofilen suchen können. Danach konfigurieren wir Aktivitäten.

### Aufgabe 1: Konfigurieren der Suchspalten und des Filterindexes 
1. In **Customer Insights** wählen Sie **Kunden** aus dem linken Navigationsmenü aus.

1. Wählen Sie **Such- und Filterindex** aus. Einige Felder sind bereits standardmäßig hinzugefügt. Klicken Sie auf der Symbolleiste auf **+Hinzufügen**.

1. Wählen Sie **CustomerId, FirstName, LastName, FullName, DateOfBirth, EMail, PostCode, ContactId (eCommerce_Contacts), und LoyaltyId** aus (falls diese noch nicht ausgewählt sind). Deaktivieren Sie alle anderen aktivierten Felder. Wählen Sie **Übernehmen**.

1. Wählen Sie **Speichern** aus.

1. Klicken Sie auf **Run** (Ausführen).

1. In **Customer Insights** wählen Sie **Kunden** aus dem linken Navigationsmenü aus. Sie sollten einen Satz von Kundenkarten angezeigt bekommen, die die **einheitlichen Profile** darstellen. Sie können Karten erweitern, um mehr über die Kundschaft zu erfahren oder die Karten nach verschiedenen Feldern zu sortieren. Versuchen Sie dies, indem Sie **Karten erweitern** und **Sortieren nach** in der Symbolleiste wählen.

1. Sie können **Kunden suchen** verwenden, um nach Textattributen zu einheitlichen Kundenprofilen zu suchen. (Beispiele: Die Suche nach „1“ wird in allen Textattributen durchgeführt und gibt Übereinstimmungen und Teilübereinstimmungen zurück.)

### Aufgabe 2: Erstellen von Aktivitäten
1. Erweitern Sie in **Customer Insights** die Option **Daten > Aktivitäten** im linken Navigationsmenü, und wählen Sie **+ Aktivitäten konfigurieren** aus.

1. Klicken Sie auf **Tabellen auswählen**.

1. Wählen Sie die Tabellen **Einkäufe : eCommerce** und **Einkäufe : PoS** aus und wählen Sie **Hinzufügen** aus.

1. Für **Einkäufe : eCommerce** konfigurieren Sie wie folgt:
    - Legen Sie den **Aktivitätstyp** auf **SalesOrder** fest.
    - Legen Sie den **Primärschlüssel** auf **PurchaseId** fest.

1. Für **Einkäufe: PoS** konfigurieren Sie wie folgt:
    - Legen Sie den **Aktivitätstyp** auf **SalesOrder** fest.
    - Legen Sie den **Primärschlüssel** auf **PurchaseId** fest.

1. Wählen Sie **Weiter** aus.
   
1. Konfigurieren Sie **eCommerce : Einkäufe** wie folgt:
    - Geben Sie **OnlinePurchase** für den **Namen der Aktivität** ein.
    - Füllen Sie die folgenden Felder aus (nicht erwähnte Felder können leer bleiben):
        - **Zeitstempel**: PurchasedOn
        - **Ereignisaktivität**: ActivityTypeDisplay
        - **Weitere Details**: Betreff
        - **Diese Aktivität in der Zeitleiste Ihres Kundenprofils anzeigen?** Ja
        - **Symbol**:Wählen Sie den Warenkorb aus.
        - **Die Feldtypen für die Attribute Ihrer Aktivität festlegen?** Ja, und konfigurieren Sie wie folgt:
            - **Verkaufsauftrags-ID**: PurchaseID
            - **Bestelldatum**: PurchasedOn
            - **Umsatzbetrag**: TotalPrice

1. Konfigurieren Sie **POS : Einkäufe** wie folgt:
    - Geben Sie **PoSPurchase** für den **Namen der Aktivität** ein.
    - Füllen Sie die folgenden Felder aus (nicht erwähnte Felder können leer bleiben):
        - **Zeitstempel**: PurchasedOn
        - **Ereignisaktivität**: ActivityTypeDisplay
        - **Weitere Details**: Betreff
        - **Diese Aktivität in der Zeitleiste Ihres Kundenprofils anzeigen?** Ja
        - **Symbol**:Wählen Sie den Warenkorb aus.
        - **Die Feldtypen für die Attribute Ihrer Aktivität festlegen?** Ja, und konfigurieren Sie wie folgt:
            - **Verkaufsauftrags-ID**: PurchaseID
            - **Bestelldatum**: PurchasedOn
            - **Umsatzbetrag**: TotalPrice

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf dem Bildschirm **Aktivitätsbeziehungen konfigurieren** bei ausgewählter Option **E-Commerce : Einkäufe** die Option **+ Beziehung hinzufügen** aus.

1. Legen Sie im Bereich **Beziehungspfad hinzufügen** die folgenden Werte fest:
    - **Fremdschlüssel**: ContactId
    - **Tabellenname**: Kontakte : eCommerce
    - **Beziehungsname**: eCommPurchasesToContacts
    - Wählen Sie **Übernehmen**.

1. Wählen Sie **POS : Einkäufe** aus. Wählen Sie **+ Beziehung hinzufügen** aus.

1. Legen Sie im Bereich **Beziehungspfad hinzufügen** die folgenden Werte fest:
    - **Fremdschlüssel**: LoyaltyId
    - **Tabellenname**: Kunden : Loyalty
    - **Beziehungsname**: PoSPurchasesToLoyalty
    - Wählen Sie **Übernehmen**.

1. Wählen Sie **Weiter** aus.

1. Wählen Sie **Aktivitäten erstellen** aus.

1. Warten Sie, bis die **Aktivitäten** aktualisiert und vereinheitlicht wurden.



