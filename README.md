Dokumentacja projektu analizy danych meteorologicznych i opadowych (IMGW 2000-2024)

Założenia projektu

1. Cel:
   Projekt ma na celu analizę danych meteorologicznych i opadowych z lat 2000-2024 w Polsce, szczególnie zaś:
   - Zrozumienie długoterminowych trendów klimatycznych, takich jak zmiany temperatur, opadów, i innych parametrów pogodowych.
   - Wykrywanie potencjalnych anomalii i odchyleń w danych pogodowych.
   - Stworzenie wizualizacji umożliwiających łatwą interpretację danych przez użytkowników końcowych.

2. 	Projekt umożliwia:
   - Agregację i łatwy dostęp do danych historycznych.
   - Zautomatyzowaną analizę dużych zbiorów danych.
   - Wizualizację, która wspiera podejmowanie decyzji na podstawie danych.

3. Zakres danych:  
   Dane meteorologiczne oraz opadowe zostały pozyskane z IMGW i obejmują lata 2000–2024. Dane zostały zebrane z różnych stacji pogodowych w Polsce.

4. Opis danych wejściowych

A. Dane meteorologiczne (2000–2024):
Zawierają podstawowe informacje o warunkach pogodowych zebrane codziennie.  
Pola w zestawie danych:
- **Kod stacji** (9 znaków) – identyfikator stacji pomiarowej.  
- **Nazwa stacji** (30 znaków) – pełna nazwa stacji pomiarowej.  
- **Rok** (4 znaki), **Miesiąc** (2 znaki), **Dzień** (2 znaki) – data pomiaru.  
- **Średnia dobowa temperatura [°C]** (5/1 znaków) – średnia temperatura w ciągu dnia.  
- **Status pomiaru TEMP** (1 znak) – status pomiaru temperatury (np. brak danych oznaczony jako "8").  
- **Średnia dobowa wilgotność względna [%]** (8/1 znaków) – średnia wartość wilgotności.  
- **Status pomiaru WLGS** (1 znak) – status pomiaru wilgotności.  
- **Średnia dobowa prędkość wiatru [m/s]** (6/1 znaków).  
- **Status pomiaru FWS** (1 znak).  
- **Średnie dobowe zachmurzenie ogólne [oktanty]** (6/1 znaków).  
- **Status pomiaru NOS** (1 znak).  

B. Dane opadowe (2000–2024):
Informacje dotyczące opadów deszczu oraz śniegu.  
Pola w zestawie danych:
- **Kod stacji** (9 znaków), **Nazwa stacji** (30 znaków), **Rok**, **Miesiąc**, **Dzień**.  
- **Suma dobowa opadów [mm]** (8/1 znaków) – łączna ilość opadów w ciągu dnia.  
- **Status pomiaru SMDB** (1 znak) – status pomiaru sumy dobowej opadów.  
- **Rodzaj opadu [S/W/ ]** (1 znak) – typ opadu (śnieg, woda lub brak danych).  
- **Wysokość pokrywy śnieżnej [cm]** (5 znaków).  
- **Status pomiaru PKSN** (1 znak).  
- **Wysokość świeżospałego śniegu [cm]** (5 znaków).  
- **Status pomiaru HSS** (1 znak).  
- **Gatunek śniegu [kod]** (1 znak).  
- **Rodzaj pokrywy śnieżnej [kod]** (5 znaków).  
- **Statusy**:  
  - "8" – brak pomiaru.  
  - "9" – brak zjawiska (również brak dnia w istniejącym miesiącu).  

---

5. Transformacja i przechowywanie danych

1. Jezioro danych (Data Lake):  
   Dane zostały zintegrowane i przechowywane w jeziorze danych utworzonym w środowisku Microsoft Fabric.  
   - Surowe dane z IMGW zostały załadowane w ich pierwotnym formacie.  
   - Dane zostały przekształcone do ujednoliconego formatu (ETL) i zapisane w strukturach ułatwiających dalsze analizy.

2. Magazyn Danych (Data Warehouse):  
   Zestawy danych zostały zorganizowane w relacyjnym magazynie danych:  
   - Tabele zostały podzielone na dane meteorologiczne i opadowe.  
   - Umożliwiono wydajny dostęp do danych dzięki optymalizacji indeksów i struktur.

---

6. Analiza i wizualizacja -  Dashboard w Power BI:  
   Stworzono interaktywny dashboard w Power BI, który umożliwia:
   - Przegląd danych historycznych w ujęciu rocznym, miesięcznym i dziennym oraz w podziale na stacje pogodowe.
   - Wyodrębniono dane dotyczące kwartałów tak by odseparować wpływ cykliczności pór roku
   - Analizę trendów długoterminowych, takich jak:
     - Średnie roczne temperatury.
     - Średnie ilości opadów deszczu i śniegu w miesiącach i latach.
   - Analizę innych parametrów pogodowych, takich jak wilgotność i prędkość wiatru.  
   - Użytkownik może filtrować dane według daty, typów opadów, czy lokalizacji stacji.  
