# Riešenie problému klasifikácie cifier pomocou hlbokých neurónových sietí
## Formulácia problému:
Úlohou projektu je pripraviť modely na klasifikáciu cifier. Jeden z modelov pracuje na EEG dát z datasetu MindBigData, The Visual "MNIST" of Brain Digits (2021). Druhý z modelov pracuje na obrázkoch z toho istého datasetu. Klasifikácia cifier z datasetu obrázkov je dlhšie známy problém, ktorý pracuje s veľmi dobrou presnosťou. Avšak klasifikácia cifier nad EEG dátami je ťažší problém. Po skúmaní podobných prác sa nepodarilo nájsť model, ktorý pracuje s dostatočnou presnosťou. Súčasťou projektu je overenie získaných informácií.
## Príprava dát:
V tomto projekte sa pracuje s datasetom MindBigData, The Visual "MNIST" of Brain Digits (2021) dostupnom na odkaze: https://vivancos.net/pendbMindBigDataVisualMnist2021-Muse2v0.17.zip .
Dataset obsahuje csv súbor, v ktorom je 30000 riadkov. Každý riadok sa skladá z týchto hodnôt:
 -  Dataset : ohodnotenie riadku na TRAIN a TEST, string hodnota
 -  Origin: integer hodnota ukazujúca na pôvodnú lokalitu v datasete Yann LeCun MNIST
 -  Digit_event: integer hodnota číslice od 0-9, pre iadok kde nenastáva udalosť číslice je hodnota -1
 - Original_png: 784 integer hodnôt reprezentujúce pôvodný obrázok o rozmere 28 na 28 pixelov
 -  Timestamp: unixový timestamp hovoriaci o počiatku aktuálnej udalosti
 - EEGdata: obsahuje 4 * 512 floating hodnôt, kde:
   -  512 prvých hodnôt reprezentujú dáta pre TP9 senzor vo frekvencii 256 hz
   - 512 druhých hodnôt reprezentujú dáta pre AF7 senzor vo frekvencii 256 hz
   -  512 tretích hodnôt reprezentujú dáta pre AF8 senzor vo frekvencii 256 hz
   -  512 štvrtých hodnôt reprezentujú dáta pre TP10 senzor vo frekvencii 256 hz

V tomto projekte s ďalšími hodnotami v riadkoch nepracujeme.