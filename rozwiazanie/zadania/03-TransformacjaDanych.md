# Transformacja danych

Dane w folderze `data/interim` są przygotowane do dalszej obróbki. Ponieważ są w postaci tabelarycznej, możemy dalej je przetwarzać używając `Pandas`. Przed przejściem do analizy danych wykonaj następujące zadania:

1. Do dalszej analizy wybierz tylko te oferty, które są kwotowane w `PLN`,
1. Nazwy ofert pracy oraz miasta (kolumny `name` oraz `location_city`) zmień by były z małych liter,
1. Dodaj nową kolumną `salary_avg` jako średnia z kolumn `salary_high`, `salary_low`,
1. Zunifikuj nazwy miast np. `wroclove, wroclaw, wrocław` powinno zostać zmienione na `wrocław`,
1. Ofertą, gdzie jest dostępna tylko praca zdalna (kolumna `location_city`), i nie jest podana informacja o kraju zatrudnienia `location_country`, jako kraj ustaw `B/D` (brak danych),
1. Dodaj nową kolumnę `is_senior`, która będzie informowała o tym, czy stanowisko jest seniorskie czy nie. Np. Senior Data Analyst -> is_senior = 1,
1. Wyniki zapisz do pliku `data/processed/job_offers.csv` używając separatora `;`, kodowania `UTF-8` oraz bez indexu (`index=False`)