# Pobieranie informacji o stronie

Na podstawie plików z katalogu `../data/raw` wyciągnij następujące informacje dotyczące oferty:
- lokalizacja - miasto jak i państwo,
- wynagrodzenie - dolna, górna granica oraz waluta. Jeśli nie ma widełek dolna granica = górnej granicy,
- nazwa stanowiska,
- firma,
- technologia.

Wyniki pojedyńczej oferty zapisz do słownika o następującej konstrukcji:
```
{
    'name': 'nazwa stanowiska',
    'company': 'firma',
    'technology': 'technologia',
    'job': 'informacja o ',
    'location': {'city': 'miasto', 'country': 'panstwo'},
    'salary': {'low': 'dolna granica', 'high': 'gorna granica', 'currency': 'waluta'} 
}

```
Taka konstrukcja danych ma celu przedstawienie kolejnej metody w `Pandas` - `json_normalize` ([link do dokumentacji](https://pandas.pydata.org/docs/reference/api/pandas.json_normalize.html)), ponieważ json jest powszechnie używaną konstrukcją do komunikacji pomiędzy modułami.

Wyniki w postaci `DataFrame` zapisz w katalogu `data/interim/job_offers.csv` używając separatora `;`, kodowania `UTF-8` oraz zapisując dane bez indexu `index=False`.