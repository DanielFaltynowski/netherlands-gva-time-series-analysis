# 🇳🇱 Netherlands Gross Value Added (GVA): Time Series Analysis

Niniejsze repozytorium zawiera projekt zaliczeniowy z przedmiotu **Analiza Szeregów Czasowych**, którego celem jest analiza szeregu czasowego przedstawiającego **wartość dodaną brutto (Gross Value Added, GVA) w Holandii** w okresie **2015Q1–2025Q2** oraz budowa modeli mogących znaleźć zastosowanie w **prognozowaniu**.

Projekt obejmuje pełen proces analizy szeregów czasowych — od wstępnego przetwarzania danych, przez modelowanie ekonometryczne, aż po interpretację wyników.

Wykorzystane narzędzia: Excel, Gretl

### Zakres projektu

W ramach projektu zrealizowano następujące etapy analizy:

- dekompozycja szeregu czasowego (usuwanie trendu i sezonowości),
- deflacja danych – konwersja cen nominalnych do cen stałych,
- estymacja modeli przy użyciu **klasycznej metody najmniejszych kwadratów (KMNK)**,
- identyfikacja i analiza **załamania strukturalnego** spowodowanego pandemią COVID-19,
- analiza autokorelacji i własności składnika losowego,
- zastosowanie **zmiennych sztucznych (dummy variables)**,
- budowa i analiza **modeli autoregresyjnych (AR)**.

Projekt ma charakter analityczno-modelowy i stanowi spójną podstawę do dalszych prac prognostycznych oraz rozbudowy o bardziej zaawansowane modele.

# Raport

*W tej sekcji przedstawiono kluczowe etapy analizy oraz najważniejsze wnioski.  
W celu zapoznania się z pełnym projektem oraz kompletną dokumentacją obliczeń i modeli, zapraszam do przejrzenia pliku Excel znajdującego się w folderze* `src`*.*

### Opis szeregu

Wartość dodana brutto (GVA – *Gross Value Added*) jest miarą określającą, ile realnej wartości ekonomicznej zostało wytworzone w gospodarce przez przedsiębiorstwa, sektory gospodarki lub całe państwo w danym okresie.

Analizowany szereg czasowy opisany jest przez następujące zmienne:

- $t$ — zmienna reprezentująca czas,  
- $GVA_t$ — wartość dodana brutto w okresie $t$.

### Dekompozycja szeregu czasowego

Do usunięcia trendu zastosowano **różnicowanie pierwszego rzędu** (*first-order differencing*):

$$
GVA_{\text{no\_trend}} = GVA_{t} - GVA_{t-1}
$$

Sezonowość usunięto metodą **addytywnej dekompozycji sezonowej z wykorzystaniem wskaźników sezonowych**:

$$
GVA_{\text{no_trend_and_no_seasonality}} = GVA_{\text{no_trend}} - \text{cleaned_indicator}(q)
$$
