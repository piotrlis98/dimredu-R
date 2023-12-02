# Analiza porównawcza metod selekcji cech i klasyfikatorów na różnych zbiorach danych

Ten kod ma na celu zbadanie wpływu różnych metod selekcji cech i klasyfikatorów na jakość klasyfikacji na pięciu zbiorach danych: breast-cancer, nba, pistachio, sonar i weather. Zbiory danych pochodzą z repozytorium UCI Machine Learning Repository oraz z Kaggle.

## Kroki

1. Importuje wymagane pakiety z opcjonalną instalacją.
2. Tworzy listę nazw folderów, w których znajdują się pliki z danymi i wynikami klasyfikacji.
3. Mapuje nazwy plików z wynikami klasyfikacji na skrócone nazwy klasyfikatorów.
4. Inicjalizuje ramki danych do przechowywania danych i wyników analizy.
5. Pętli po każdym folderze i wykonuje następujące czynności:
   - Wczytuje pliki z wynikami klasyfikacji dla każdego klasyfikatora i metody selekcji cech. Wyniki są wyrażone w formie współczynnika korelacji Matthewsa (MCC).
   - Przygotowuje dane do analizy Scott-Knott ESD, która dzieli metody selekcji cech na grupy o różnym poziomie istotności statystycznej.
   - Generuje wykresy pudełkowe dla każdego klasyfikatora i metody selekcji cech, z zaznaczeniem grup Scott-Knott ESD.
   - Zapisuje wykresy do pliku PDF dla każdego folderu.
   - Przeprowadza analizę Kendall W dla każdego klasyfikatora, aby sprawdzić, czy istnieje zgodność w rankingu metod selekcji cech.
   - Zapisuje wyniki analizy Kendall W do pliku CSV w formie tabeli.
6. Łączy dane z wszystkich folderów i tworzy ogólny wykres pudełkowy dla wszystkich metod selekcji cech, z zaznaczeniem średniej rangi dla każdej metody.
7. Zapisuje wykres do pliku SVG.
8. Tworzy tabele dla każdego klasyfikatora i zbioru danych, pokazujące średnią rangę dla każdej metody selekcji cech.
9. Sortuje tabele względem średniej rangi i dodaje mediany dla każdej metody, zbioru danych i klasyfikatora.

## Źródła danych

- UCI Machine Learning Repository
- Kaggle
