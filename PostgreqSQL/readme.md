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

# Język bazodanowy PostgreSQL
Jezykiem wykorzystywanym przez PostgreSQL jest jezyk **SQL**(ang. Structured Query Language) - który jest opracowanym w latach 70 strukturalnym oraz deklaratywnym językiem zapytań. Jest to język dziedzinowy używany do tworzenia, modyfikowania relacyjnych baz danych. 

## Podział zapytań w SQL
Użycie SQL, zgodnie z jego nazwą, polega na zadawaniu zapytań do bazy danych. Zapytania można zaliczyć do jednego z czterech głównych podzbiorów:

* SQL DML (ang. Data Manipulation Language) – język manipulacji danymi
* SQL DDL (ang. Data Definition Language) – język definicji danych
* SQL DCL (ang. Data Control Language) – język kontroli nad danymi
* SQL DQL (ang. Data Query Language) – język definiowania zapytań

## Składnia i polecenia PostgreSQL
Dane wejściowe SQL składają się z sekwencji poleceń. Polecenie składa się ze słów kluczowych które są łatwe do zapamiętania, ponieważ są poprostu angielskimi słowami oznaczającymi czynność za kórą odpowiadają. Każde polecenie musi być zakończone średnikiem(;) umozliwia to na wykonanie więcej niz jdenej instrukcji

## Najważniejsze polecenia SQL
* SELECT - pobiera dane z bazy danych
* UPDATE - aktualizuje dane w bazie danych
* DELETE - usuwa dane z bazy danych
* INSERT INTO - wstawia nowe dane do bazy danych
*  CREATE DATABASE - tworzy nową bazę danych
*  ALTER DATABASE - modyfikuje bazę danych
*  CREATE TABLE -  tworzy nową tabelę
*  ALTER TABLE - modyfikuje tabelę
*  DROP TABLE - usuwa tabelę
*  REATE INDEX - REATE INDEX - tworzy indeks (klucz wyszukiwania)
*  DROP INDEX - usuwa indeks

## Przykładowe zapytania

```sql
SELECT *
    FROM pracownicy
    WHERE pensja > 2000
    ORDER BY staz DESC;
``` 
Zwraca tabelę (listę) utworzoną ze wszystkich kolumn (*) tabeli „pracownicy” (**FROM pracownicy**) zawierającą pracowników, których pensja jest większa niż 2000 (**WHERE pensja > 2000**) i sortuje wynik malejąco według parametru staz (**ORDER BY staz DESC**)  

```sql
INSERT INTO pracownicy
    (imie, nazwisko, pensja, staz)
VALUES
    ('Jan', 'Kowalski', 5500, 1);
```  
Dodaje do tabeli „pracownicy” (**INTO pracownicy**) wiersz (rekord) zawierający dane pojedynczego pracownika.  

```sql
CREATE TABLE pracownicy
(
    imie varchar(255),
    nazwisko varchar(255),
    pensja float,
    staz int
);
```  
Tworzy tabelę „pracownicy” zawierającą pola tekstowe zmiennej długości (varchar) o nazwach „imie” (imię) i „nazwisko”, o maksymalnej długości 255 znaków, zapisaną za pomocą liczby rzeczywistej (float od ang. floating point) pensję oraz zapisany za pomocą liczby całkowitej (int od ang. integer) staż.
