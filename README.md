# NTPD7

# Zadanie 1.1 
Zadanie polegało na wygenerowaniu zbiorów danych treningowych oraz produkcyjnych. Do tego zadania wykorzystałem generator biblioteki scikit
<img width="709" height="218" alt="image" src="https://github.com/user-attachments/assets/55cfc73b-142b-487a-a557-1c820ddbabaa" />
<img width="619" height="334" alt="image" src="https://github.com/user-attachments/assets/72e964cc-0e0b-45e8-860d-b75d77c695f4" />

# Zadanie 1.2
Następnym etapem było wytrenowanie modelu RandomForestClassifier na utworzonych w poprzednim zadaniu danych treningowych oraz predykcje tego modelu co do danych na produkcji
<img width="632" height="101" alt="image" src="https://github.com/user-attachments/assets/38539669-fa80-4c80-ae8c-67465f0cea07" />

# Zadanie 1.3
Końcowym etapem zadania pierwszego jest analiza danych. Do analizy wykorzystałem metody biblioteki pandas dzięki którym otrzymałem informację dotyczące krztałtu zbioru, typów danych, braków oraz statystyki (średnia, odchylenie, kwartyle, maksimum i minimum) 
<img width="436" height="257" alt="image" src="https://github.com/user-attachments/assets/704b9a84-2e9d-42f5-9865-b4cd1a68e786" />

## Dane treningowe
<img width="648" height="790" alt="image" src="https://github.com/user-attachments/assets/ad779ab6-f567-4e9f-b45e-905e0b755cf0" />

## Dane Produkcyjne
<img width="697" height="817" alt="image" src="https://github.com/user-attachments/assets/d0c4c2bd-2c15-4de0-9900-0fd603899f98" />

# Zadanie 2
Zadanie polegało na zainstalowaniu biblioteki evidently oraz stworzeniu raportu "Data Drift". Przy tworzeniu tego raportu natknąłem się na problem związany z wersjami biblioteki. W najnowszych wersjach rozmieszczenie pakietów tej biblioteki jest zupełnie inne niż w wersji 0.2 (z której dokumentacji korzystałem). W tej wersji również metoda do zapisywania raportu wymaga utworzenia jego snapshota. Z raportu wynika, że drift został zauważony w połowie z cech. 
## Instalacja
<img width="226" height="61" alt="image" src="https://github.com/user-attachments/assets/22e34b6e-3c6b-4238-aa9a-e4f064cd5f4d" />

## Tworzenie oraz zapis raportu
<img width="857" height="250" alt="image" src="https://github.com/user-attachments/assets/7692612f-c6f6-48b2-9990-987fe22c6f8e" />

## Dashboard z wynikami
<img width="1824" height="673" alt="image" src="https://github.com/user-attachments/assets/51651cf3-dd00-4ed0-b831-ea77e0f39362" />

## Wykres driftu z cechy
Na zrzucie jest widoczny wykres Data Drift z cechy "feature_1". Zielony prostokąt obrazuje zakres z wartości treningowych o szerokości jednego odchylenia standardowego. Czerwona linia jest wartością średnią z kolejnych danych produkcyjnych a czerwone tło to wartości pojedynczych cech. Na zrzucie zauważalne jest wykroczenie obydwu czerwonych wskaźników poza zielony prostokąt co wskazuje na data drift między zbiorami.
<img width="1588" height="458" alt="image" src="https://github.com/user-attachments/assets/ee8a8c40-6718-41c5-91d3-c3103ab1181d" />

# Zadanie 3
Utworzono raport z predykcji na danych treningowych oraz produkcyjnych. Z wyników widoczny jest duży spadek w jakości predyckji pomiędzy zbiorami. Model został przeuczony. Spowodowało to bardzo słabe wyniki predykcji na danych z produkcji. Wcześniejszy wynik raportu wskazywał na datadrift. Mogło się to przełożyc na wynik predykcji ponieważ model nie jest przyzwyczajony do tak odbiegających od norm danych (concept drift). Aby naprawić aktualny stan modelu należało by zastosować retraining modelu ze zmienionym zbiorem treningowym np. Wmieszać w dane treningowe pewną ilość danych z produkcji.
<img width="711" height="477" alt="image" src="https://github.com/user-attachments/assets/5ad351cb-03c2-4aa0-b125-8389c2fdaaa4" />
<img width="900" height="442" alt="image" src="https://github.com/user-attachments/assets/a522f26e-d20c-443f-aa71-3f5d350913c8" />



