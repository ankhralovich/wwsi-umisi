# Systemy liczbowe

## System dwójkowy (binarne):
- Podstawa: 2
- Cyfry: 0, 1
- Przykład: 1010₂ = 10₁₀
- Używany w komputerach (bity i bajty).

## System ósemkowy:
- Podstawa: 8
- Cyfry: 0, 1, 2, 3, 4, 5, 6, 7
- Przykład: 12₈ = 10₁₀
- Czasem używany w programowaniu.

## System dziesiętny:
- Podstawa: 10
- Cyfry: 0-9
-  Przykład: 10₁₀ = 10₁₀
- Najczęściej używany przez ludzi.

## System szesnastkowy (heksadecymalny):
-  Podstawa: 16
- Cyfry: 0-9, A-F (gdzie A=10, B=11, ..., F=15)
-  Przykład: A₁₆ = 10₁₀
- Używany w adresach IP, kolorach w HTML (np. #FF5733).

# Sieć komputerowa

## **Urządzenia sieciowe:**

1. **Przełącznik (switch):**  
   - Przełącza pakiety między urządzeniami w sieci lokalnej (LAN).  
   - Działa na warstwie 2 (model OSI).  

2. **Ruter (router):**  
   - Łączy różne sieci i przesyła dane między nimi.  
   - Działa na warstwie 3 (model OSI).  

3. **Most (bridge):**  
   - Łączy dwie sieci lokalne, np. segmenty LAN.  
   - Działa na warstwie 2.

4. **Wzmacniacz (repeater):**  
   - Wzmacnia sygnał w sieci przewodowej lub bezprzewodowej.  
   - Przydatny przy dużych odległościach.

5. **Systemy IDS/IPS:**  
   - **IDS (Intrusion Detection System):** Wykrywa ataki w sieci.  
   - **IPS (Intrusion Prevention System):** Wykrywa i zapobiega atakom.  

6. **Serwery:**  
   - Oferują usługi (np. WWW, e-mail, pliki) dla klientów w sieci.

7. **Firewalle:**  
   - Kontrolują ruch sieciowy, chroniąc przed nieautoryzowanym dostępem.

8. **Drukarki, komputery, smartfony:**  
   - Urządzenia końcowe w sieci, które korzystają z zasobów sieciowych.

---

## **Media transmisyjne:**

1. **Przewodowe:**
   - **Miedziane:**  
     - Kable UTP, STP, coaxial (np. Ethernet).  
     - Tanie, ale podatne na zakłócenia.  
   - **Światłowodowe:**  
     - Przesyłają dane za pomocą światła.  
     - Bardzo szybkie i odporne na zakłócenia.  

2. **Bezprzewodowe:**
   - **Wi-Fi:**  
     - Używa fal radiowych (np. 2.4 GHz, 5 GHz).  
     - Wygodne, ale mniej stabilne niż przewodowe połączenia.

---

## **Protokoły:**

1. **Ethernet:**  
   - Podstawowy protokół w sieciach LAN.  

2. **IP (Internet Protocol):**  
   - Adresuje i przesyła dane między sieciami (IPv4, IPv6).  

3. **TCP/UDP:**  
   - **TCP (Transmission Control Protocol):** Niezawodny, kontroluje poprawność transmisji.  
   - **UDP (User Datagram Protocol):** Szybszy, ale mniej niezawodny (np. VoIP, gry).  

4. **HTTP/HTTPS:**  
   - Protokół komunikacji dla stron WWW. HTTPS szyfruje dane (SSL/TLS).  

5. **DNS (Domain Name System):**  
   - Tłumaczy nazwy domen (np. google.com) na adresy IP.
  
6. **FTP/SFTP:**  
   - Używane do przesyłania plików przez sieć.

# Typy sieci komputerowych

1. **Peer-to-Peer (P2P):**
   - Wszystkie urządzenia mają równorzędny status (brak serwera).  
   - Każdy komputer może działać jako klient i serwer.  
   - Przykład: udostępnianie plików między komputerami.  
   - Zaleta: prostota, brak centralnego zarządzania.  
   - Wada: trudne zarządzanie w dużych sieciach.

---

2. **LAN (Local Area Network):**
   - Sieć lokalna, np. w domu, biurze lub szkole.  
   - Ograniczona zasięgiem (kilkaset metrów).  
   - Przykład: sieć w biurze z komputerami i drukarką.  
   - Zaleta: wysoka szybkość i niezawodność.  
   - Wada: ograniczony zasięg.

---

3. **MAN (Metropolitan Area Network):**
   - Obejmuje większy obszar, np. miasto.  
   - Łączy różne sieci LAN.  
   - Przykład: sieć dla całego kampusu uniwersyteckiego.  
   - Zaleta: większy zasięg niż LAN.  
   - Wada: wyższe koszty budowy i utrzymania.

---

4. **WAN (Wide Area Network):**
   - Sieć rozległa, łącząca różne lokalizacje na dużych odległościach.  
   - Może obejmować miasta, kraje, a nawet kontynenty.  
   - Przykład: Internet jako największy przykład WAN.  
   - Zaleta: globalny zasięg.  
   - Wada: niższa szybkość niż w LAN/MAN.


# Typy sieci: Intranet, Ekstranet, Internet

#### **1. Intranet:**
- **Definicja:** Prywatna sieć, dostępna tylko dla określonej grupy użytkowników (np. pracowników firmy).  
- **Przykład:** Sieć wewnętrzna w biurze, gdzie pracownicy mogą korzystać z firmowego oprogramowania, dokumentów i usług.  
- **Zalety:**
  - Bezpieczeństwo – ograniczony dostęp dla osób z zewnątrz.
  - Ułatwia współpracę w organizacji.  
- **Wady:**
  - Ograniczony zasięg (tylko wewnątrz firmy).  

---

#### **2. Ekstranet:**
- **Definicja:** Rozszerzenie intranetu, które umożliwia dostęp do wybranych zasobów także zewnętrznym użytkownikom (np. partnerom biznesowym).  
- **Przykład:** Portal dla dostawców, gdzie mogą sprawdzić zamówienia lub status płatności.  
- **Zalety:**
  - Ułatwia współpracę między firmą a partnerami/dostawcami.
  - Kontrolowany dostęp dla użytkowników spoza firmy.  
- **Wady:**
  - Ryzyko naruszenia bezpieczeństwa, jeśli nie jest odpowiednio zabezpieczony.

---

#### **3. Internet:**
- **Definicja:** Globalna sieć łącząca miliardy urządzeń na całym świecie.  
- **Przykład:** Przeglądanie stron WWW, korzystanie z e-maila, przesyłanie plików.  
- **Zalety:**
  - Globalny zasięg.
  - Ogromna ilość dostępnych zasobów i usług.  
- **Wady:**
  - Brak pełnej kontroli nad danymi.
  - Ryzyko cyberataków.

---

**Podsumowanie różnic:**
| Typ       | Zasięg          | Dostęp                   | Przykład użycia               |
|-----------|-----------------|--------------------------|-------------------------------|
| Intranet  | Wewnątrz firmy  | Tylko dla pracowników    | Portal firmowy                |
| Ekstranet | Firma + partnerzy | Wybrane osoby spoza firmy | Portal dostawców           |
| Internet  | Globalny        | Otwarty dla wszystkich   | WWW, e-mail, social media     |


# Modele: ISO/OSI i TCP/IP

## **1. Model ISO/OSI (Open Systems Interconnection):**
- **Definicja:** Teoretyczny model komunikacji sieciowej, dzielący proces komunikacji na 7 warstw.  
- **Cel:** Standaryzacja komunikacji między urządzeniami różnych producentów.  
- **Warstwy:**
  1. **Fizyczna:** Przesył sygnałów przez media transmisyjne (kable, fale).  
     - Przykład: Ethernet, USB.
  2. **Łącza danych:** Kontrola dostępu do medium, korekcja błędów.  
     - Przykład: MAC, ARP.
  3. **Sieciowa:** Adresowanie i routowanie pakietów między sieciami.  
     - Przykład: IP.  
  4. **Transportowa:** Zapewnienie niezawodności transmisji (kontrola błędów).  
     - Przykład: TCP, UDP.  
  5. **Sesji:** Zarządzanie sesjami (nawiązanie, utrzymanie, zakończenie).  
     - Przykład: NetBIOS, RPC.  
  6. **Prezentacji:** Konwersja danych (np. szyfrowanie, kompresja).  
     - Przykład: SSL/TLS.  
  7. **Aplikacji:** Interakcja użytkownika z siecią (usługi i aplikacje).  
     - Przykład: HTTP, FTP.  
- **Zalety:**  
  - Jasny podział funkcji.
  - Ułatwia naukę i diagnozowanie problemów.

---

## **2. Model TCP/IP (Transmission Control Protocol / Internet Protocol):**
- **Definicja:** Praktyczny model, który opisuje działanie Internetu.  
- **Warstwy:**
  1. **Dostęp do sieci:** Odpowiada za przesył danych w sieci lokalnej.  
     - Przykład: Ethernet, Wi-Fi.  
  2. **Internetu:** Adresowanie i routowanie pakietów między sieciami.  
     - Przykład: IP (IPv4/IPv6).  
  3. **Transportu:** Zarządza niezawodnością transmisji danych.  
     - Przykład: TCP, UDP.  
  4. **Aplikacji:** Obsługuje protokoły i usługi widoczne dla użytkownika.  
     - Przykład: HTTP, DNS, FTP.  
- **Zalety:**  
  - Prostota i praktyczność.  
  - Szeroko stosowany w Internecie.  

---

## **Porównanie ISO/OSI i TCP/IP:**

| Cecha                   | Model ISO/OSI              | Model TCP/IP                  |
|-------------------------|----------------------------|-------------------------------|
| Liczba warstw           | 7                          | 4                             |
| Podejście               | Teoretyczne                | Praktyczne                    |
| Złożoność               | Bardziej szczegółowy       | Prostota                      |
| Zastosowanie            | Standard edukacyjny        | Podstawa działania Internetu  |
| Przykłady protokołów    | HTTP, FTP, IP, SSL         | HTTP, FTP, TCP, IP            |


# Urządzenia sieciowe

## **1. Karta sieciowa (NIC - Network Interface Card):**
- **Funkcja:** Umożliwia urządzeniom łączenie się z siecią.  
- **Adres MAC:**  
  - Każda karta sieciowa posiada unikalny adres MAC (Media Access Control).  
  - Adres MAC ma 48 bitów (np. `00:1A:2B:3C:4D:5E`).  
  - Służy do identyfikacji urządzenia w sieci lokalnej (warstwa 2 OSI).  

---

## **2. Ruter (Router):**
- **Funkcja:**  
  - Łączy różne sieci i przesyła dane między nimi (np. LAN z Internetem).  
  - Działa na warstwie 3 OSI (sieciowej).  
- **Dodatkowe cechy:**
  - Umożliwia translację adresów (NAT).  
  - Może mieć funkcje Wi-Fi i firewalla.

---

#### **3. Hub (koncentrator):**
- **Funkcja:**  
  - Wysyła dane do **wszystkich urządzeń** w sieci.  
  - Nie rozróżnia odbiorcy – każde urządzenie musi sprawdzić, czy dane są dla niego.  
- **Wady:**  
  - Powoduje **kolizje** pakietów w sieci (przestarzałe rozwiązanie).  
- **Warstwa OSI:** 1 (fizyczna).  

---

## **4. Switch (przełącznik):**
- **Funkcja:**  
  - Wysyła dane **tylko do jednego urządzenia**, do którego są przeznaczone.  
  - Używa adresów MAC do identyfikacji urządzeń.  
- **Zalety:**  
  - Brak kolizji w sieci (wydajniejsze niż hub).  
  - Podstawowe urządzenie w sieciach LAN.  
- **Warstwa OSI:** 2 (łącza danych).

---

## **Podsumowanie różnic między Hub i Switch:**

| Cecha                  | Hub                         | Switch                       |
|------------------------|-----------------------------|------------------------------|
| Sposób wysyłania danych| Do wszystkich urządzeń      | Do konkretnego urządzenia    |
| Kolizje               | Tak                         | Nie                          |
| Inteligencja          | Brak                        | Używa tablic adresów MAC     |
| Warstwa OSI           | Fizyczna (1)                | Łącza danych (2)             |


# Adresowanie logiczne i fizyczne

## **1. Adresowanie logiczne:**
- **Definicja:** Adres przypisywany na poziomie oprogramowania, który identyfikuje urządzenie w sieci.  
- **Charakterystyka:**
  - Używane w warstwie sieciowej (OSI, warstwa 3).
  - Może być zmieniane (dynamiczne lub statyczne).  
  - Adresem logicznym jest **adres IP** (IPv4 lub IPv6).
- **Przykład:**
  - IPv4: `192.168.1.1`  
  - IPv6: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`  
- **Zastosowanie:**  
  - Adres logiczny wskazuje, **gdzie znajduje się urządzenie w sieci** (np. w Internecie).

---

## **2. Adresowanie fizyczne:**
- **Definicja:** Adres przypisany na poziomie sprzętowym, który identyfikuje urządzenie w sieci lokalnej (LAN).  
- **Charakterystyka:**
  - Używane w warstwie łącza danych (OSI, warstwa 2).  
  - Jest unikalny dla każdej karty sieciowej (NIC).  
  - Adresem fizycznym jest **adres MAC** (Media Access Control).  
- **Przykład:**  
  - `00:1A:2B:3C:4D:5E` (adres MAC składa się z 48 bitów).  
- **Zastosowanie:**  
  - Adres fizyczny wskazuje, **które urządzenie odbiera dane** w sieci lokalnej.  

---

#### **Różnice między adresowaniem logicznym i fizycznym:**

| Cecha                  | Adresowanie logiczne         | Adresowanie fizyczne          |
|------------------------|------------------------------|--------------------------------|
| Warstwa OSI            | Sieciowa (3)                | Łącza danych (2)              |
| Typ adresu             | IP (IPv4/IPv6)              | MAC                           |
| Możliwość zmiany       | Tak                         | Nie (przypisany przez producenta) |
| Zakres                 | Globalny (Internet)         | Lokalny (sieć LAN)            |
| Przykład               | `192.168.0.1`               | `00:1A:2B:3C:4D:5E`           |


# Rodzaje adresów w sieciach komputerowych

## **1. Adres sieci (network address):**
- **Definicja:**  
  - Adres identyfikujący **całą sieć**, a nie pojedyncze urządzenie.
- **Charakterystyka:**
  - Wszystkie bity części hosta w adresie IP są ustawione na `0`.  
  - Określa początek zakresu adresów IP w danej sieci.
- **Przykład:**
  - Adres IP: `192.168.1.0/24`  
    - `192.168.1.0` to adres sieci, maska `255.255.255.0`.
- **Zastosowanie:**
  - Do identyfikacji sieci w routingu i konfiguracjach.

---

## **2. Adres hosta (host address):**
- **Definicja:**  
  - Adres przypisany konkretnemu urządzeniu w sieci.
- **Charakterystyka:**
  - Znajduje się pomiędzy adresem sieci a adresem broadcast.  
  - Wszystkie bity w części hosta są różne od `0` i `1`.  
  - W sieci `192.168.1.0/24` przykładowe adresy hostów to:  
    - `192.168.1.1`  
    - `192.168.1.254`.  
- **Zastosowanie:**
  - Identyfikacja urządzeń (komputerów, drukarek, itp.).

---

## **3. Adres rozgłoszeniowy (broadcast address):**
- **Definicja:**  
  - Specjalny adres używany do wysyłania danych **do wszystkich urządzeń** w danej sieci.
- **Charakterystyka:**
  - Wszystkie bity części hosta w adresie IP są ustawione na `1`.  
  - Przykład w sieci `192.168.1.0/24`:  
    - Adres rozgłoszeniowy: `192.168.1.255`.  
- **Zastosowanie:**
  - Wysyłanie wiadomości do wszystkich hostów w sieci lokalnej.

---

## **Przykład w sieci 192.168.1.0/24:**

| Typ adresu            | Wartość                  |
|-----------------------|--------------------------|
| **Adres sieci**       | `192.168.1.0`           |
| **Adres hosta**       | `192.168.1.1` - `192.168.1.254` |
| **Adres broadcast**   | `192.168.1.255`         |


# Klasy adresów IP

## **1. Klasy adresów IPv4:**
- Adresy IPv4 zostały pierwotnie podzielone na **klasy**, aby zarządzać różnymi rozmiarami sieci.

| **Klasa** | **Zakres adresów**         | **Ilość sieci**     | **Ilość hostów w sieci**       |
|-----------|----------------------------|---------------------|--------------------------------|
| **A**     | `0.0.0.0` – `127.255.255.255` | 128 (duże sieci)   | ~16 milionów (2³¹-2)           |
| **B**     | `128.0.0.0` – `191.255.255.255` | 16 384            | ~65 tysięcy (2¹⁶-2)           |
| **C**     | `192.0.0.0` – `223.255.255.255` | 2 miliony         | 254 (2⁸-2)                    |
| **D**     | `224.0.0.0` – `239.255.255.255` | Multicast         | N/A                           |
| **E**     | `240.0.0.0` – `255.255.255.255` | Zarezerwowane     | N/A                           |

- **Klasy A, B, C**: Używane do standardowego adresowania w sieciach.  
- **Klasa D**: Używana do multicastu (rozsyłanie do grup).  
- **Klasa E**: Zarezerwowana dla badań i testów.

---

## Adres bezklasowy (CIDR - Classless Inter-Domain Routing)
- **Definicja:** System, który zastąpił podział na klasy adresów IP.  
- **Zakres:** Określany za pomocą notacji `adres/maska`.  
- **Przykład:**
  - `192.168.1.0/24` – oznacza sieć z maską 255.255.255.0 (24 bity dla sieci).  
  - `192.168.1.0/28` – oznacza sieć z mniejszą liczbą hostów (16 adresów).  
- **Zaleta:**  
  - Lepsze wykorzystanie przestrzeni adresowej (np. możliwość tworzenia sieci o niestandardowym rozmiarze).

---

## Podsieci (Subnetting)
- **Definicja:** Proces dzielenia dużej sieci na mniejsze części (podsiec).  
- **Zalety:**  
  - Lepsze zarządzanie ruchem sieciowym.  
  - Izolacja i zwiększenie bezpieczeństwa.  
- **Przykład:**  
  Sieć `192.168.1.0/24` można podzielić na 4 podsieci:  
  - `192.168.1.0/26` (64 adresy)  
  - `192.168.1.64/26` (64 adresy)  
  - `192.168.1.128/26` (64 adresy)  
  - `192.168.1.192/26` (64 adresy)

---

## Maski podsieci
- **Maska podsieci:** Określa, która część adresu IP odnosi się do sieci, a która do hostów.  
- **Przykłady masek:**
  | **CIDR** | **Maska dziesiętna** | **Ilość hostów** |
  |----------|----------------------|------------------|
  | `/8`     | `255.0.0.0`          | ~16 mln          |
  | `/16`    | `255.255.0.0`        | ~65 tys.         |
  | `/24`    | `255.255.255.0`      | 254              |
  | `/30`    | `255.255.255.252`    | 2 (np. połączenie punkt-punkt) |

- **Obliczanie liczby hostów:**  
  - **Wzór:** \( 2^n - 2 \), gdzie \( n \) to liczba bitów w części hosta.  
  - Dla `/24`: \( 2^8 - 2 = 254 \) hosty.






