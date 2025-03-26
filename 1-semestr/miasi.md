# Modelowanie i analiza systemów informatycznych 

## Pojęcia podstawowe
- **Klasa** -- abstrakcyjny opis zbioru objektów o podobnych właściwościach i zachowaniach. Klasa definiuje szablon lub wzór, na podstawie którego tworzone są obiekty.
- **Obiekt** -- konkretny byt, instancja  klasy. Obiekty posiadają atrybuty (cechy statyczne) oraz operacje (określające zachowanie). Obiekty w systemie informatycznym przechodzą przez różne stany podczas swojego cyklu życia.
- **Model** -- pewna abstrakcja projektowanego systemu, widziana z określonej perspektywy, na określonym poziomie szczegółowości.
- **Interakcja** -- sposób, w jaki objekty komunikują się ze sobą w systemie. Interakcje są przedstawiane na diagramach interakcji, takich jak diagramy sekwencji, diagramy komunikacji i diagramy sterowania interakcją. Interakcje mogą być współbieżne, warunkowe oraz iteracyjne.
- **Stereotyp** -- mechanizm rozszerzalności w UML, modyfikuje znaczenie elementów UML, dodając im nową semantykę.
- **Metka** -- mechanizm w UML, który pozwala dodawać niestandardowe właściwości do elementów modelu.
- **Profil** -- podzbior języka UML, dostosowuje UML do konkretnych dziedzin, grupując stereotypy i metki.
- **Diagram** -- środek służący do opisu modelu.
- **Pakiet** -- mechanizm ogólnego zastosowania, służący do organizowania elementów w grupy. Pakiety pozwalają na grupowanie logicznie powiązanych elementów modelu.

## Cykl życia oprogramowania
- Rozpoczęcie (Inception):  jest początkiem projektu, gdzie głównym celem jest zrozumienie celów i zakresu projektu.
- Opracowanie (Elaboration): celem tej fazy jest szczegółowe zrozumienie wymagań oraz zaplanowanie architektury systemu.
- Budowa (Construction): implementacja systemu, czyli pisanie kodu na podstawie wcześniej opracowanych projektów.
- Przekazanie (Transition): wdrożenie oprogramowania do środowiska użytkownika, szkolenie użytkowników oraz akceptację systemu. W tej fazie następuje ostateczne testowanie i poprawki.

## Diagramy Modelowania UML
### I. Strukturalne diagramy UML (opisują statyczne aspekty systemu)

### Klas

Służą do przedstawienia statycznej struktury systemu informatycznego. Diagramy te pokazują klasy, ich atrybuty, operacje oraz związki między nimi.

**Związki między klasami:**
- **Asocjacja** jest ogólnym powiązaniem między dwiema lub więcej klasami, opisującym relacje pomiędzy ich instancjami. Dwukierunkowe, jednokierunkowe.
- **Agregacja** to szczególny rodzaj asocjacji, który reprezentuje relację "ma-a" (ang. "has-a") lub "składa się z" (ang. "part of"), gdzie jedna klasa jest częścią innej. Agregacja częściowa, całkowita (kompozycja).
- **Uogólnienie** tworzy hierarchię dziedziczenia między klasami, gdzie podklasa (ang. subclass) dziedziczy atrybuty i operacje nadklasy.
- **Zależność** oznacza, że jedna klasa (niezależna) używa lub zależy od innej klasy (zależnej). 
- **Realizacja** to związek między interfejsem a klasą, gdzie klasa implementuje operacje zdefiniowane w interfejsie.

**Typy klas:**
- Klasy abstrakcyjne (ang. abstract classes): Klasy, które nie mogą mieć konkretnych instancji, stanowią uogólnienie obiektów konkretnych znajdujących się na niższych poziomach hierarchii.
- Klasy konkretne (ang. concrete classes): Klasy, które mogą mieć instancje obiektów
- Klasa asocjacyjna (ang. association class): Klasa, która reprezentuje asocjację między dwoma klasami, zawierająca dodatkowe atrybuty i operacje związane z tym związkiem. Służy do bardziej precyzyjnego opisu relacji między klasami.

Związki między klasami mogą być wielokrotne (kilka asocjacji między tymi samymi klasami) lub zwrotne (klasa połączona z samą sobą).

