## Work-Case №6
1. В робочому просторі операційної системи необхідно встановити декілька командних інтерпретаторів (окрім bash ще 2 на ваш вибір):

- Якими командами це можна зробити;

Встановлюємо dash і ksh

За допомогою команд: 

```sudo apt update```

  ``` sudo apt install dash ksh```
  
<img width="426" height="52" alt="Снимок экрана 2025-11-17 в 18 57 35" src="https://github.com/user-attachments/assets/3666ec49-1bb0-4266-884e-f0461a779070" />

- Опишіть коротко можливості кожного з них.

bash

– стандартний shell  
– автодоповнення, історія команд  
– підтримка складних скриптів  

dash

– легковаговий /bin/sh  
– дуже швидкий  
– мінімальний набір можливостей  
– використовується для системних скриптів  

ksh (KornShell)

– потужний shell  
– схожий на bash  
– підтримує асоціативні масиви  
– розширені можливості для скриптів  

2. Необхідно створити 10 нових користувачі в вашій системі та розподілити їх по групам:

- Technical support (технічна підтримка, системні адміністратори);

- Developers (розробники, технічні спеціалісти свого профілю);

- Financiers (бухгалтерія, економісти тощо);

- Founders (керівництво);

- Guests (гості).

3. Для кожного з користувачів визначити його командний інтерпретатор за замовчуванням:

- Technical support – bash;

- Developers – командний інтерпретатор 1 (ksh);

- Financiers – заборонити доступ до командних інтерпретаторів;

- Founders – командний інтерпретатор 2 (dash);

- Guests – заборонити доступ до командних інтерпретаторів.


<p align="center"><img width="434" height="236" alt="image" src="https://github.com/user-attachments/assets/672d8e5e-9be1-4bac-a517-b7d612d0b827" /></p>
<p align="center">Створення груп</p>

<p align="center"><img width="662" height="547" alt="image" src="https://github.com/user-attachments/assets/3037fa32-b091-4957-b9e1-429dcd1a4c60" /></p>
<p align="center">Створення користувачів та додавання інтерпретаторів за замовчуванням</p>
<p align="center"><img width="674" height="138" alt="image" src="https://github.com/user-attachments/assets/7f091473-80c6-4ebe-9a61-25859abea906" /></p>
<p align="center">Показати всіх користувачів</p>

Паролі до користувачів: <img width="248" height="126" alt="image" src="https://github.com/user-attachments/assets/0909f655-f2b5-4edd-9e26-f74dad612697" />

Для кожного користувача я додав пароль за допомогою команди ```passwd <username> ```


<p align="center"><img width="933" height="199" alt="image" src="https://github.com/user-attachments/assets/b2d7c33a-64c9-4ed8-9a91-11ef084ef2f5" /> </p>
<p align="center"> Перевірка записів у /etc/passwd (щоб побачити shell для кожного)</p>


4. Продемонструвати приклади роботи кожної групи користувачів у своєму командному інтерпретаторі – наприклад збір відомостей про систему, визначення базової конфігурації, системної дати, поточних каталогів тощо.
<p align="center"><img width="916" height="957" alt="image" src="https://github.com/user-attachments/assets/736320c1-b2db-433c-b2e5-cf4d5d52907f" /></p>
<p align="center">Демонстрація роботи кожної групи користувачів </p>

## Conclusion

During the completion of this Work-Case, full user and group management was implemented within a Linux operating system. Three different command interpreters — bash, ksh, and dash — were installed and configured, with their basic capabilities demonstrated. Five separate user groups and exactly ten user accounts (two per group) were created. Each user was assigned an appropriate shell according to their role, while restricted groups were configured with the nologin shell to prevent system access.

Passwords for all users were set manually, enabling verification of authentication procedures. The functionality of each shell environment was demonstrated by executing basic system commands. Additional verification was performed using system files such as /etc/passwd and /etc/group, as well as through Linux user-management commands.

This assignment provided practical experience with essential Linux administration tools, including user creation, group management, shell assignment, and access control verification. The work builds fundamental system administration skills and strengthens understanding of how Unix-like systems organize and manage user environments.
