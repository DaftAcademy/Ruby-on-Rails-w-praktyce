# Zadanie 2

Do rozwiązania tego zadania przyda się wiedza o klasach, którą znasz z ostatnich zajęć. W szczególności zwróć uwagę na takie zagadnienia jak dziedziczenie, zmienne klasowe i instancyjne, oraz możliwość nadpisywania metod.

Chcemy zbudować funkcjonalność typu kalendarz, która będzie wyświetlała użytkownikowi zapisane wydarzenia.

W tym celu powinniśmy wykonać kilka kroków:
1. Przygotuj klasę `Event` opisującą pojedyncze wydarzenie z kalendarza zawierającą następujące pola:
   - `created_at`
   - `description`
   - `due_date`
2. Stwórz kontroler w którym stworzysz nowe wydarzenie i widok w którym go wyświetlisz w przystępnej dla użytkownika postaci. Nie zapomnij dodać odpowiedniej ścieżki do `routes.rb`!

   `get 'my_address' => 'controller#action'`
   
   Tip: `rails generate controller` potrafi od razu wygenerować akcje i widoki
3. Korzystając z dziedziczenia utwórz klasy dla bardziej sprecyzowanych typów wydarzeń:
   - `Birthday` - zawiera dodatkowo imię i nazwisko jubilata
   - `Reminder` - posiada dodatkowy opis
   - `Task` - przechowuje informację o ukończeniu zadania natomiast nie posiada konkretnej daty
4. Stwórz przykładowe wydarzenie każdego typu i wyświetl je w aplikacji, uwzględniając różnice między nimi.
5. Teraz możemy spróbować zgrupować nasze wydarzenia w jakiś kalendarz. Na nasze potrzeby wystarczy jeśli będziemy je przechowywać w tablicy.

   (*) Albo przedstawić kalendarz za pomocą klasy.
6. Wypisz pod kalendarzem liczbę wydarzeń w aktualnym kalendarzu.
   
   (*) Wyświetl obok liczbę wszystkich wydarzeń stworzonych kiedykolwiek, niekoniecznie dodanych do aktualnego kalendarza.
7. (*) Skoro mamy już wydarzenia w postaci tablicy-kalendarza to nie ma potrzeby przekazywania ich do widoku pojedynczo. Spróbuj tak zmodyfikować widok i kontroler, aby jedynym przekazywanym obiektem (jedyna zmienna instancyjna) był kalendarz. Tip: zapewne będziemy chcieli w widoku zrobić jakieś `.each`
   
   (**) Skorzystaj z partiala, któremu przekażesz listę wydarzeń jako kolekcję
