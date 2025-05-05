# Bazy Danych

# Typy baz danych

## 1. Relacyjne bazy danych (RDBMS)
- **Opis**: Dane przechowywane w tabelach (wiersze i kolumny).
- **Język zapytań**: SQL (`SELECT`, `JOIN`, `INSERT`, itd.)
- **Cechy**: Silna spójność, integralność, relacje między danymi.
- **Przykłady**: PostgreSQL, MySQL, Oracle, SQL Server

---

## 2. Hierarchiczne bazy danych
- **Opis**: Struktura drzewa (rodzic → dziecko).
- **Cechy**: Szybki dostęp, mało elastyczne.
- **Przykłady**: IBM IMS

---

## 3. Sieciowe bazy danych
- **Opis**: Dane powiązane w grafie (relacje wiele-do-wielu).
- **Cechy**: Lepsze niż hierarchiczne dla złożonych relacji.
- **Przykłady**: Integrated Data Store (IDS)

---

## 4. Obiektowe bazy danych (OODBMS)
- **Opis**: Dane jako obiekty (jak w OOP).
- **Zastosowanie**: Systemy CAD, multimedia.
- **Przykłady**: ObjectDB, db4o

---

## 5. Dokumentowe bazy danych (NoSQL)
- **Opis**: Dokumenty w formacie JSON, BSON itd.
- **Cechy**: Brak sztywnego schematu, elastyczne.
- **Przykłady**: MongoDB, CouchDB

---

## 6. Klucz-wartość (Key-Value Store)
- **Opis**: Proste pary klucz → wartość.
- **Cechy**: Bardzo szybkie, skalowalne.
- **Przykłady**: Redis, Amazon DynamoDB

---

## 7. Grafowe bazy danych
- **Opis**: Wierzchołki (obiekty) i krawędzie (relacje).
- **Zastosowanie**: Analiza sieci, zależności.
- **Przykłady**: Neo4j, ArangoDB

---

## 8. Kolumnowe bazy danych
- **Opis**: Przechowywanie danych kolumnowo.
- **Zastosowanie**: Analityka, hurtownie danych.
- **Przykłady**: ClickHouse, Apache Cassandra, Amazon Redshift

---

## 9. Bazy danych typu Time-Series
- **Opis**: Dane z sygnaturą czasową.
- **Zastosowanie**: IoT, monitoring, analiza czasowa.
- **Przykłady**: InfluxDB, TimescaleDB, Prometheus

---

## 10. Wektorowe bazy danych (Vector DBs)
- **Opis**: Przechowywanie i przeszukiwanie wektorów.
- **Zastosowanie**: AI, LLMs, wyszukiwanie semantyczne.
- **Przykłady**: Weaviate, Pinecone, Milvus

---

# Elementy projektowania i implementacji baz danych

Proces projektowania i implementacji baz danych zawiera szereg istotnych faz:
- **Tabele i ich struktura**
- **Klucze**
- **Zależności i związki między tabelami**
- **Normalizacja**
- **Optymalizacja i indeksy**

### Analiza wymagań
- Zbieranie informacji od użytkowników
- Zrozumienie procesów biznesowych i danych

### Modelowanie danych (np. ERD)
- Tworzenie diagramów z encjami i relacjami (Entity-Relationship Diagram)
- Wybór typów relacji: 1:1, 1:N, N:M

### Typy danych i atrybuty
- Określenie typów (np. INT, VARCHAR, DATE)
- Ustalanie ograniczeń (np. `NOT NULL`, `DEFAULT`, `UNIQUE`)

### Reguły integralności danych
- Spójność encji i relacji
- Stosowanie ograniczeń (`CHECK`, `FOREIGN KEY`, `UNIQUE`)

### Bezpieczeństwo danych
- Kontrola dostępu (role, uprawnienia)
- Szyfrowanie i ochrona wrażliwych danych

### Testowanie i walidacja projektu
- Testy funkcjonalne i wydajnościowe
- Przeglądy zgodności ze specyfikacją

## Rodzaje kluczy w bazach danych

### 1. Klucz główny (Primary Key)
- Unikalnie identyfikuje każdy wiersz w tabeli.
- Nie może zawierać wartości NULL.
- Każda tabela może mieć tylko jeden klucz główny.

### 2. Klucz obcy (Foreign Key)
- Wskazuje na `Primary Key` w innej tabeli.
- Umożliwia powiązanie danych pomiędzy tabelami.

### 3. Klucz kandydujący (Candidate Key)
- Każdy zestaw kolumn, który mógłby pełnić rolę klucza głównego.
- Tylko jeden zostaje wybrany jako `Primary Key`, pozostałe są kandydatami.

### 4. Klucz alternatywny (Alternate Key)
- Każdy `Candidate Key`, który nie został wybrany jako `Primary Key`.

### 5. Klucz złożony (Composite Key)
- Składa się z więcej niż jednej kolumny.
- Używany, gdy pojedyncza kolumna nie może zapewnić unikalności.

### 6. Klucz sztuczny (Surrogate Key)
- Sztucznie wprowadzona kolumna, np. `ID` typu `AUTO_INCREMENT`.
- Zwykle nie ma znaczenia biznesowego, ale gwarantuje unikalność.