### Obiektów
Są to wystąpienia diagramów klas, pokazujące konkretne obiekty w systemie i ich powiązania. Odwzorowują strukturę systemu w wybranym momencie jego działania.

### Pakietów
Pokazują organizację elementów modelu w logiczne grupy (pakiety), pomagając zarządzać złożonymi systemami. Mogą być zagnieżdżane, opisywane dodatkowo przy pomocy stereotypów.

**Elementy:**
- Pakiety: Reprezentowane jako prostokąty z zakładką, zawierają elementy modelu.
- Zależności:  Przedstawiane za pomocą strzałek, pokazują, jak pakiety są ze sobą powiązane. Zależności mogą oznaczać, że jeden pakiet używa lub zależy od elementów w innym pakiecie.

### Komponentów
Przedstawiają logiczne elementy systemu zwane komponentami, ich interfejsy oraz zależności między nimi. Koncentrują się na architekturze oprogramowania, opisując interfejsy (usługi) dostarczane i wymagane przez poszczególne komponenty.

### Wdrożenia
Ilustrują fizyczną architekturę systemu, czyli rozmieszczenie infrastruktury sprzętowej oraz platform użytkowania. Diagramy wdrożenia często wykorzystują stereotypy i metki, aby opisać dodatkowe właściwości węzłów.

**Elementy:**
- Węzły (nodes) -- fizyczne lub wirtualne elementy infrastruktury.
- Artefakty -- izyczne manifestacje komponentów oprogramowania, takie jak pliki wykonywalne (.exe, .jar), pliki konfiguracyjne, bazy danych czy pliki bibliotek.
- Połączenia -- zależności i komunikację między węzłami.

### II. Behawioralne (dynamiczne) diagramy UML (opisują zachowanie i interakcje systemu)
### Przypadków użycia

Definiują funkcjonalność systemu z punktu widzenia użytkownika, opisując interakcje między aktorami (użytkownikami) a systemem.

### Czynności (aktywności)
Służą do modelowania dynamiki systemu, przedstawiając sekwencyjne i równoległe przepływy sterowania oraz danych między czynnościami, akcjami i obiektami.
Diagramy te mogą być wykorzystywane do modelowania procesów biznesowych, systemów, scenariuszy przypadków użycia, operacji i algorytmów.
**Elementy:**
- Przepływy sterowania
- Decyzje
- Rozwidlenia i scalenia
- Przepływ danych

### Maszyny stanowej
Przedstawiają dyskretne, skokowe zachowanie obiektów poprzez zbiór stanów i przejść między nimi. Wykorzystywane są do modelowania systemów czasu rzeczywistego i multimedialnych. 
**Elementy:**
- Stany
- Przejścia
- Stan początkowy
- Stan końcowy

### Sekwencji
Są to diagramy interakcji, które przedstawiają sekwencję komunikatów wymienianych między instancjami klasyfikatorów systemu. Ilustrują przepływ sterowania w systemie oraz kolejność wykonywania operacji.

**Rodzaje:** 
- Konceptualne
- Implementacyjne 
- Wystąpieniowe

**Elementy:**
- Klasyfikator
- Komunikat
- Linia życia
- Ośrodek sterowania

**Bramki** 
Są punktami przejścia komunikatów. Mogą być nazywane bezpośrednio (nazwa zbieżna z nazwą komunikatu który przez nią przechodzi, symbol) lub pośrednio (dodanie komunikatu). Typy: formalne, właściwe, wyrażeniowe.
- Formalne bramki: dotyczą całego diagramu.
- Właściwe bramki: dotyczą operandów interakcji w ramach fragmentów wyodrębnionych, pozwalają na szczegółowe modelowanie przepływu komunikatów wewnątrz złożonych struktur interakcji, jakimi są fragmenty wyodrębnione. Umożliwiają one precyzyjne zdefiniowanie, jak dane fragmenty interakcji reagują w różnych scenariuszach.

