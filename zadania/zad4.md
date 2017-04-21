# Zadanie 4

Ostatnio stworzyliśmy działającą aplikację linkującą. Poszerzmy jej funkcjonalność!

1. Dodaj do modelu `Link` pole `redirect_count`, które będzie zliczać ilość przekierowań wykonanych dla danego linku. Ustaw jego domyślną wartość na `0` i zwiększaj przy każdym przekierowaniu. Wyświetl tę wartość w widoku `index`.

   Tip: wykorzystaj migrację - również do ustawienia domyślnej wartości początkowej
2. Dodaj możliwość usuwania raz stworzonego linka. W widoku `index` obok danych na temat linka umieść odnośnik do akcji usuwającej.
   
   Tip: spróbuj ustawić metodę zapytania wykonywanego przez link usuwający na `:delete`
3. Ulepsz walidację adresu docelowego `target` w modelu `Link` korzystając z modułu `URI`.
4. W przypadku błędu walidacji zamiast przekierowywać na `new` skorzystaj z `render` by "zachować" stan formularza użytkownika.

   Tip: przypisz tworzony obiekt do zmiennej instancyjnej, żeby był dostępny w widoku
4. (*) Wykorzystaj moduł `URI` by pozwolić użytkownikowi na wprowadzenie niepełnego adresu docelowego. Popraw go przed zapisaniem.

   Przykład poprawki: `google.com` -> `http://google.com`
5. (*) Korzystając z modułu `SecureRandom` wygeneruj użytkownikowi kilkoznakowy digest przy tworzeniu linka zamiast pozwalać mu wpisywać własny. Nie zapomnij zablokować inputu oraz zabezpieczyć parametrów.

   Tip: pomoże metoda `urlsafe_base64`
6. (**) Zmień routing tak, by przekierowania były dostępne pod `/:source` zamiast `/links/:source`. Postaraj się zrobić to tak, by routing tylko brał pod uwagę `source` w poprawnym formacie.

   Tip: pomoże tu regex
