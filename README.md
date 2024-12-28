# CDV-Big-Data-projekt-zaliczeniowy

Wymagania projektu

Big Data, projekt zaliczeniowy

Celem projektu zaliczeniowego jest stworzenie niewielkiego systemu analitycznego. System musi się składać z:

warstwy wczytującej dane początkowe, czyli na przykład:
wczytywanie plików płaskich

wczytywanie plików json

wczytywanie plików kolumnowych

strumienia danych

parsowania danych z dokumentów pdf

itp.

warstwy przekształceń danych 
baza sql bądź nosql

jezioro danych

lub inne rozwiązanie

warstwy wynikowej 
hurtownia danych z kwerendami wynikowymi, eksport danych do tabel stałych, tabel przestawnych, narzędzi BI
Mile widziane rozszerzenie projektu w postaci zastosowania metod uczenia maszynowego. 
Studenci samodzielnie łączą się w zespoły trzy-cztero osobowe, wybierają lidera i proponują temat pracy. Lider zgłasza to do prowadzącego w celu akceptacji (mailowo) do 31 października. Lider jest odpowiedzialny za komunikację z prowadzącym. Termin oddania projektu 12 stycznia.

Przykładowe pomysły:

Zescrapowanie kilkuset filmów z witryny imdb, zebranie o nich kilkudziesięciu informacji (20 - 30 atrybutów) do bazy danych, zbudowanie kwerend do warstwy wynikowej dla użytkownika końcowego, ewentualnie dodanie narzędzia typu BI tool do analizy wyników końcowych

Napisanie api / skryptu / programu do pobrania informacji ze strony NBP (http://api.nbp.pl/api/) dotyczących kursu walut i / lub złota. Dane załadować do bazy / hurtowni (np. BigQuery) i stworzyć dla użytkownika końcowego wygodne narzędzia do analizy danych. 

Pobranie danych pomiarowo obserwacyjnych IMGW (jakieś tysiąc plików) i połączenie ich w jedną bazę / hurtownie danych. Stworzyć wygodne dla użytkownika końcowego rozwiązania do analizy danych. 

Kryteria oceny projektu:

terminowość tj. projekt zostaje dostarczony nie później niż w wyznaczonym czasie (12 stycznia)

przekrojowość tj.:

dane wynikowe są obszerne, posiadają wymiary nadające się do sensownej analizy, odpowiadają na potrzeby użytkownika, cechy zostają odpowiednio przekształcone (np. wieku w kategoriach, powierzchnia w klasach wielkości)

prawidłowość tj.:
projekt pozbawiony jest błędów technicznych (np. brak błędów we wczytywaniu danych, prawidłowe formaty, itp.), wyniki analityczne są pozbawione błędów obliczeniowych, wyników końcowe zostały sprawdzone przez uczestników

niezawodność tj.: 
kod działa zgodnie z intencją programisty bez ingerencji użytkownika

czystość tj.: 
kod nie generuje błędów

kod nie generuje ostrzeżeń (jeżeli to tylko możliwe)

kod nie zawiera zbędnych elementów

dokumentacja tj.:
spisane na początku istniejące założenia dot. projektu

(np. jakie dane, po co, jaki problem rozwiązuje, itp.)

ważniejsze części / sekcje kodu są wyodrębnione komentarzami

komentarze pojawiają się w miejscach wymagających wyjaśnień

poziom kodu: 
najważniejszy jest działający kod 

mile widziane jest użycie elementów jak: 

własne funkcje, instrukcje warunkowe

pętle

wizualizacje danych 

pomocnicze pliki skryptu (np. ładujące etykiety)

itp.

Czego oczekuję po formie projekcie:

mile widziane BiGQuery, ale jestem otwarty na różne środowiska i narzędzia

Projekt wszystkie niezbędne pliki, linki, itp.

pliki źródłowe, 

pliki skryptu, 

pliki pomocnicze,

pliki wynikowe

Brak "śmieci" tj. zbędnych plików lub innych obiektów
