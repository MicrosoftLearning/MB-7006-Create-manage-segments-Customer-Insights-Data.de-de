---
lab:
  title: 'Lab 3: Erstellen von Measures'
---

# Lab 3: Erstellen von Measures

In diesem Lab lernen Sie Folgendes:
- Definieren von Geschäfts-Measures zum Nachverfolgen der Geschäftsleistung und -integrität
- Definieren von Kunden-Measures, um Erkenntnisse über einzelne Kundinnen und Kunden zu gewinnen

## Übung 1: Definieren von Measures und Attributen
### Aufgabe 1: Durchschnittswert von In-Store-Eiinkäufen
In dieser ersten Aufgabe erstellen wir ein Measure, um den Durchschnittswert aller In-Store-Einkäufe zu definieren, die bei **Contoso Coffee** getätigt wurden.

1. Erweitern Sie **Insights**, und wählen Sie **Measures** im linken Navigationsmenü aus.

1. Wählen Sie auf der Symbolleiste **+Neu** aus, und wählen Sie dann **Eigene erstellen** aus.

1. Wählen Sie neben dem Kopfzeilentext **Unbenanntes Measure** die Option **Details bearbeiten** aus.

1. Legen Sie den **Namen** auf **Durchschnittlicher Store-Kaufwert ($)** fest, und wählen Sie **Fertig** aus.

1. Schalten Sie **Measure-Typ** von **Kunde** auf **Geschäft** um.

1. Wählen Sie neben **Berechnung 1** die Option **Namen bearbeiten** aus.

1. Legen Sie den **Namen** auf **Durchschnittlicher Store-Kaufwert ($)** fest.

1. Überprüfen Sie, ob der **Name des Ausgabeattributs** auf **AverageStorePurchaseValue** festgelegt ist.

1. Wählen Sie **Fertig** aus.

1. Wählen Sie unter der Berechnung des **durchschnittlichen Store-Kaufwerts ($)** die Option **Mittelwert** aus der Dropdownliste **Funktion auswählen** aus.

1. Wählen Sie **+Attribut hinzufügen** aus, erweitern Sie **Käufe : PoS**, und wählen Sie **TotalPrice** aus.

1. Wählen Sie **Hinzufügen**.

1. Wählen Sie die Schaltfläche **Ausführen** aus, um Ihr Measure abzuschließen.

    In dieser nächsten Aufgabe erstellen wir ein Measure, um den Mittelwert aller Webkäufe zu definieren, die bei **Contoso Coffee** getätigt wurden.

1. Wählen Sie **Insights > Measures** aus dem linken Navigationsmenü aus.

1. Wählen Sie **+Neu > Eigenes erstellen** auf der Symbolleiste aus.

1. Wählen Sie neben dem Kopfzeilentext **Unbenanntes Measure** die Option **Details bearbeiten** aus.

1. Legen Sie den **Namen** auf **Durchschnittlicher Webkaufwert ($)** fest, und wählen Sie **Fertig** aus.

1. Schalten Sie **Measure-Typ** von **Kunde** auf **Geschäft** um.

1. Wählen Sie neben **Berechnung 1** die Option **Namen bearbeiten** aus.

1. Legen Sie den **Namen** auf **Durchschnittlicher Webkaufwert ($)** fest.

1. Überprüfen Sie, ob der **Name des Ausgabeattributs** auf **AverageWebPurchaseValue** festgelegt ist.

1. Wählen Sie **Fertig** aus.

1. Wählen Sie unter der **Berechnung des durchschnittlichen Webkaufwerts ($)** die Option **Mittelwert** aus der Dropdownliste **Funktion auswählen** aus.

1. Wählen Sie **+ Attribut hinzufügen** aus, erweitern Sie **Käufe: eCommerce** und wählen Sie **Gesamtpreis** aus.

1. Wählen Sie **Hinzufügen**.

1. Wählen Sie die Schaltfläche **Ausführen** aus, um Ihr Measure abzuschließen.

