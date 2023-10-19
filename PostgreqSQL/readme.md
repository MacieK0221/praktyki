# Czym jest PostrgeSQL
PostgreSQL to darmowy, otwarty system zarządzania relacyjnymi bazami danych o bardzo wysokiej dostępności. Początki PostgreSQL sięgają 1986 roku jako część projektu _POSTGRES_ na Uniwersytecie Kalifornijskim w Berkeley i od ponad 35 lat jest stale udoskonalany przez aktywną społeczność ekspertów. PostgreSQL zyskał dobrą reputację dzięki sprawdzonej architekturze, niezawodności, integralności danych, solidnemu zestawowi funkcji np.:
* Typy danych
* Integralność danych
* Współbieżność, wydajność
* Niezawodność, odzyskiwanie po awarii
* Bezpieczeństwo
* Rozciągliwość
* Internacjonalizacja, wyszukiwanie tekstu
# Jak działa PostgreSQL
PostgreSQL jest relacyjno-obiektową bazą danych oznacza to że pozwala na trzymanie danych w postaci tabel opisanych jakimiś relacjami oraz na manipulacje tych danych za pomocą języka zapytań. Dodatkowo, integruje on obiektowe podejście do baz danych z relacyjnym pozwalając na utrzymanie narzędzi znanych z relacyjnych baz danych ale poszerzonych o możliwości związane z obiektowością: obiekty, klasy i dziedziczenie. 

## Porównanie MySQL i PostgreSQL

| Najważniejsze funkcje | MySQL | PostgreSQL |
| :-------------------: | :--: | :--------: |
|Pierwsze kroki|Łatwa obsługa i konfiguracja|Mniej dostępny, ponieważ używany do zarządzania złożonymi zapytaniami i dużymi bazami danych.|
|Open source|Kod źródłowy MySQL jest otwarty. Jest rozpowszechniany na podwójnej licencji GNU GPL oraz licencji własnościowej. Oprogramowanie zawierające kod MySQL jest zatem bezpłatne, jednak aby mogło być sprzedawane, musi uzyskać płatną licencję|Oprogramowanie to jest dostępne z licencją BSD, czyli open source. Może być modyfikowane lub sprzedawane wyłącznie pod warunkiem zamieszczenia wzmianki, że zostało stworzone przez PostgreSQL Development Group.|
|Baza danych| Szybka baza danych dla dużych obciążeń w trybie odczytu |Najbardziej zaawansowana na świecie relacyjna baza danych open source|
|Integralność danych|Tworząc tabele, należy określić typ InnoDB. Dzięki temu nie pojawią się duplikaty wartości|System ten jest szczególnie odpowiedni w przypadku aplikacji z dużą liczbą rekordów. Zapewnia on niezawodność informacji, w szczególności dzięki autonomicznemu systemowi kopii zapasowych i replikacji|

## Zalety PostgreSQL
1. Hybrydowość(relacyjno-obiektowa baza danych)
2. Otwarte Oprogramowanie
3. Niezawodność
