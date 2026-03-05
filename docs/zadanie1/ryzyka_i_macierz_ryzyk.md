| # | Zadanie | Ryzyko | Prawdopodobieństwo | Wpływ | Łagodzenie |
|---|------------|--------|--------------------|-------|------------|
| R1 | Zadanie 6 | Problemy z rozpoznawaniem kart Borderless i Showcase oraz Foil | Wysokie | Duży | Dodatkowe kroki preprocessu obrazów przed wykrywaniem tekstu |
| R2 | Zadanie 2 |Limity i opóźnienia zapytań API Scryfall | Niskie | Średni | Cashe'owanie albo pobieranie całej bazy kart lokalnie i pilnowanie opóźnień zalecanych przez Scryfall | 
| R3 | Zadanie 6 |Błędne rozpoznanie edycji karty (ten sam art w różnych setach) | Bardzo wysokie | Niski | Użytkownik będzie mógł wybrać z listy setów jeśli uzna to za przydatne |
| R4 | Zadanie 7  |Znaczny spadek dokładności rozpoznawania kart przy słabych warunkach oświetlenia | Średnie | Duży | Dodanie dokładnych instrukcji co do optymalnych warunków  i ostrzeżenie użytkowników o potencjalnych niedokładnościach |
| R5 | Zadanie 7 |Problemy z synchronizacją między aplikacją mobilną, a web UI | Średnie | Duży | Wykorzystanie serializacji operacji i ustalenie zasad rozwiązywania konfliktów |
| R6 | Zadanie 6 |Scope Creep | Niskie | Średni | Zasada każdy dodatkowy nowy feature można zacząć pisać po skończeniu 2 poprzednich |


Macierz ryzyk:

| Prawdopodobieństwo \ Skutek | 1 - Niski | 2 - Mały | 3 - Średni | 4 - Duży | 5 - Krytyczny |
|---|---|---|---|---|---|
| 5 - Bardzo wysokie | 🟧 R3 | 🟥 | 🟥 | 🟥 | 🟥 |
| 4 - Wysokie        | 🟧 | 🟧 | 🟥 | 🟥 R1 | 🟥 |
| 3 - Średnie        | 🟨 | 🟧 | 🟧 | 🟥 R4, R5 | 🟥 |
| 2 - Niskie         | 🟩 | 🟨 | 🟧 R2, R6 | 🟧 | 🟥 |
| 1 - Bardzo niskie  | 🟩 | 🟩 | 🟨 | 🟧 | 🟧 |


