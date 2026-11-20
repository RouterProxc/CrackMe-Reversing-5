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
