## Netzwerkarchitektur:
Die Netzwerkarchitektur basiert auf einem tiefen neuronalen Netzwerk, das mithilfe der Keras-Bibliothek implementiert wurde.

Die Architektur beginnt mit einer Eingabeschicht. Diese umfasst aufgrund der im Datensatz verwendeten 11 chemischen Eigenschaften von Wein bzw. Features eine Anzahl von 11 Neuronen. 
Aus der Eingabeschicht werden die Daten an die folgenden Schichten weitergeleitet, wo die eigentliche Verarbeitung stattfindet.

Es folgen die verdeckten Schichten, welche jeweils eine bestimmte Anzahl von Neuronen beinhalten. Jedes Neuron berechnet eine gewichtete Summe seiner Eingaben und wendet dann eine Aktivierungsfunktion auf das Ergebnis an. Es wird hier auf die ReLU-Aktivierungsfunktion zurückgegriffen, da die Regression mit einer nichtlinearen Aktivierungsfunktion durchgeführt werden sollte. ReLU zeichnet sich durch die Effizienz und die gute Gradientenverbreitung aus. 
Die Anzahl der verdeckten Schichten und die Anzahl der Neuronen in jeder Schicht sind Hyperparameter, welche mittels einer Hyperparameter-Optimierung bestimmt werden sollten.

Abschließend folgt eine Ausgabeschicht, welche eine einzige Ausgabe liefert. Diese Ausgabe repräsentiert die Vorhersage des Modells für den Weinscore basierend auf den Eingabedaten. 

## Loss-Fkt und Optimizer:
Auf Basis der Aufgabenstellung wurden die Mean Squared Error (MSE) Loss-Funktion und der Adam-Optimizer ausgewählt.

Die MSE Loss-Funktion ist eine häufig verwendete Loss-Funktion, da sie die Genauigkeit der Vorhersagen quantifiziert und das Modell dadurch anregt, möglichst nahe an den tatsächlichen Werten zu liegen. 

Der Adam-Optimierer ist einer der beliebtesten Optimierer und bietet eine adaptive Lernrate. Er überzeugt durch seine Effizienz und minimale Speicheranforderungen und ist auch für Probleme mit großen Datensets gut geeignet. Durch die adaptive Skalierung seiner Lernraten eignet sich Adam gut für Modelle mit verrauschten Daten.

Einer der wichtigsten Hyperparameter für die Nutzung des Adam-Optimizers ist die Learning-Rate, welche mittels Hyperparameter-Optimierung bestimmt wird.

## Fragen:
Aktuell Loss-Fuktion MSE
Loss Funktion auch gleichzeitig der Bewertungsparameter nachdem das beste Modell in der Kreuzvalidierung ausgewählt wird?
Aktuell R2 Score um bestes Modell rauszufinden.

Welcher Parameter der wichtigste (R2 Score, RMSE, MSE, MAPE)?

Wie explizit soll Aufteilung angegeben werden?