### 7. Klucz naturalny (Natural Key)
- Atrybut rzeczywisty z danych biznesowych, np. PESEL, NIP, e-mail.
- Może służyć jako `Primary Key`, jeśli jest stabilny i unikalny.


# Podstawy diagramu ERD (Entity-Relationship Diagram)

## Główne elementy ERD 

- **Encja (Entity)** – obiekt lub pojęcie, które chcemy przechowywać w bazie danych (np. Klient, Zamówienie).
- **Atrybut (Attribute)** – cecha encji (np. imię, data zamówienia).
- **Relacja (Relationship)** – powiązanie między encjami (np. Klient składa Zamówienie).
- **Klucz główny (PK)** – unikalny identyfikator encji.
- **Klucz obcy (FK)** – odwołanie do `PK` innej encji.

## Typy relacji

1. **Jeden do jednego (1:1)** – np. osoba ↔ paszport
2. **Jeden do wielu (1:N)** – np. klient → zamówienia
3. **Wiele do wielu (M:N)** – np. student ↔ kurs (wymaga tabeli pośredniczącej)


# Tabela, Widok i Widok zmaterializowany


## Tabela (Table)
- Fizycznie przechowuje dane.
- Można wykonywać operacje `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
- Dane są trwale zapisane w bazie.
  
## Widok (View)
- Logiczna reprezentacja zapytania SELECT.
- Nie przechowuje danych fizycznie – odświeżane przy każdym wywołaniu.
- Użyteczne dla ukrycia złożoności, kontroli dostępu, agregacji.

## Widok zmaterializowany (Materialized View)
- Widok, który fizycznie przechowuje dane (cache zapytania).
- Szybszy od zwykłego widoku przy dużych zapytaniach.
- Trzeba go odświeżać (REFRESH MATERIALIZED VIEW), aby dane były aktualne.

# Mechanizm transakcyjny

Transakcja to **logiczny zbiór operacji na danych**, który musi zostać wykonany w całości albo wcale.

```
BEGIN;

UPDATE konta SET saldo = saldo - 100 WHERE id = 1;  -- klient A wysyła 100 zł
UPDATE konta SET saldo = saldo + 100 WHERE id = 2;  -- klient B otrzymuje 100 zł

COMMIT;  -- zatwierdzenie zmian
```

Jeśli w dowolnym miejscu wystąpi błąd (np. brak konta), możemy przerwać operację:

```
ROLLBACK;  -- cofnięcie wszystkich zmian
```

| Poziom izolacji        | Przeciwdziała                  | Uwaga |
|------------------------|---------------------------------|-------|
| **READ UNCOMMITTED**   | ❌ nic                         | Można widzieć niezatwierdzone dane (ang. dirty reads) |
| **READ COMMITTED**     | ✅ dirty reads                 | Domyślny w PostgreSQL |
| **REPEATABLE READ**    | ✅ dirty + non-repeatable reads | Widok danych nie zmienia się w trakcie transakcji |
| **SERIALIZABLE**       | ✅ wszystkie anomalie          | Najbezpieczniejszy, ale najmniej wydajny |

## Gdzie stosować transakcje?

- W systemach finansowych (np. przelewy)
- W procesach rejestracji (np. użytkownik + jego dane kontaktowe)
- Podczas importu wielu rekordów – łatwe cofanie w razie błędu
- W aplikacjach wymagających silnej spójności danych


# Języki SQL

## DDL – Data Definition Language
- Służy do **tworzenia, modyfikowania i usuwania** struktur bazy danych.
- Działa na poziomie **schematu** (struktury, nie danych).
- Operacje DDL są zazwyczaj **automatycznie zatwierdzane** (`auto-commit`).

###  Główne polecenia DDL:
- `CREATE` – tworzy nową tabelę, widok, indeks, itd.
- `ALTER` – zmienia istniejącą strukturę (np. dodaje kolumnę)
- `DROP` – usuwa tabelę, widok, indeks
- `TRUNCATE` – usuwa wszystkie dane z tabeli (szybciej niż `DELETE`)
- `RENAME` – zmienia nazwę obiektu

###  Przykład DDL:
```sql
CREATE TABLE produkty (
    id INT PRIMARY KEY,
    nazwa VARCHAR(100),
    cena DECIMAL
);
```
## DML – Data Manipulation Language

DML to podzbiór języka SQL służący do **manipulowania danymi** w istniejących strukturach baz danych (tabelach).

###  Główne polecenia DML
- SELECT – pobieranie danych
- INSERT – dodawanie danych
- UPDATE – modyfikacja danych
- DELETE – usuwanie danych

### Cechy DML
- Operuje na danych, nie zmienia struktury tabel.
- Działa wewnątrz transakcji – można użyć COMMIT lub ROLLBACK.
- Wspiera filtrację (WHERE), sortowanie (ORDER BY), łączenia (JOIN), itd.

### Przykład DML:

```
BEGIN;

INSERT INTO konta (id, saldo) VALUES (1, 1000);
UPDATE konta SET saldo = saldo - 200 WHERE id = 1;
DELETE FROM konta WHERE saldo < 0;

COMMIT;
```

### Gdzie stosować DML?
- Pobieranie danych do aplikacji
- Tworzenie i aktualizacja rekordów
- Obsługa formularzy, logów, transakcji
- Operacje masowe na danych