**Przykłady użycia bramek właściwych**
- Operator alt (alternatywa): We fragmencie wyodrębnionym z operatorem alt może istnieć wiele operandów, ale tylko jeden z nich jest realizowany w zależności od warunku. Bramy wyrażeniowe będą tu wskazywać, który operand jest aktywny i jakie komunikaty są przez niego przesyłane.
- Operator opt (opcja): W przypadku operatora opt dany operand jest wykonywany opcjonalnie, a brama wyrażeniowa będzie wskazywać czy i kiedy ten operand jest realizowany.
- Operator loop (iteracja): Fragment oznaczony operatorem loop wykonuje operandy wielokrotnie.  Bramy wyrażeniowe mogą śledzić które komunikaty są wysyłane w każdej iteracji.
- Operator break (przerwanie): We fragmencie z operatorem break, brama wyrażeniowa wskaże, że przerwanie zostało zainicjowane i dalsze komunikaty w danym fragmencie nie zostaną przesłane.

### Komunikacji 
Te diagramy, podobnie jak diagramy sekwencji, pokazują interakcje między obiektami, ale kładą nacisk na strukturalne relacje między obiektami a nie na czasową sekwencję, co jest głównym celem diagramów sekwencji. Obiekty są przedstawione jako węzły połączone liniami, a strzałki na liniach wskazują przepływ komunikatów.

**Elementy:**
- Obiekty (Instancje Klasyfikatorów): Reprezentują konkretne obiekty biorące udział w interakcji.
- Komunikaty:  Są to przesyłane informacje między obiektami. Komunikaty są opatrzone numeracją, która wskazuje na kolejność ich wymiany.
- Powiązania (Asocjacje):  Linie między obiektami, które pokazują relacje i możliwość komunikacji między nimi.
- Numery sekwencyjne:  Oznaczenia, które pokazują, w jakiej kolejności przesyłane są komunikaty.

### Harmonogramowania
Rodzaj diagramu interakcji, reprezentujący na osi czasu zmiany dopuszczalnych stanów jakie może przyjmować instancja klasyfikatora uczestnicząca w interakcji. Diagramy te koncentrują się na czasie trwania interakcji i zmianach stanów obiektów w czasie

**Elementy:**
- Linia życia (Lifeline): Przedstawia obiekty lub komponenty, których stany są analizowane w czasie
- Oś czasu:  Oś pozioma, która reprezentuje upływ czasu.
- Stany:  Przedstawiane jako poziome pasy lub prostokąty, reprezentują stan, w jakim znajduje się obiekt w danym czasie
- Przejścia:  Pokazują momenty, w których obiekt zmienia stan.
- Ograniczenia czasowe:  Dodatkowe elementy, które mogą precyzować minimalny lub maksymalny czas trwania stanu lub przejścia.

### Opisu interakcji
Przedstawiają połączone interakcje jako czynności.

### II. Diagramy modelowania analitycznego
Diagramy te służą do analizy wymagań i projektowania struktury systemu informatycznego.

### Diagramy Klas Analitycznych
Przedstawiają klasy graniczne, sterujące i przechowujące, które są wykorzystywane do modelowania funkcjonalności systemu. Służą do przejścia z poziomu opisu wymagań (np. przypadków użycia) na poziom bardziej szczegółowy.Łączą diagramy przypadków użycia z bardziej szczegółowymi modelami systemu, takimi jak diagramy klas (modelowanie statyczne) i diagramy interakcji (modelowanie dynamiczne). Ich celem jest analiza wymagań, aby określić, jakie elementy systemu muszą zostać zaimplementowane.

- Aktorzy -- użytkownicy lub zewnętrzne systemy, które wchodzą w interakcję z modelowanym systemem.
- Związki -- reprezentują relacje pomiędzy klasami analitycznymi i aktorami.

  **Klasy w modelowaniu analitycznym:**
- Klasa graniczna (ang. boundary class):  Klasa, która reprezentuje interakcję aktora z systemem, w tym interfejsy użytkownika, raporty, strony internetowe, protokoły komunikacyjne i inne interfejsy. Może być interfejsem dla użytkownika, systemu, lub urządzenia. 
- Klasa sterująca (ang. control class): Klasa reprezentująca logikę aplikacji i procesy, które koordynują interakcje między różnymi klasami. Pośredniczy między klasami granicznymi, przechowującymi i innymi klasami sterującymi. Obiekty tych klas często istnieją tylko podczas wykonywania przypadku użycia.
- Klasa przechowująca (ang. entity class): Klasa reprezentująca dane, które muszą być przechowywane przez dłuższy czas (np. tabele w bazach danych, pliki). Nie może samodzielnie inicjować interakcji.

