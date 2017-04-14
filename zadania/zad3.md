# Zadanie 3

Zrobiliśmy sobie ostatnio podstawy `ActiveRecordu` i RESTa, poniższe zadania pozwolą lepiej przyswoić sobie ten szeroki temat.

Pamiętajcie, że możecie zawsze się poradzić czy dopytać mailowo :)

1. Wygeneruj migrację, stwórz model Event opisujący te same informacje, które opisywała poprzednia klasa Event. Stwórz odpowiedni kontroler.
2. Aby umożliwić użytkownikowi zobaczenie wydarzeń stwórz w kontrolerze RESTowe akcje `index` i `show`. Postaraj się wyświetlić dane korzystając z już istniejących widoków, które stworzyliśmy przy okazji poprzedniej pracy domowej.

    - Stwórz kilka przykładowych rekordów w bazie
    - W widoku listy wydarzeń dodaj linki umożliwiające zobaczenie każdego wydarzenia osobno
    
      Tip: `link_to resource_path` generuje odnosnik
    - (*) W widoku `index` domyślnie ukryj zakończone wydarzenia (`due_date` w przeszłości). Pozwól na pokazanie wszystkich np. przez przekazanie parametru w adresie

3. Prawdziwy kalendarz, oprócz oglądania pozwala zwykle też tworzyć nowe wydarzenia. Pierwszym takim krokiem jest przygotowanie formularza umożliwiającego wysłanie danych na serwer. Stwórz w kontrolerze akcję `new` i odpowiedni widok w którym wyświetlisz formularz tworzenia wydarzenia.

    Tip: `form_for resource` pomoze w generacji formularza

    - Ponieważ dostępna jest ograniczona liczba rodzajów wydarzenia, użyj `<select>` do wyświetlenia listy dostępnych rodzajów wydarzenia.
    - (*) Żeby ułatwić użytkownikowi podanie daty w odpowiednim formacie rozejrzyj się za jakąś biblioteką do wyświetlania kalendarza i spróbuj użyć jej w projekcie

4. Dane z formularza muszą gdzieś trafić, żeby zostały zapisane. Odpowiedzialna za to jest akcja `create`, która powinna przyjmować parametry wysłane przez formularz i tworzyć z nich nowy `Event`. Dla ułatwienia możesz założyć, że przekazane parametry są zawsze poprawne.
    
    Tip: Railsy dbają o bezpieczeństwo i nie pozwolą stworzyć obiektu przez przekazanie im wszystkich parametrów z zapytania. Żeby nie musieć wypisywać wszystkich parametrów osobno przeczytaj o strong parameters w Ruby on Rails
    - (*) Dodaj pozostałe modele opisujące typ wydarzenia (`Birthday`, `Task`, `Reminder`). Wykorzystaj STI aby przechowywać je wszystkie w jednej tabeli.

      Pamiętaj o dodaniu odpowiednich pól wymaganych przez różne typy wydarzeń i o ich odzwierciedleniu w formularzu dodawania wydarzenia
      
      Nie zapomnij też o dodaniu do klas metod wyświetlających odpowiednio sformatowane dane, które tworzyliśmy poprzednim razem
    - (**) Wykorzystując JavaScript lub odpowiednią konstrukcję formularza wyświetlaj tylko pola pasujące do aktualnie tworzonego wydarzenia
