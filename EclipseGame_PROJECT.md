# EclipseGame --- dokument główny projektu

## Cel projektu

Tekstowe MMORPG science fiction. Gra koncentruje się na fabule, świecie,
opisach postaci, broni i budynków, misjach, rozwoju bazy, zarządzaniu
armią oraz decyzjach strategicznych. Nie ma sterowania ruchem postaci
klawiaturą ani eksploracji przez chodzenie po mapie.

## Publikacja i kod

-   Repozytorium GitHub: `EclipseGame`
-   Właściciel/konto GitHub: `wadiamo`
-   Opublikowana strona: https://wadiamo.github.io/EclipseGame/
-   Obecna wersja to wczesny prototyp ekranu wyboru rasy i klasy.
-   GitHub Pages służy do publikacji interfejsu; prawdziwe funkcje MMO
    (wspólny świat, konta, trwałe zapisy, serwerowy czas działań i
    walki) będą wymagały backendu.

## Ustalona koncepcja rozgrywki

### Rasy i klasy

-   Rasy: Ludzie i Obcy.
-   Klasy: Kreator, Wojownik, Łowca.
-   Każda rasa ma dostęp do trzech klas.

### Bohater i armia

-   Bohater oraz armia mają niezależne kolejki działań.
-   Bohater może wykonywać tylko jedną aktywność naraz: misję, walkę
    osobistą, trening, eksplorację itp.
-   Armia może w tym samym czasie prowadzić operację wojskową, bronić
    bazy, eskortować, zbierać zasoby itp.
-   Gdy bohater dołącza do armii, nie wykonuje równolegle osobnej misji.
    Jego klasa, poziom, umiejętności i wyposażenie dają armii bonusy.
-   Bohater ma wzmacniać armię, ale nie gwarantować zwycięstwa.
-   Premie dowódcze muszą mieć limity i nie mogą bez końca mnożyć się ze
    sobą.

### Walka

-   Wybrany model: automatyczne starcia na podstawie siły, wyposażenia,
    składu jednostek, taktyki, dowódcy, warunków/terenu i zdarzeń.
-   Gracz przygotowuje armię i wybiera cel/taktykę; po walce dostaje
    raport z wynikiem, stratami, nagrodami i doświadczeniem.
-   Balans należy testować symulacjami wielu walk.
-   Jednostki, morale, rozpoznanie, obrona, szybkość, technologia i
    koszty strat mają znaczenie.

### Zasoby

-   Ogień: energia, przemysł, broń i amunicja.
-   Powietrze: rozpoznanie, komunikacja, sensory i systemy
    podtrzymywania życia.
-   Woda: życie kolonii, leczenie, regeneracja i rozwój populacji.
-   Ziemia: zasób unikalny, rzadki, odkrywany w specjalnych
    misjach/ruinach/wydarzeniach. Nie jest zwykłym surowcem produkowanym
    bez ograniczeń.

### Misje

-   Gracz wybiera misje z menu; nie steruje postacią w świecie.
-   Misje różnią się trudnością, czasem trwania, wymaganiami, ryzykiem,
    nagrodami i wydarzeniami fabularnymi.
-   Misje mają być historiami i decyzjami, nie tylko timerami.
-   Bohater może być na misji w tym samym czasie, gdy armia prowadzi
    osobną operację.

### Budynki, jednostki i szkolenie

-   Gra ma budynki wojskowe, cywilne, umocnienia, rekrutację jednostek,
    szkolenie wojsk, trening bohatera, badania/technologie i misje.
-   Każdy obiekt powinien być opisany w centralnej matrycy danych:
    nazwa, kategoria, opis fabularny, funkcja, poziomy, wymagania,
    koszty zasobów, czas, efekty/produkcja, limity i odblokowania.
-   Matryca ma być źródłem danych wykorzystywanym przez grę, a nie tylko
    opisowym dokumentem.

## Tempo rozgrywki i czasy

-   Początek gry ma być szybki: wiele pierwszych działań trwa około 1
    minuty.
-   W miarę rozwoju rosną czasy, koszty i wymagania, ale również
    korzyści.
-   Przykład podany przez użytkownika dla koszar:
    -   Poziom 1: 2 minuty budowy, wydajność produkcji 1×.
    -   Poziom 2: 4 minuty budowy, wydajność produkcji 1,5×.
    -   Poziom 3: 10 minut budowy, wydajność produkcji 4×.
-   To wartości przykładowe do dalszego balansu, nie zatwierdzona pełna
    ekonomia.
-   Wydajność produkcji i siła pojedynczej jednostki to odrębne
    parametry.
-   Trening wyższego poziomu trwa dłużej, kosztuje więcej i daje większą
    premię.
-   Czas działania powinien postępować także po zamknięciu przeglądarki;
    w docelowym MMO stan i czas działań kontroluje serwer.

## Główne zasady balansu

1.  Armia bez bohatera pozostaje użyteczna.
2.  Bohater daje przewagę, ale nie zapewnia automatycznej wygranej.
3.  Różne klasy i składy armii mają różne zastosowania.
4.  Koszty, czas, straty, leczenie i odbudowa muszą tworzyć istotne
    decyzje.
5.  Rosnące poziomy wymagają coraz większych inwestycji, ale nie mogą
    tworzyć niekontrolowanej eksplozji mocy.
6.  Gracz nie powinien być karany katastrofalnie za odejście od gry na
    sen lub pracę.
7.  Balans liczb ma być testowany symulacjami, a nie ustalany wyłącznie
    intuicyjnie.

## Plan matrycy

1.  Ekonomia i źródła zasobów.
2.  Budynki wojskowe.
3.  Budynki cywilne.
4.  Umocnienia.
5.  Jednostki wojskowe i rekrutacja.
6.  Szkolenie jednostek.
7.  Rozwój bohatera, klasy i umiejętności.
8.  Misje i ich nagrody.
9.  Badania i technologie.
10. Artefakty i Ziemia.
11. Automatyczne walki, straty i raporty.
12. Symulacje balansu.

## Najbliższe kroki

1.  Założyć projekt ChatGPT o nazwie `EclipseGame` i przenieść do niego
    tę rozmowę, jeśli interfejs daje taką możliwość.
2.  Zachować ten dokument w repozytorium jako `PROJECT.md` lub
    `docs/PROJECT.md`.
3.  Zaprojektować centralną matrycę danych, zaczynając od zasobów i
    podstawowych budynków.
4.  Zdecydować, które elementy należą do pierwszego grywalnego
    prototypu, a które wymagają backendu.
5.  Rozwijać istniejącą stronę GitHub Pages, nie tworząc nowego
    repozytorium bez potrzeby.

## Ważne rozróżnienie

Rzeczy opisane jako „ustalone" są kierunkiem projektowym. Konkretne
koszty, nagrody, premie, czasy poza przykładem koszar i dokładne
wartości bojowe nadal wymagają zaprojektowania i testów.
