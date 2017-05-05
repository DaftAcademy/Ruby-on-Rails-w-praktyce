# Zadanie 5

Na ostatnich zajęciach pogłębiliśmy temat relacji oraz biblioteki (gema) Devise. Usprawnijmy funkcjonalność naszego serwisu o poniższe:

1. Przenies wyświetlanie wiadomości `flash` z pojedyńczych widoków do layoutu (`views/layouts/application.html.erb`). Wyświetlaj je tylko wtedy gdy istnieją, jeśli "owiniesz" je w jakiś kontener, jego również nie wyświetlaj.

2. Dodaj do layoutu nagłówek z następującymi elementami:
   - link do listy linków (`links#index`)
   - link do zalogowania
   - link do rejestracji
   
   Tip: w razie niepewności - `rake routes`

3. W razie gdy jest zalogowany uzytkownik, zastąp linki do logowania i rejestracji poniższymi:
   - adres email
   - link do wylogowania
   
   Tip: pomoże metoda `user_signed_in?`

4. Zmodyfikuj akcję `index` oraz jej widok w taki sposób, by wyświetlała wszystkie linki w serwisie, ale licznik wejść oraz link do usunięcia tylko dla właściciela danego linka. Pamiętaj, że link może być tylko usunięty przez jego właścicela, nie wystarczy schować link na widoku!

5. Dodaj do modelu `User` booleanowskie pole `admin` oraz:
   - ustaw jego wartość domyślną na `false`
   - (*) pozwól administratorom widzieć licznik i kasować wszystkie linki
   - (**) ujednolić metodę autoryzacji (właściciel lub admin), tak by skorzystać z tej samej metody zarówno przy wyświetlaniu jak i usuwaniu linków
