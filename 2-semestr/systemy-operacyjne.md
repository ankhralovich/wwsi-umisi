# Systemy operacyjne

## 1. Konta użytkowników i grupy

### Konta 

**Konto użytkownika** -- zbiór danych informujący OS o dostępie do poszczególnych plików, folderów, możliwości wprowadzania zmian. Umożliwia wspólne korzystanie z tego samego komputera z zachowaniem własnych plików i ustawień. Dostęp do konta jest możliwy przy pomocy nazwy użytkownika (ważne!) i hasła -- jednopoziomowe uwierzytelnienie. Drugi etap: biometria, dodatkowy kod sms itd.

Konto funkcyjne -- na przykłąd konto użytkownika logicznego `sekretariat`, dostęp do którego ma kilka osób fizycznych. Rozliczenie konta funkcyjnego jest prowadzone przez Administratora.

**Konto administratora** -- zapewnia najwyższy poziom kontroli nad komputerem. Może instalować programy, ma dostęp do wszystkich plików na komputerze, wprowadzać zmiany na innych kontach użytkowników. 

Po zakończeniu konfigurowania komputera zaleca się korzystanie ze standardowego konta użytkownika do wykonywania codziennych zadań.

Uprawnienia:
• prawa konta standardowego
• tworzenie, zmiana i usuwanie kont użytkowników
• zmiany w konfiguracji komputera
• dostęp do wszystkich plików na komputerze
• instalacja sprzętu i oprogramowania

**Konto standardowe** -- do codzinnego użytku, może korzystać z większości programów.

Uprawnienia:
• prawa, jakie posiada konto z ograniczeniami
• możliwość zmiany podstawowych ustawień komputera takich jak zmiana
ustawień wyświetlania oraz zarządzania energią

**Konto gościa** -- dla użytkownika bez stałego konta na komputerze. Goście nie mogą instalować oprogramowania ani sprzętu, nie mogą zmieniać ustawień ani tworzyć haseł. Konto gościa musi zostać włączone, aby można było z niego korzystać.

**Profil użytkownika** -- to zbiór ustawień środowiska pracy, do którego zaliczamy ustawienia pulpitu, menu Start, ustawienia aplikacji, folder Moje dokumenty oraz pliki cookies. 

**Rodzaje profili:**
- lokalny (znajduje się na komputerze)
- wędrujący czyli mobilny (przechowywane w sieciowym udziale -- udostępnionym folderze -- do którego użytkownik ma dostęp z każdego komputera pracującego w sieci)

## Grupy

**Grupa** – to zbiór użytkowników i komputerów, kontaktów i innych grup, którymi można zarządzać jako pojedynczą jednostką. Grupom można przepisywać prawa, i te prawa będzie miał każdy użytkownik grupy.

**Grupy w usługach domenowych AD** --  są obiektami katalogu znajdującymi się w obiektach kontenerowych domeny oraz jednostkach organizacyjnych. Usługi AD zapewniają zestaw domyślnych grup podczas instalacji systemu Windows Server. Zapewniają opcję tworzenia innych grup.


**Rodzaje wbudowanych grup użytkowników:**
1. Operatorzy kopii zapasowych - członkowie mogą tworzyć kopie zapasowe i przywracać foldery i pliki zapisane w tych kopiach. Mają dostęp do programu "kopia zapasowa".
2. Usługi pomocy - członkowie mają za zadanie współpracę Microsoftu i niektórych producentów komputerów z użytkownikami sprzętu i oprogramowania. Usługi są świadczone na platformie pomocy zdalnej, która jest dostępna jako element pomocy systemu Windows.
3. Operatorzy konfiguracji sieci - członkowie mają uprawnienia do konfiguracji sieci.
4. Użytkownicy zaawansowani - członkowie mają rozszerzone uprawnienia, mogą udostępniać foldery, zarządzać drukarkami i tworzyć konta lokalne.
5. Użytkownicy pulpitu zdalnego - członkowie mogą zdalnie logować się do systemu.
6. Replikator - członkowie  mogą replikować pliki w obrębie domeny, stacji roboczej i serwera.

**Typy grup:**
1. Dystrybucyjne – do tworzenia list dystrybucyjnych poczty e-mail. Można używać tylko z aplikacjami e-mail takimi jak Microsoft Exchange Server do wysyłania wiadomości e-mail do kolekcji użytkowników. Grupy dystrybucji nie obsługują zabezpieczeń, co oznacza, że nie można ich wymieniać na dyskretnych listach kontroli dostępu.
2. Zabezpieczeń –  można kontrolować dostęp do asobów udostępnionych dla użytkowników.
3. Grupa lokalna - członkowie  mogą mieć przypisane uprawnienia w dowolnej domenie w drzewie.
4. Grupa globalna - członkowie mogą mieć przypisane uprawnienia w dowolnej domenie w lesie.
5. Grupa uniwersalna - członkowie mogą mieć przypisane uprawnienia w dowolnej domenie w drzewie lub lesie.

Las -- zbiór domen (firma1.pl, firma2.pl), drzewo -- domena (firma.pl). Gałęzie -- 1.firma.pl, 2.firma.pl. 

Logowanie interakcyjne potwierdza tożsamość użytkownika na koncie domeny Active Directory lub komputerze lokalnym użytkownika. 

### Konta, logowanie

## Konta wg rodzajów logowania:

1. Lokakne -- loguje się do komputera. Każdy komputer z systemem Windows, który nie jest kontrolerem domeny, może przechowywać lokalne konta użytkowników, ale te konta mogą być używane tylko w celu uzyskania dostępu do tego lokalnego komputera.