### Aufgabe 2: Definieren von Kunden-Measures
Wir benötigen zwei Kunden-Measures, die zum Berechnen eines Kundenattributes verwendet werden können. Wir erstellen ein Measure, um die Gesamtausgaben der Kundinnen und Kunden für **Onlinekäufe** und ein Measure zu ermitteln, um ihre Gesamtausgaben für **In-Store-Einkäufe** zu ermitteln. Nachdem wir diese erstellt haben, können wir ein Kundenattribut erstellen, um diese beiden zusammen hinzuzufügen.

In dieser Aufgabe erstellen wir ein Measure, um die Summe aller In-Store-Einkäufe zu definieren.

1. Wählen Sie **Insights > Measures** aus dem linken Navigationsmenü aus.

1. Wählen Sie **+Neu > Eigenes erstellen** auf der Symbolleiste aus.

1. Wählen Sie neben dem Kopfzeilentext **Unbenanntes Measure** die Option **Details bearbeiten** aus.

1. Legen Sie den **Namen** auf **Summe aller In-Store-Ausgaben** fest, und wählen Sie **Fertig** aus.

1. Wählen Sie unter der Berechnung **Summe aller In-Store-Ausgaben** die Option **Summe** in der Dropdownliste **Funktion auswählen** aus.

1. Wählen Sie **+Attribut hinzufügen** aus, erweitern Sei **Einkäufe : PoS**, wählen Sie **TotalPrice** und dann **Hinzufügen** aus.

1. Um die Measureberechnung einzurichten, wählen Sie **Dimensionen( 1)** aus.

1. Wählen Sie **Dimensionen bearbeiten** aus.

1. Erweitern Sie **Einkäufe : PoS**, wählen Sie **LoyaltyId** und dann **Fertig** aus.

1. Wählen Sie **Übernehmen**.

1. Wählen Sie die Schaltfläche **Ausführen** aus, um Ihr Measure abzuschließen. Wenn ein Fehler auftritt und der **Beziehungspfad**ausgewählt werden muss, wählen Sie **PoS_Purchases > Kunde** und dann die Schaltfläche **Ausführen** aus, um den Vorgang abzuschließen.

    Als Nächstes erstellen wir ein Measure, um die Summe aller online getätigten Einkäufe zu definieren.

1. Wählen Sie **Insights > Measures** aus dem linken Navigationsmenü aus.

1. Wählen Sie **+Neu > Eigenes erstellen** auf der Symbolleiste aus.

1. Wählen Sie neben dem Kopfzeilentext **Unbenanntes Measure** die Option **Details bearbeiten** aus.

1. Legen Sie den **Namen** auf **Summe aller Onlineausgaben** fest, und wählen Sie **Fertig** aus.

1. Wählen Sie unter der Berechnung **Summe aller Online-Ausgaben** die Option **Summe** in der Dropdownliste **Funktion auswählen** aus.

1. Wählen Sie **+ Attribut hinzufügen** aus, erweitern Sie **Einkäufe : eCommerce**, wählen Sie **TotalPrice** und dann **Hinzufügen** aus.

1. Wählen Sie unter **Measure-Berechnungen einrichten** die Option **Dimensionen (1)** aus.

1. Wählen Sie **Dimensionen bearbeiten** aus.

1. Erweitern Sie **Einkäufe : eCommerce**, wählen Sie **ContactId** und dann **Fertig** aus.

1. Wählen Sie **Übernehmen**.

1. Wählen Sie die Schaltfläche **Ausführen** aus, um Ihr Measure abzuschließen.

### Aufgabe 3: Definieren von Kundenattributen 
Zunächst definieren wir **Treuepunkte insgesamt**, die von jedem Kunden erzielt werden.

1. Wählen Sie bei Bedarf **Insights > Measures** aus dem linken Navigationsmenü aus.

1. Wählen Sie **+Neu > Eigenes erstellen** auf der Symbolleiste aus.

1. Wählen Sie neben dem Kopfzeilentext **Unbenanntes Measure** die Option **Details bearbeiten** aus.

1. Legen Sie den **Namen** auf **Clubpunkte insgesamt** fest, und wählen Sie **Fertig** aus.

1. Wählen Sie unter der Berechnung **Clubpunkte insgesamt** die Option **Summe** aus der Dropdownliste **Funktionstyp** aus.

