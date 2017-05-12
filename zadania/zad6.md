# Zadanie 6

Na ostatnich zajęciach dowiedzieliśmy się więcej o Devise i zaczęliśmy przestrukturowywanie naszej architektury. Dokończmy to co zaczęliśmy:

1. Wykonaliśmy już migrację, ale brakuje nam jeszcze jednej rzeczy. Zdefiniuj relacje w modelach `User` i `Link` w taki sposób, by wskazywały na połączone modele (np. `link.user` zwróci właściciela linku).
   
   Tip: przy relacji wykorzystaj opcję `through:`

2. Dodaj do widoku tworzenia opcję wybrania odpowiedniej widoczności (użyj `radio_button`).

3. Zapisz efekt w akcji `create`, pamiętaj o modelu `Setting` oraz silnych parametrach.
   
   (*) skorzystaj z jednego zestawu parametrów by stworzyć `Setting` i `Link` "na raz"

   Tip: poczytaj sobie o `nested_attributes`

4. Ustaw odpowiednią widoczność dla linków w akcji `show`, tzn:
   - pozwól wszystkim `global` linkom być używanym przez wszystkich (nie wymaga logowania)
   - pozwól wszystkim `users` linkom być używanym tylko przez zalogowanych
   - pozwól wszystkim `owner` linkom być używanym tylko przez właścicieli
   - zachowaj fakt, że admin ma taki dostęp jak owner

(**) Ostatnie zadanie można rozwiązać na wiele sposobów, postaraj się zaproponować taki, który byłby zgodny z ogólnymi zasadami czytelności Railsów, chociażby minimalizując "rozmiar" kontrolera. Poczytaj sobie o patternie Service Objectu.
