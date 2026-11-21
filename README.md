# CrackMe-Reversing-5

<img width="867" height="152" alt="image" src="https://github.com/user-attachments/assets/569858ec-9887-408d-be7c-83d53a4e7e8b" />

Открыв в BinaryNinja нахожу _start 

<img width="856" height="306" alt="image" src="https://github.com/user-attachments/assets/2be5fc6c-92e9-4be6-a5cd-46c781a2556d" />

Вызывается функция расшифровки функций, а после нее проверка на отладчик

<img width="756" height="316" alt="image" src="https://github.com/user-attachments/assets/26762bba-bfcc-494b-a4a1-9449c777ed26" />

Отладка ловится - выдает ошибку 

<img width="286" height="228" alt="image" src="https://github.com/user-attachments/assets/8977645b-ff3e-43c0-b252-f3e2e03092e7" />

Патчим проверку на отладку (обязательно обе проверки - && состояние)

После проверки на отладчик вырисовывается картина 

<img width="603" height="301" alt="image" src="https://github.com/user-attachments/assets/4cf2e428-54f1-4fff-9ecc-fa83421dac68" />

Дальше для удобства я открыл .data с расшифрованными функциями и сопоставил их в BinaryNinja по адресам и названиям

<img width="456" height="566" alt="image" src="https://github.com/user-attachments/assets/b7f5d4c6-b92f-404e-aef4-1ac0178754fa" />


<img width="869" height="533" alt="image" src="https://github.com/user-attachments/assets/e4e1a897-401a-4fc1-83b4-478517906271" />

Пройдемся по модулям защиты (функциям имеется ввиду)

ExceptionBreakPoint:

<img width="592" height="224" alt="image" src="https://github.com/user-attachments/assets/905c19f4-b6e3-469b-a977-229368c4c8c2" />

~ Происходит установка байта отладки (0xCC - int 3). Если к программе присоединен отладчик - он перехватит этот БРЯК и функция в VEH (идет до SEH) не найдет бряк - то есть программа отлаживается  
