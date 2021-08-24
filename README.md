![logo optymizacja.pl](https://logo.optymizacja.pl/1/cover.png)
## [optymizacja](https://optymizacja.github.io/www/)
+ [logo optymizacja](https://optymizacja.github.io/logo/)
+ [docs optymizacja](https://optymizacja.github.io/docs/)


# Definicja - znaczenie optymizacji

## Optymizacja
[optymizacja – Słownik języka polskiego PWN](https://sjp.pwn.pl/sjp/optymizacja;2495887)

optymizacja «spowodowanie optymalnego przebiegu danego procesu technologicznego» 



## Optymalizacja
[Optymalizacja – Wikipedia, wolna encyklopedia](https://pl.wikipedia.org/wiki/Optymalizacja)

Metoda wyznaczania najlepszego (optymalnego) rozwiązania (poszukiwanie ekstremum funkcji) z punktu widzenia określonego kryterium (wskaźnika) jakości (np. kosztu, drogi, wydajności).
W programowaniu komputerowym optymalizacja oprogramowania oznacza działania mające na celu programu komputerowego, tak by czas jego działania oraz używane zasoby komputerowe takie jak pamięć, użycie procesora, ilość przesyłanych danych potrzebnych do jego uruchomienia i działania były jak najmniejsze. Działaniami w tym zakresie są optymalizacja kodu wynikowego, wybór wydajniejszych algorytmów i kodowania danych. 


# Wzory - wyznaczanie optymizacji

Jest to przykładowy sposób podejścia do porównania efektywności wykonania zadania przez różne osoby
Dzięki czemu można określić nie tylko trudność zdania, ale też potencjał do szybszego wykonania przez konkretną osobę.
 
To ważny fakt, a przecież każdy z nas się różni poprzez doświadczenie i efektywność (talent) wykonaywania specyficznych zadań.

Jest to uzupełnienie do Agile-owej techniki nazywanej Planning Poker [Jak estymować? cz. 2 - techniki estymacji - Agile Hunters](https://agilehunters.com/jak-estymowac-techniki-estymacji/)

Przy dużym stopniu automatyzacji metoda ta może być stosowana na podstawie już wykonanych iteracji i badać dane historyczne w systemie opartym o [GitOps](http://www.gitops.pl/)
gdzie jedna iteracja to jeden commit-push na serwer repozytorium i monitorowanie rezultatu testów w warunkach uruchamiania w chmurze a nie na lokalnym środowisku.

Wówczas łatwo porównać dane różnych członków zespołu i zbudować graficzną reprezentację silnych i słabych stron, specyficznej dla każdego i pozwalające w przyszłości przydzielać zadania, które będą bardziej intuicyjne dla konkretnej osoby, przez co czas i energia zużyta na wykonanie zadania będzie niższa.


## Efektywność wytwarzania*

*pojedynczej osoby w zespole

jest zależna od doświadczenia i doskonałości danej osoby w procesach iteracji
Specjalizacja procesu oraz niska Awaryjność systemu i prosota zadania(zmiany) wpływa na efektywność wykonania iteracji.

    Efektywność = Doświadczenie * Doskonałość * Specjalizacja * Awaryjność * Prostota

Wartość jest większa od 1, krotność jest wyznacznikiem ryzyka skali niepewności co do oczekiwanego rezultatu


## Doświadczenie osoby w kontekście 1 iteracji

Doświadczenie jest równe 1, gdy osoba miała możliwość uczestniczenia na każdym etapie w procesie wytwarzania w przeszłości

    Doświadczenie = ilość wykonywanych procesów* / ilość wszystkich procesów*
    
*w iteracji

## Doskonałość wykonania jednej czynności/procesu, 

Doskonałość jest równa 1 gdy osoba wykonuje proces bezbłednie, 
wartość jest tym mniejsza im mniej razy dane zadanie zostało wykonane poprawnie,
dotyczy np. iteracji wytwarzania funkcjonalności, gdzie po jej wprowadzeniu kod od razu działa poprawnie.
Gdy użyjemy lepszej technologii jakość wykonania pojedynczej próby może ulec zwiększeniu co pozwalając zwiększyć doskonałość

    Doskonałość = ilość udanych prób / ilość prób


## Specjalizacja procesu (nie człowieka)
Specjalizacja (Efektywność iteracji) udowadnia, że lepiej mieć więcej procesów, ale powtarzalnych niż mniej ale definiowalnych
pozwala też określić na ile wystepuje potrzeba modularyzacji procesów wytwarzania, ich podziału na bardziej wyspecjalizowane 

    Specjalizacja = stałe procesy / zmienne procesy
    
+ stałe procesy = ilość powtarzalnych procesów*

+ zmienne procesy = ilość zależnych/niezdefiniowanych/zmiennych procesów*   


*ilość procesów składających się na 1 iterację


## Awaryjność środowiska systemu
Prawdopodobieństwo / zdolność do awarii wynikająca z ilości zmiennych poza samym procesem

    Awaryjność 
    = ilość kontrolowanych warstw / ilość warstw  w ogóle (mających wpływ na rezultat)

## Prostota
Prostota wykonania jest 1, gdy jest najprościej lub część ułamka gdy wzrasta poziom trudności

    Prostota 
    = (ilość już wykonanych dokładnie takich samych funkcjonalnie zadań / ilości różnic ) 
                / ilość warstw(zależnych miejsc), które te różnice dotyczą 


# Obliczenia Efektywność wytwarzania na przykładach
    
    Efektywność = Doświadczenie * Doskonałość * Specjalizacja * Awaryjność * Prostota



## W procesie wytwarzania oprogramowania opartego o framework laravel są 3 warstwy dotyczące funkcjonowania oprogramowania oraz 3 warstwy dotyczące uruchomienia

### Warstwy oprogramowania:

+ Frontend
    +   Biblioteki zewnętrzne
+ Backend
    +   framework, warstwa struktury
    +   warstwa kodu, język programowania
    +   warstwa danych, bazy danych
    +   Biblioteki zewnętrzne

+ Environment
    +   system
    +   usługi   
        +   http apache
        +   mysql baza danych


### Sposób wytwarzania:
+ specyfikacja
    + przykladowe dane wejsciowe    
+ pisanie


### Zadanie nr 1
wdrożenie zmiany, która wcześniej nie miała miejsca

#### 1 osoba:

+ Doświadczenie = 1
bo to autor, który już wykonywał prototyp

+ Doskonałość = 0.2
gdyż to faza wytwarzania i potrzeba przetstować różne warianty

+ Specjalizacja = 0.2
Wiele etapów wytwarzania jest niezdefiniowanych z powodu wielu warstw środowiska

+ Awaryjność = 3/5 = 0.6
Biblioteki zewnętrzne oraz srodowisko

+ Prostota = 0,13
(2/5) /3 

#### Efektywność = Doświadczenie * Doskonałość * Specjalizacja * Awaryjność * Prostota

Efektywność = 1*0.2*0.2*0.6*0.13

1*0,2*0,2*0,6*0,13=0,0031

1/0,0031=322

To oznacza, że wykonując idealną iterację w ciągu 1 Minuty,
iteracja wykonywana w zmiennych i trudnych warunkach może zająć 322 razy dłużej,

gdyby było mniej warstw środowiska mająych wpływ na wynik i tego typu zmiany byłyby już wcześniej wykonywane to można by było obniżyć ryzyko o 26 razy

+ Doskonałość = 1
+ Specjalizacja = 1

0,6*0,13=0,078

1/0,078=12

322/12=26

### Zadanie nr 2
wdrożenie zmiany, która była już wprowadzana, np zmiany nazwy zmiennej/klasy/stałej prywatnej w jednym pliku

#### 1 osoba:

+ Doświadczenie = 1
bo to autor, który już wykonywał prototyp

+ Doskonałość = 1
Gdyż osoba ta wykonywała to wielokrotnie bez błędu

+ Specjalizacja = 1
Jedna warstwa

+ Awaryjność = 1/1
Bo zmiana dotyczy zmiennej, która nie występuje w innych plikach, to zmienna prywatna klasy

+ Prostota = 1/1/1 = 1


#### Efektywność = Doświadczenie * Doskonałość * Specjalizacja * Awaryjność * Prostota

Efektywność = 1
to znaczy, że dokonując tej zmiany, nie ma szansy nic się zepsuć, gdyż to nie wpływa na inne warstwy systemu
Zadanie jest jasno sprecyzowane, nie ma żadnych zależności, dlatego jeśli cykl wykonania normalnie zajmuje 1 Minutę, to 
nie wystąpi żadno ryzyko/błąd mogący zwielokrotnić ilość iteracji

