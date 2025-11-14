<h1>Work-Case№6</h1>

Розгляньте дані питання та дайте відповіді:

1. В робочому просторі операційної системи необхідно встановити декілька командних інтерпретаторів (окрім bash ще 2 на ваш вибір):

- Якими командами це можна зробити?

Я обрав zsh та fish.

Встановити їх можна задопомогою:

    sudo apt update
    sudo apt install zsh
    sudo apt install fish
<img width="619" height="141" alt="image" src="https://github.com/user-attachments/assets/bf8deff2-b086-4778-a37e-64a6a2ececf5" />
<img width="622" height="138" alt="image" src="https://github.com/user-attachments/assets/48d171f5-1973-443a-8bd9-711fece623bc" />

  
- Опишіть коротко можливості кожного з них.

Zsh

    -	Розширене автодоповнення.
    
    -	Удосконалені шаблони та робота з файлами.
    
    -	Підтримка Oh-My-Zsh для розширень і тем.
    
    -	Більш гнучка конфігурація ніж bash.

Fish (Friendly Interactive Shell)

    -	Інтерактивний автоперфект: підсвічування, підказки.
    
    -	Не використовує POSIX-сумісний синтаксис (простий для вивчення).
    
    -	Має готову автоконфігурацію та web-based конфігуратор.
    
    -	Тему та плагіни можна додавати через fisher.


2. Необхідно створити 10 нових користувачі в вашій системі та розподілити їх по групам:

Для початку створимо групи:

<img width="742" height="203" alt="image" src="https://github.com/user-attachments/assets/37fd510a-c1a1-4a1f-9e05-e3eff0ee6620" />

<img width="375" height="173" alt="image" src="https://github.com/user-attachments/assets/2f4f3e24-5f26-4a03-b3d6-5a1f7ba13eab" />

Далі додаємо користувачів й одразу розподіляємо інтерпретатори:

- Technical support (технічна підтримка, системні адміністратори);

<img width="1004" height="69" alt="image" src="https://github.com/user-attachments/assets/6987e59b-e6a7-4cf5-ad95-ee50fa7fb993" />

- Developers (розробники, технічні спеціалісти свого профілю);

<img width="1004" height="64" alt="image" src="https://github.com/user-attachments/assets/80a5eb12-8665-4b91-a121-267ae7a9e73c" />

- Financiers (бухгалтерія, економісти тощо);

<img width="1004" height="26" alt="image" src="https://github.com/user-attachments/assets/726e3e31-3c72-4ad4-a2ac-853f25101055" />
<img width="1004" height="62" alt="image" src="https://github.com/user-attachments/assets/72f2432d-6d21-49a4-be6b-f02d3d570131" />

- Founders (керівництво);

<img width="897" height="57" alt="image" src="https://github.com/user-attachments/assets/1299cae2-20e1-403c-86aa-449e76b0f84a" />

- Guests (гості).

<img width="957" height="25" alt="image" src="https://github.com/user-attachments/assets/e17baed0-baa3-4234-a620-9afaa96affb6" />

Задопомогою cat/etc/passwd перевіряємо список користувачів:

<img width="517" height="31" alt="image" src="https://github.com/user-attachments/assets/2c72d149-1e63-4345-86f8-a939287748b0" />
<img width="799" height="344" alt="image" src="https://github.com/user-attachments/assets/ff2cffb2-2815-4738-bf3f-95892c8df6c0" />

Далі додаємо паролі длдя користувачів (я зробив паролі ідентичними іменам користувачів):

<img width="911" height="438" alt="image" src="https://github.com/user-attachments/assets/a7fe3cc2-747c-498b-9b7a-dc402f6df4ea" />

3. Продемонструвати приклади роботи кожної групи користувачів у своєму командному інтерпретаторі – наприклад збір відомостей про систему, визначення базової конфігурації, системної дати, поточних каталогів тощо.

- Technical support (технічна підтримка, системні адміністратори);

<img width="1004" height="249" alt="image" src="https://github.com/user-attachments/assets/bf49a6c9-c904-47a5-95c2-c9ce654a336c" />

- Developers (розробники, технічні спеціалісти свого профілю);

<img width="388" height="66" alt="image" src="https://github.com/user-attachments/assets/f8548d41-e9f9-4df0-8d75-79b3a4ac192c" />
<img width="1004" height="716" alt="image" src="https://github.com/user-attachments/assets/0554831c-1501-42c3-809d-2831077d30fe" />
<img width="377" height="80" alt="image" src="https://github.com/user-attachments/assets/5eda7966-afd8-4078-9567-68f610a89b8a" />

- Founders (керівництво);

<img width="750" height="180" alt="image" src="https://github.com/user-attachments/assets/58341645-da55-4197-9d5f-ba614835ff31" />
<img width="459" height="70" alt="image" src="https://github.com/user-attachments/assets/86d4e428-4924-4d01-84db-752acc03275b" />

<h1>Glossary of terms</h1>

Bash (Bourne Again Shell) - Основний shell у Linux; підтримує скрипти, команди та автоматизацію.

Zsh (Z Shell) - Розширений shell з покращеним автодоповненням, налаштуваннями та плагінами.

Fish (Friendly Interactive Shell) - Зручний shell із підсвічуванням, підказками та простим налаштуванням.

Group - Об’єднання користувачів, яке дозволяє керувати дозволами.

Technical Support Group - Група працівників технічної підтримки та адміністраторів.

Developers Group - Група розробників та технічних спеціалістів.

Financiers Group - Група бухгалтерів, економістів та фінансових співробітників.

Founders Group - Група управлінців і керівництва.

Guests Group - Група тимчасових або обмежених користувачів.

UID (User ID) - Унікальний числовий ідентифікатор користувача.

/etc/passwd - Системний файл, що зберігає дані про всіх користувачів.

/etc/group - Файл із записами всіх груп у системі.

useradd - Команда для створення нового користувача.

usermod - Команда для зміни параметрів існуючого користувача.

userdel - Команда для видалення користувача з системи.

groupadd - Команда для створення нової групи.

chsh (Change Shell) - Команда для зміни shell за замовчуванням.

<h1>Conclusion</h1>

During the completion of this work, the main tools for managing users, groups, and command-line shells in the Ubuntu operating system were studied and applied. Additional shells, specifically Zsh and Fish, were installed, their functionalities were analyzed, and compared with the default Bash. Ten new users were created and assigned to the appropriate groups according to the task requirements. For each group, the required shell was configured or access to the shell was restricted as needed.

Basic commands were demonstrated for different types of users within their respective shells, which allowed verifying the correctness of the system configuration. Practical experience was gained using commands such as useradd, usermod, groupadd, passwd, chsh, as well as understanding the structure of system files /etc/passwd and /etc/group.
