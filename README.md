# Bachelorarbeit

## Einleitung

Im Rahmen der Bachelorarbeit „Graphentheoretische Untersuchung von deut-schen Städten mithilfe von OpenStreetMap“ sollten die Straßennetzwerke von verschiedenen analysiert werden. Ziel ist es, ein besseres Verständnis der Struktur, Effizienz und Resilienz urbaner Verkehrsnetze zu gewinnen. Als Da-tengrundlage dient der Straßennetzdatensatz von Unterfranken, aus dem aus-gewählte Städte und Dörfer untersucht und miteinander verglichen wurden. Hierbei wurden die einzelnen Datensätze für die Auswertung vorbereitet und gefiltert. Die Netzwerkeigenschaften wurden anhand verschiedener Metriken, darunter der Netzwerkdichte, der Deaktivierung der Zentralen Knoten, der Stra-ßendiversität und -längenverteilung ermittelt. Zudem wurden Städte mit einer geplanten, rasterförmigen Straßenstruktur mit solchen verglichen, die orga-nisch gewachsen sind, um Unterschiede in der Topologie und den Eigenschaf-ten herauszuarbeiten.

## Vorbereitung

Es wurde als Python-Umgebug Anaconda verwendet

1. Anaconda herunterladen

2. Python-Umgebung erstellen mit `conda create --name <Umgebungsname>`

3. Bibliotheken in der Umgebung installieren

- Osmium: `conda install conda-forge::osmium-tool`
- Pandas: `conda install anaconda::pandas`
- NetworkX: `conda install conda-forge::networkx`
- Matplotlib: `conda install conda-forge::matplotlib`
- Seaborn: `conda install conda-forge::seaborn`
- Numpy: `conda install conda-forge::numpy`
- Requests: `conda install conda-forge::requests`

## Auswahl des Datensatz

Unter `Datasets` werden die Datensätze, die Geografische Daten von mehreren Orten beinhalten, von OpenStreetMap gespeichert.
Unter `City_data` werden die einzelnen Datensätze der angegebenen Orte aus dem Datensatz in `Datasets` gespeichert.

Wurde der installierte Datensatz im Ordner `Datasets` eingefügt, soll der Dateiname in der ersten Zelle "Imports und Datei" von `Dataset_Visualization.ipynb` unter `dataset_path` eingefügt werden. Unter `cities`, in der selben Zelle, werden die Orte angegeben, die analysiert werden sollen. Wird das Skript bis zum Punkt "Datensatz nach Städten filtern" werden die einzelnen Datensätze der angegebenen Orten unter `City_data` in den entsprechenden Sub-Ordnern `village`, `town` oder `city` gespeichert, je nachdem um welche Art von Ort es sich dabei handelt.

Beispiel:

```
dataset_path = os.path.join("Datasets", "unterfranken-latest.osm")
cities = ["Ringheim", "Mömlingen", "Glattbach", "Großostheim", "Marktheidenfeld", "Aschaffenburg", "Würzburg"]  
```
