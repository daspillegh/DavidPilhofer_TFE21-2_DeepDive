# DeepDive Artificial Neuronal Network

Dieses Repository dokumentiert die Erstellung eines Neuronalen Netzwerkes mit Tensorflow und Keras.

Hier ist der Link zum Binder des Projektes  [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/daspillegh/DavidPilhofer_TFE21-2_DeepDive.git/HEAD)

> [!IMPORTANT]
> In dem Binder ist der letzte Trainingsstand dargestellt. Ohne GPU oder TPU dauert der Trainingsprozess sehr lange.

## Diskussion und Ergebnis

Zusammenfassend lässt sich festhalten, dass die Verarbeitung der Bilder trotz der begrenzten Anzahl von Label erfolgreich durch die Verwendung eines Convolutional Neural Networks erreicht wurde. Es wurde bewusst ein minimalistisches CNN gewählt, um die Anzahl der Netzparameter gering zu halten. Diese Entscheidung hatte jedoch einen negativen Einfluss auf die Genauigkeit des Netzes.

Die Reduzierung der Anzahl der Label erforderte das Augmentieren der Daten, um eine größere Variation in den reduzierten Trainingsdaten zu erhalten und damit die Genauigkeit des Netzes zu verbessern. Während des Trainingsprozesses trat Overfitting auf, welches erfolgreich durch die Integration eines Dropout-Layers reduziert wurde. Zusätzlich verbesserte der Einsatz von Methoden wie Early Stopping, Checkpoints und der dynamischen Reduzierung der Lernrate während des Trainings den gesamten Trainingsverlauf.

Nach Abschluss des Trainings wurde das Netz jeweils anhand einer Confusion-Matrix überprüft. Die erhaltenen Ergebnisse dienten als Grundlage für Anpassungen am Training selbst und den Parametern der Datenaugmentierung. Durch die Variation verschiedener Hyperparameter und zusätzliche Trainingsdurchläufe erreichte das Netz eine Genauigkeit von 98,69 % bei einer Parameteranzahl von 347.146. Das Netz wurde dabei über 2 Trainingsdruchläufe mit 30 Epochen mit einer Batch-Size von 64 trainiert.

Die anfänglich definierten Ziele konnnten größtenteils ebefalls erreicht werden. Die erforderliche Genauigkeit von mindestens 98 %, welche zu Beginn definiert wurde, erreicht das optimierte Neuronale Netz. Die Reduzierung der Label wurde durch die zufällige Auswahl von 500 Label pro Klasse und anschließende Augmentierung auf 30.000 Label ebenfalls erreicht. Die Reduzierung der Netzparameter wurde im direkten Vergleich zum Ausgnangsnetz nicht erreicht. Allerdings wurde das gewählte CNN so angepasst um die Netzparameter zwar zu reduzieren, aber gleichzeitig die Genauigkeit des Netzes so hoch wie möglich zu halten. 
