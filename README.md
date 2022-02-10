# [SysinternalsSuite](https://download.sysinternals.com/files/SysinternalsSuite.zip)

--------------------------

Świetne narzędzia dla systemu Windows


# Case 1
# Płatnik po aktualizacji  nie uruchamia się ze zwykłego użytkownika

Po dodaniu user01 do grypy Administratorzy program płatnik uruchamia się bez problemu, na zwykłym użytkowniku nie działa - brak komunikatu dlaczego.

Uruchamiamy program Process Monitor ustawiamy odpowiedni filtr

![platnik_process_monitor](https://user-images.githubusercontent.com/75216446/153391844-cc71c419-aae7-478b-bb9e-d9a78897a4d8.png)

okazało się że ACCESS DENIED wystąpił na pliku - C:\Platnik\ASSECO.AKTUALIZUJ.PP.exe

po dodanu uprawnień dla konkretnego użytkownika (bądź grupy) wszystko działa prawidłowo.


Nie należy od razy dodawać użytkownika do grupy local Admin gdy coś nie działa, warto czasem sprawdzić programem Process Monitor