1. Wählen Sie **+ Attribut hinzufügen** aus, erweitern Sie **Einkäufe : PoS**, wählen Sie **RewardsPointsAdded** und dann **Hinzufügen** aus.

1. Wählen Sie die Schaltfläche **Ausführen** aus, um Ihr Measure abzuschließen.

    Als Nächstes definieren wir den Gesamtwert aller Einkäufe, die für jeden Kunden getätigt wurden.

1. Wählen Sie **Insights > Measures** aus dem linken Navigationsmenü aus.

1. Wählen Sie **+Neu > Eigenes erstellen** auf der Symbolleiste aus.

1. Wählen Sie neben dem Kopfzeilentext **Unbenanntes Measure** die Option **Details bearbeiten** aus.

1. Legen Sie den **Namen** auf **Lebensdauerausgaben ($)** fest, und wählen Sie **Fertig** aus.

1. Wählen Sie unter der Berechnung **Lebensdauerausgaben ($)** die Option **Summe** aus der Dropdownliste **Funktionstyp** aus.

1. Klicken Sie auf **+ Attribut hinzufügen**.

1. Wählen Sie die Registerkarte **Measures** aus, erweitern Sie **TotalInStoreSpend: CustomerInsights**, wählen Sie **Berechnung 1** und dann **Hinzufügen** aus.

1. Wählen Sie das **+ (Pluszeichen)** aus, um nach dem soeben hinzugefügten Attribut ein Pluszeichen hinzuzufügen. Das Pluszeichen sollte in der Berechnungsformel angezeigt werden.

1. Klicken Sie auf **+ Attribut hinzufügen**.

1. Wählen Sie die Registerkarte **Measures** aus, erweitern Sie **TotalOnlineSpend: CustomerInsights**, wählen Sie **Berechnung 1** und dann **Hinzufügen** aus.

1. Wählen Sie die Schaltfläche **Ausführen** aus, um Ihr Measure abzuschließen.

    Als Nächstes definieren wir den Durchschnittswert aller Store-Käufe für jeden Kunden.

1. Wählen Sie **Insights > Measures** aus dem linken Navigationsmenü aus.

1. Wählen Sie **+Neu > Eigenes erstellen** auf der Symbolleiste aus.

1. Wählen Sie neben dem Kopfzeilentext **Unbenanntes Measure** die Option **Details bearbeiten** aus.

1. Legen Sie den Namen auf **Durchschnittlicher Store-Kauf ($)** fest, und wählen Sie **Fertig** aus.

1. Wählen Sie unter der Berechnung **Durchschnittlicher Store-Kauf ($)** die Option **Mittelwert** aus der Dropdownliste **Funktion auswählen** aus.

1. Wählen Sie **+Attribut hinzufügen** , erweitern Sie **Einkäufe : PoS**, wählen Sie **Gesamtpreis**und dann **Hinzufügen** aus.

1. Wählen Sie die Schaltfläche **Ausführen** aus, um den Measure abzuschließen.

### Aufgabe 4: Durchschnittswert von Webkäufen
Als Nächstes definieren wir den Durchschnittswert aller Webkäufe für jeden Kunden.

1. Wählen Sie bei Bedarf **Measures** aus dem linken Navigationsmenü aus.

1. Wählen Sie **+Neu > Eigenes erstellen** auf der Symbolleiste aus.

1. Wählen Sie neben dem Kopfzeilentext **Unbenanntes Measure** die Option **Details bearbeiten** aus.

1. Legen Sie den Namen auf **Durchschnittlicher Webkauf ($)** fest, und wählen Sie **Fertig** aus.

1. Wählen Sie unter der Berechnung **Durchschnittlichen Webkauf ($)** die Option **Mittelwert** aus der Dropdownliste **Funktion auswählen** aus.

1. Wählen Sie **+ Attribut hinzufügen** aus, erweitern Sie **Einkäufe : eCommerce**, wählen Sie **Total Price** und dann **Hinzufügen** aus.

1. Wählen Sie die Schaltfläche **Ausführen** aus, um Ihr Measure abzuschließen.
