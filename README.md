## Data-Mining---Predykcja-choroby-serca
# Opis projektu

Projekt dotyczy analizy danych medycznych oraz budowy modeli uczenia maszynowego w celu przewidywania występowania chorób serca. Wykorzystano ogólnodostępny zbiór danych Heart Disease Dataset.

# Cel projektu

przeprowadzenie wstępnej eksploracji danych,

identyfikacja najważniejszych cech wpływających na występowanie choroby,

porównanie skuteczności różnych modeli klasyfikacyjnych.

# Dane

Zbiór danych zawiera 1025 obserwacji oraz 13 cech opisujących m.in.:

age - wiek

sex - płeć

cp - typ bólu w klatce piersiowej (od 0 do 3)

trestbps - Spoczynkowe ciśnienie krwi mmHg

chol - cholesterol w surowicy mg/dl

fbs - poziom glukozy na czczo większy niż 120 mg/dl (1 - tak, 0 - nie)

restecg - wynik kardiograficzny w spoczynku (od 0 do 2)

thalach - Maksymalne osiągalne tętno

exang - dławica wywołana wysiłkiem (1 - tak, 0 - nie)

oldpeak - depresja w odcinku ST wywołana wysiłkiem w porównaniu do spoczynku

slope - nachylenie szczytowego odcinka ST podczas ćwiczeń

ca - Liczba głównych naczyń krwionośnych pokolorowanych przy użyciu fluoroskopii (od 0 do 3)

thal - zaburzenia syntezy hemoglobiny (1 - norma, 2 - stała wada, 3 - wada odwracalna).


Zmienna docelowa:

0 – brak choroby

1 – choroba serca


# Eksploracja danych

W ramach analizy:

sprawdzono kompletność danych,

przeanalizowano statystyki opisowe,

wykonano wizualizacje (boxploty),

obliczono macierze korelacji (Pearsona i Spearmana).


# Selekcja cech

W celu identyfikacji najważniejszych zmiennych wykorzystano:

- współczynnik korelacji Pearsona,

- korelację Spearmana,

- test chi-kwadrat.



Najważniejsze cechy:

- cp,

- exang,

- oldpeak,

- thalach,

- ca.


# Zastosowane modele

Porównano następujące modele:

- regresja logistyczna,

- drzewo decyzyjne,

- las losowy (Random Forest).


Modele były trenowane na różnych zestawach cech (wszystkie cechy oraz wybrane na podstawie analizy).

# Wyniki

Porównanie dokładności modeli:

- regresja logistyczna: 0.81

- regresja logistyczna (z selekcją cech): 0.85

- drzewo decyzyjne (głębokość 4): 0.84

- drzewo decyzyjne (głębokość 9): 0.99

- las losowy (wybrane cechy): 0.92–0.98

- las losowy (wszystkie cechy): 1.00


Najlepsze wyniki osiągnął model Random Forest.

# Wnioski

- Modele Random Forest i Decision Tree osiągają najwyższą skuteczność.
  
- Najważniejsze cechy mają bezpośredni związek z objawami choroby serca.
  
- Bardzo wysoka dokładność (bliska 100%) może wskazywać na przeuczenie modelu.
  
- Regresja logistyczna daje bardziej interpretowalne, ale mniej dokładne wyniki.
  

# Ograniczenia

niewielki rozmiar zbioru danych,

możliwe przeuczenie modeli,