2. Domenowe -- loguje się do sieci, uzyskuje dostep do zasobów w domenie i dowolnych zaufanych domen. Można się zalogować na konto lokalne, mimo tego że komputer jest dołączony do domeny. 

**Autoryzacja** -- przypisanie użytkownikowi uprawnień do operacji na zasobie (i sprawdzanie, czy użytkownik ma te uprawnienia). Zasoby: katalog, baza danych, uruchomienie aplikacji.

Autoryzacja użytkownika -- z punktu widzenia użytkownika. Z punktu widzenia chronionego obiektu nazywane jest kontrolą dostępu opartą na obiektach.

**Uwierzetylnienie** -- niewidoczne dla użytkowników z kontem domeny (profil jest tworzony i utrzymywany w domenie), dla konta lokalnego potrzebne są hasło i login.

### Prawa użytkownika

Przypisane do grup. 

**Rodzaje praw użytkownika:**

1. Przywilej -- prawo do tworzenia kopii zapasowych plików i katalogów.
2. Prawo logowania -- np do logowania się lokalnie.

Prawa -- stosuj się do  kont użytkowników, uprawnienia -- dołączone do obiektów.


"Deny" ma pierwszeństwo przed "Allow". Niektóre uprawnienia mogą przesłonić lub zignorować uprawnienia ustawione dla obiektu (np. ACL, czyli listy kontroli dostępu).


Na przykład użytkownik zalogowany do konta domeny jako członek grupy Operatorzy kopii zapasowych ma prawo do wykonywania operacji tworzenia kopii zapasowych dla wszystkich serwerów domeny. Wymaga to jednak możliwości odczytu wszystkich plików na tych serwerach, nawet plików, w których ich właściciele ustawili uprawnienia, które jawnie odmawiają dostępu wszystkim użytkownikom, w tym członkom grupy Operatorzy kopii zapasowych. Prawo użytkownika, w tym przypadku prawo do wykonywania kopii zapasowej, ma pierwszeństwo przed wszystkimi uprawnieniami do pliku i katalogu.

## Kontrola dostępu

**Kontrola dostępu** -- proces przydzielenia uprawnień do dostępu do obiektów AD.

Można przypisać dostępy do:
1. Grupy, użytkownicy i specjalne tożsamości w domenie;
2. Grupy i użytkownicy w tej domenie i dowolne zaufanie domeny;
3. Lokalne grupy i użytkownicy na komputerze, na którym znajduje się obiekt

**Deskryptor bezpieczeństwa** to specjalna struktura danych w systemie Windows, która określa, kto i w jaki sposób może uzyskać dostęp do obiektu (np. pliku, folderu, procesu, klucza rejestru, gniazda sieciowego itd.).


**Komponenty bezpieczeństwa deskryptora:**
1. Właściciel (zazwyczaj twórca obiektu)
2. Dyskretna lista dostępu (określa kto ma jakie uprawnienia)
3. Lista kontroli dostępu do systemu (służy nie do kontroli dostępu, lecz do audytu -- logowania prób dostępu)

### Uprawnienia

Każdy obiekt Active Directory ma właściciela.

**Sbosoby przenoszenia własności obiektu:**
1. Właściciel udziela uprawnienia "Przejmij własność"
2. Administrator przejmuje obiekt na własność "Przejmij prawo własności"

**Typy uprawnień wspólne dla wszystkich typów obiektów:**
1. Odczyt
2. Modyfikacja
3. Zmiana właściciela
4. Usuwanie


Uprawnienia mogą być jawne i dziedziczone.

**Rodzaje ziarnistosci:**
1. Uprawnienia typu obiektu – uprawnienia nadawane na podstawie typu/klasy obiektu, niezależnie od konkretnej instancji. Przykład: "czytanie dokumentów" - może czytać WSZYSTKIE dokumenty w systemie.
2. Uprawnienia na podstawie właściwości – uprawnienia nadawane na podstawie konkretnych atrybutów/właściwości obiektu, użytkownika lub kontekstu. Przykład: użytkownik może edytować tylko dokumenty, których jest autorem.

**Group Policy Objects (GPO)** -- "książka zasad" dla komputerów i użytkowników w sieci Windows. Tworzysz jeden zestaw reguł, który automatycznie zastosuje się do wszystkich wybranych urządzeń.

**Microsoft Management Console (MMC)** -- To główne narzędzie administracyjne - myśl o nim jak o "centrum dowodzenia" dla administratora. MMC to framework, do którego można dodawać różne "przystawki" (snap-ins).

**Rozszerzenia MMC:**
1. Szablony administracyjne –  regulują zachowanie i wygląd pulpitu, w tym składników systemu operacyjnego i aplikacji;
2. Ustawienia bezpieczeństwa 
3. Instalacja oprogramowania – aby centralnie zarządzać oprogramowaniem w organizacji.
4. Skrypty – za pomocą skryptów można zautomatyzować uruchamianie i zamykanie komputera oraz logowanie użytkownika i wylogowanie.


## 2. Budowa Active Directory

**Usługa katalogowa Active Directory (AD)** -- to usługa sieciowa identyfikująca wszystkie zasoby w sieci i udostępniająca informacje o nich użytkownikom oraz aplikacjom w systemach Windows Server.



## 3. Zastosowanie DNS

## 4. Usługi sieciowe

## 5. Zastosowanie IIS

## 6. Zastosowanie Hyper-V

## 7. Zastosowanie pamięci masowej

## 8. Bezpieczeństwo danych


