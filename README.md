[NET4.md](https://github.com/user-attachments/files/28324499/NET4.md)
# Platformy programistyczne .NET i Java
# Sprawozdanie 4 - Wiktor Hebdowski

## Wstęp

Repozytorium zawiera program będący modyfikacją przykładowej aplikacji webowej Blazor, dostępnej w Visual Studio. Zmodyfikowano podstronę wyświetlającą losowo wygenerowane dane pogodowe oraz dodano nową podstronę z zaimplementowanym uczeniem maszynowym oceniającym nastrój na podstawie wpisanego tekstu.
## Pogoda (Weather.razor)
Rozszerzono rozpiętość danych pogodowych do 10 rekordów co osiągnięto poprzez modyfikację zakresu zmiennej forecasts. Dodano także zliczanie dni z temperaturą powyżej 15 stopni, przycisk odfiltrowujący te dni ze zbioru wszystkich prognoz (i przywracający stan poprzedni) oraz możliwość filtrowania po wprowadzonej nazwie. Za odfiltrowanie wyników odpowiada funkcja filterLows(), zliczanie dni dodano do pierwotnej funkcji generującej rekordy, dodano także funkcję restoreOriginal() która przywraca oryginalny stan prognoz.
## Odczyt nastroju (Uczucie.razor)

Wykorzystano bibliotekę MLNET oraz zbiór z Kaggle do wytrenowania modelu z zakresu odczytywania nastroju użytkownika na podstawie jego wpisu. Następnie utworzono nową podstronę zawierającą pole tekstowe i przycisk po którego naciśnięciu zwracany jest szacowany nastrój oraz procent pewności z jaką model podjął decyzję. Ze względu na specyfikę zbioru uczącego, szacowanie nastroju działa poprawnie jedynie dla angielskiego tekstu.

## Wyniki
Poniżej zaprezentowano wygląd zmienionych podstron Weather i Uczucie
![enter image description here](https://i.imgur.com/ow3LOIR.png)
![enter image description here](https://i.imgur.com/2jKbVv9.png)
## Drzewo projektu

![enter image description here](https://i.imgur.com/ws54NM6.png)
