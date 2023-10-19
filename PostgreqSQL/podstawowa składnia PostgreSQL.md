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