### III. Diagramy Modelowania Biznesowego
Diagramy te służą do modelowania procesów biznesowych organizacji.

### Biznesowe Diagramy Przypadków Użycia
Przedstawiają procesy biznesowe z punktu widzenia aktorów biznesowych, pokazując wartość dostarczaną przez organizację.
### Biznesowe Diagramy Klas
Prezentują klasy biznesowe, ich atrybuty oraz relacje, odzwierciedlając strukturę informacji w organizacji.
### Biznesowe Diagramy Czynności
Modelują przepływ pracy i czynności biznesowe w organizacji.
### Biznesowe Diagramy Sekwencji
Opisują interakcje między aktorami biznesowymi w czasie, pokazując kolejność działań.
### Biznesowe Diagramy Pakietów
Pokazują strukturę organizacyjną firmy i podział na jednostki biznesowe.

### IV. Diagramy Sterowania Interakcją
Dokumentują przepływ sterowania między logicznie powiązanymi fragmentami interakcji, np. diagramami sekwencji i komunikacji, z wykorzystaniem elementów diagramów czynności. Umożliwiają powiązanie diagramów interakcji w logiczny ciąg.

**Elementy:**
- Przepływy sterowania: wskazuje kierunek przepływu kontroli między fragmentami interakcji.
- Początek
- Koniec
- Fragmenty interakcji: odwołuje się do diagramu sekwencji (sd), komunikacji (cd) lub harmonogramowania (td), opisanych w danym fragmencie interakcji. W nagłówku diagramu sterowania interakcją wyróżnik jest wymagany, a nazwa fragmentu jest opcjonalna.
- Przywoływanie wystąpienia interakcji: jest odwołaniem do diagramu interakcji (ref) oznaczonego nazwą.

Diagram sterowania interakcją jest prezentowany w formie obramowanej, z wyróżnikiem diagramu (id), jego nazwą oraz listą instancji klasyfikatorów, które biorą udział w interakcji.

**Sposoby oznaczania fragmentów interakcji:**
- Jako przywoływane wystąpienia interakcji (ref), które odsyłają do innych diagramów interakcji. Stosuje się je zwłaszcza w przypadku złożonych diagramów, jak implementacyjne diagramy sekwencji.
- Poprzez wyróżniki diagramów interakcji (sd, cd, td), gdy diagram sterowania interakcją przedstawia niezbyt złożone diagramy składowe.

**Może składać się z:**
- Diagramów sekwencji
- Diagramów komunikacji
- Diagramów harmonogramowania

## CASE
Narzędzia CASE (Computer-Aided Software Engineering) to zintegrowane środowiska wspomagające proces tworzenia oprogramowania.

- Edytor Diagramów UML: Jest to podstawowy składnik, który umożliwia tworzenie i modyfikację diagramów UML.
- Moduł Kontroli Poprawności: Do wykrywania na bieżąco błędów podczas edycji diagramów i słownika danych.
- Moduł Kontroli Jakości: Do automatycznej oceny miar projektu.
- Moduł Zarządzania Pracą Grupowa: Do zabezpieczenia fragmentów projektu przed przypadkową zmianą. Do dodawania i usuwania kont użytkowników.
- Repozytorium Metadanych: Centralne miejsce przechowywania wszystkich informacji o projekcie.
- Moduł Generowania Kodu: Na podstawie utworzonych modeli UML, ten moduł jest w stanie automatycznie generować kod źródłowy w różnych językach programowania. 
- Moduł Modelowania Analitycznego: Ten moduł umożliwia specyfikację wymagań systemu na podstawie przypadków użycia.
- Moduł Modelowania Procesów Biznesowych: : Umożliwia modelowanie i dokumentowanie procesów biznesowych organizacji. Pomaga w zrozumieniu, w jaki sposób funkcjonuje organizacja i jakie są jej cele. 
Moduł Testowania i Weryfikacji: Wspomaga tworzenie testów, zarządzanie procesem testowania i analizę wyników testów.
