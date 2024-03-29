# Simple-Server
Sieci komputerowe zadanie nr. 1

Należy przygotować serwer, do którego można podłączyć się programem telnet,
pełniącym rolę klienta.

Po zaakceptowaniu połączenia od klienta serwer wypisuje na standardowe wyjście
informację, że klient się podłączył. U klienta wypisuje się menu główne:

Opcja A  
Opcja B  
Koniec  

W kliencie strzałkami w górę i w dół poruszamy się po menu, a enterem wybieramy
opcję. Po wybraniu opcji Koniec serwer wypisuje na standardowe wyjście
informację, że klient się odłączył i zamyka połączenie z klientem, ale nie
kończy działania – czeka na kolejnego klienta. Klienty są obsługiwane
sekwencyjnie.

Po wybraniu opcji A u klienta poniżej menu wypisuje się A. Po wybraniu opcji B
u klienta wypisuje się menu:

Opcja B1  
Opcja B2  
Wstecz  

Analogicznie wybranie opcji B1 lub B2 powoduje wypisanie u klienta poniżej menu
B1 lub B2. Wybranie opcji Wstecz powoduje powrót do menu głównego i jego
wyświetlenie. Opcjonalnie można dodać powrót przez wciśnięcie PgUp.

Serwer uruchamia się z linii poleceń, podając jako argument numer portu (liczba
dziesiętna), na którym serwer ma odbierać połączenia od klientów.

Komunikacja pomiędzy klientem a serwerem odbywa się po TCP z wykorzystaniem
protokołu telnet. Serwer powinien odpowiednio ustawić opcje telnetu.

Serwer powinien być odporny na podanie w linii poleceń niepoprawnego parametru
lub złej liczby parametrów. W takim przypadku należy wypisać stosowny komunikat
o błędzie na standardowe wyjście diagnostyczne i zakończyć serwer z kodem
powrotu 1.

Serwer nie powinien wysyłać nieprawidłowych danych.

Serwer powinien być odporny na na dowolne dane odebrane od klienta. W przypadku
otrzymania nieprawidłowych (złośliwych) danych serwer powinien je ignorować
i kontynuować działanie.

Rozwiązanie:

– powinno działać w środowisku Linux w laboratorium komputerowym  
– być napisane w języku C lub C++ z wykorzystaniem interfejsu gniazd  
– nie może korzystać z libevent ani boost::asio  
– powinno kompilować się za pomocą GCC (polecenie gcc lub g++)
  z parametrami -Wall -Wextra -O2 oraz -std=c11 lub -std=C++17

