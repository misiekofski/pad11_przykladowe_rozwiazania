# Pobranie danych z NoFluffJobs

Pierwszą częścią zadania będzie pobranie danych ze strony głównej NoFluffJobs, zadanie wykonaj w następujących krokach:

1. Otwierając stronę używając Selenium, pobierz jej zawartość,
1. Dla zapytań _data scientist_, _data engeenier_, _data analyst_ pobierz wszystkie dostępne strony.
1. Strony w formacie `*.html` zapisz w katalogu `../data/raw` jako dane źródłowe. Przyjmiemy następującą konwencję nazewnictwa plików:<br>
```
'{job_name}_{page_number}.html'
```
Przykładowo `data analyst_1.html` będzie oznaczało listę ofert dla analityka danych ze strony pierwszej.

Dodatkowe informacje:
- Pamiętaj o dodaniu odstępu czasowego pomiędzy przejściami na poszczególne strony np. 5 sekund,

- Jako url do otworzenia przez przeglądarkę, możesz użyć następującego szablonu: 
```
'https://nofluffjobs.com/pl/jobs?criteria={job_name}&page={page_number}'
```

- W celu pobrania zawartości HTML strony, możesz posłużyć się np. `element.get_attribute('innerHTML')`,

> Na tym etapie jeszcze nie przetwarzamy danych, pobieramy je w formie takiej, jakiej są dostępne.