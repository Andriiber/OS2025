<h1>Work-Case№7</h1>

Розгляньте дані питання та дайте відповіді:

1. В ході роботи досить часто виникає завдання планування задач:

- Охарактеризуйте основні функції які може виконувати планувальник завдань в будь-якій ОС. Порівняйте можливості планування завдань в різних ОС на прикладі Windows та Linux.

| Характеристика         | Linux Cron                                            | Windows Task Scheduler                               |
| ---------------------- | ----------------------------------------------------- | ---------------------------------------------------- |
| Конфігурація           | Текстовий файл (*crontab*)                            | Графічний інтерфейс + CLI                            |
| Частоти запуску        | Дуже гнучкі (хвилини, дні, місяці, діапазони, списки) | Гнучкі, але складні через GUI                        |
| Запуск по подіях       | Обмежено (лише anacron/atd)                           | Є запуск по подіях (лог, idle, підключення живлення) |
| Легкість автоматизації | Висока (файли, SSH, DevOps)                           | Середня                                              |
| Логування              | Через syslog                                          | Вбудоване у Task Scheduler                           |
| Гранулярність часу     | До хвилини                                            | До хвилини, але можливі тригери подій                |

    Linux Cron — найкращий для системного адміністрування та серверів.
    
    Windows Task Scheduler — зручний у середовищах з GUI та подіями системи.

- Опишіть основні принципи роботи з планувальником Cron в ОС Linux. Як його налаштовувати? Чи є йому альтернативи (дайте їх характеристику).

1. Основні принципи роботи з планувальником Cron:

Cron — це системний демон у Linux/Unix, який запускає команди або скрипти за розкладом. Його ключові принципи:
    
      Cron працює у фоновому режимі
      
      Процес crond постійно працює в системі.
      
      Кожну хвилину він перевіряє, чи потрібно щось запускати.

Налаштування завдань у спеціальних таблицях — crontab:

      Cron працює з так званими "таблицями завдань":
      
      Системний crontab: /etc/crontab
      
      Користувацькі crontab-файли: зберігаються у /var/spool/cron/username
      
      Редагуються через команду: crontab -e


2. Як налаштовувати Cron

Перегляд існуючих завдань

    crontab -l

Редагування

    crontab -e

Видалення всіх завдань

    crontab -r

Системний crontab

    Редагується вручну:
    
        sudo nano /etc/crontab

3. Альтернативи Cron:

        systemd timers – сучасна заміна, гнучкі, підтримують логування та запуск пропущених завдань.
        
        Anacron – для ПК, які не завжди увімкнені; виконує пропущені завдання при наступному старті.
        
        fcron – гнучкі інтервали, працює як cron та anacron одночасно.
    
        at / batch – одноразові або виконувані при низькому навантаженні завдання.
        
        Jenkins / GitLab CI – для автоматизації CI/CD, підтримують cron-подібний розклад.
        
        Kubernetes CronJobs – запуск контейнерів за розкладом у кластері Kubernetes.


2. Для вашої віртуальної машини зі встановленою ОС Linux здійсніть планування обраних вами задач (запуск додатків, вмикання/вимикання машини, очистка каталогів, видалення файлів, резервне копіювання, архівування тощо на ваш вибір) через планувальник Cron:

Для початку створюємо папку для скриптів:

<img width="423" height="23" alt="image" src="https://github.com/user-attachments/assets/f7e8743c-7a7d-4f53-9997-84770432b72a" />

Далі створюємо скрипти які в майбутньому будуть виконуватись:

Скрипт очищення каталогу:

<img width="424" height="20" alt="image" src="https://github.com/user-attachments/assets/4825e8da-48b9-4781-a6df-f3fdc9dcb818" />

<img width="1004" height="652" alt="image" src="https://github.com/user-attachments/assets/658b4b4d-a8cb-43e8-b9a3-b800e822070d" />

Скрипт для резервного копіювання:

<img width="656" height="36" alt="image" src="https://github.com/user-attachments/assets/0052722a-413e-4b57-982d-c57365eaeb03" />

<img width="1004" height="648" alt="image" src="https://github.com/user-attachments/assets/baa3f591-2885-4b5b-a17b-cda7838afac8" />

Надаємо права на виконання:

<img width="659" height="39" alt="image" src="https://github.com/user-attachments/assets/31173d23-3b19-42e9-846e-6b73f5a3bcec" />

Далі відкриваємо редактор cron задопомогою команди й додаємо туди задачі:

    crontab -e

- Виконання спланованої задачі в чітко визначений Вами час (наприклад о 8 ранку, 18.30 і т.д.).

<img width="547" height="33" alt="image" src="https://github.com/user-attachments/assets/dfabfb64-ad31-4aaa-bb15-95ba23d0ea3d" />

- Виконання однієї й тієї ж задачі двічі в день (час також визначаєте самостійно).

<img width="573" height="32" alt="image" src="https://github.com/user-attachments/assets/9e344a6c-264f-421c-a532-db73f86e90f5" />

- Виконання однієї й тієї ж задачі тільки в будні (або тільки у вихідні дні) у чітко визначений проміжок часу (наприклад з 8 до 18 години).

<img width="652" height="31" alt="image" src="https://github.com/user-attachments/assets/9d06e726-7027-4d53-a4f1-d2fd2deb25d7" />

- Виконання задач тільки раз у рік, раз у місяць, раз у день, щогодини, при вмиканні (після перезавантаження).

  Раз на рік:

<img width="532" height="28" alt="image" src="https://github.com/user-attachments/assets/bf53bf8f-5441-466d-b3f7-4c541e1d5b98" />

  Раз на місяць:

<img width="536" height="24" alt="image" src="https://github.com/user-attachments/assets/28c4591e-3741-4e20-9f11-fc1c75c8b275" />

  Раз на день:

<img width="550" height="30" alt="image" src="https://github.com/user-attachments/assets/f0c56858-8de8-4f76-8ac5-ffc267ab40fe" />

  Щогодини:

<img width="543" height="31" alt="image" src="https://github.com/user-attachments/assets/d79c20d5-3d2b-4ab3-83f2-d54902d59e8e" />

  При завантаженні системи:

<img width="505" height="27" alt="image" src="https://github.com/user-attachments/assets/cfa5f8e5-b966-4016-a1f0-da133befc8b4" />

Загалом повинно виглядати так:

<img width="1004" height="653" alt="image" src="https://github.com/user-attachments/assets/292b5122-0521-422a-ba9c-a6dead710998" />

Далі натискаємо Ctrl + O ---> Enter ---> Ctrl + X щоб зберегти зміни.

Після можемо перевірити список задач:

<img width="438" height="33" alt="image" src="https://github.com/user-attachments/assets/e3e72318-6601-499c-b591-8fdc1b456181" />

<img width="1004" height="652" alt="image" src="https://github.com/user-attachments/assets/7393813f-5807-4b6f-a3c6-19543ca919ef" />


3. Встановіть альтернативний Cron’у планувальник задач (на Ваш вибір). Виконані у завданні 2 дії продемонструйте через нього.

Встановлення альтернативи Cron та виконання тих самих задач

Обираємо systemd timers як найпотужнішу сучасну альтернативу.

systemd timers - замінник cron, інтегрований у systemd. Дає змогу запускати завдання за розкладом з точністю до секунд, логуванням та залежностями.

3.1. Створення systemd service

sudo apt install 

Файл:

    /etc/systemd/system/backup.service
    
    [Unit]
    Description=Backup script
    
    [Service]
    Type=oneshot
    ExecStart=/home/user/scripts/backup.sh

3.2. Створення timer
Приклад щоденного запуску о 08:00:

Файл:

    sudo nano /etc/systemd/system/backup.timer
    
    [Unit]
    Description=Daily backup at 08:00
    
    [Timer]
    OnCalendar=*-*-* 08:00:00
    Persistent=true
    
    [Install]
    WantedBy=timers.target

Активувати:

    sudo systemctl daemon-reload
    sudo systemctl enable backup.timer
    sudo systemctl start backup.timer

3.3. Приклади еквівалентів з пункту 2 через systemd timers

1. Двічі на день (10:00 і 22:00)

        OnCalendar=*-*-* 10:00:00
        OnCalendar=*-*-* 22:00:00

2. Лише у будні з 8 до 18

        OnCalendar=Mon..Fri 08..18:00

3. Раз на місяць

        OnCalendar=monthly

4. Раз на рік

        OnCalendar=yearly

5. При завантаженні

        [Timer]
        OnBootSec=1min


<h1>Glossary of terms</h1>


Task Scheduler - Планувальник задач — системна служба для автоматичного запуску програм або скриптів у заданий час або за умовами.

Cron - Планувальник задач у Linux, який виконує команди у визначений час або періодично.                                

Crontab - Файл або інструмент для редагування задач Cron; зберігає список команд для планування.                            

Shebang (#!/bin/bash) - Перша рядок скрипта, вказує Linux, яким інтерпретатором запускати скрипт.                                         

Script - Скрипт — файл із серією команд, які можна виконати автоматично.                                                                                                           

Systemd - Система ініціалізації і менеджер сервісів у сучасних Linux для керування процесами та задачами.                   

Systemd service - Файл конфігурації (.service) для systemd, який описує, як запускати програму чи скрипт.                         

Systemd timer - Файл конфігурації (.timer) для systemd, який планує запуск сервісу у визначений час або при завантаженні.       

@reboot - Спеціальний тригер в Cron, що означає “запускати після перезавантаження системи”.                                

OnCalendar - Параметр в systemd timer, що задає час і частоту запуску сервісу.                                                 

Persistent=true - Параметр systemd timer, який дозволяє виконати пропущені завдання після вимкнення системи.                        

Tar / gzip (tar -czf) - Команда Linux для архівування та стиснення файлів.                                                                

Backup - Резервне копіювання файлів чи каталогів для збереження даних.                                                     

Cleanup - Очищення тимчасових або непотрібних файлів.             

<h1>Conclusion</h1>

During the completion of this work-case, the mechanisms of task scheduling in operating systems were thoroughly examined, and their practical application was implemented using Linux as an example. A task scheduler allows for the automation of program, script, and command execution at specified times or under certain conditions, significantly simplifying system administration and ensuring the regularity of routine operations.
The practical part of the work-case included creating scripts for cleaning directories, backing up files, archiving, and running tasks at system startup. Instructions were provided on how to configure crontab for executing tasks at different time intervals: daily, hourly, twice a day, on weekdays or weekends, as well as once a month or once a year. To ensure reliable execution after system startup, systemd timers were used as a modern alternative to Cron.
Automating tasks in Linux using Cron and systemd timers enhances administrative efficiency, guarantees regular backups, and maintains system support without continuous user intervention. These tools are powerful and flexible for solving a wide range of system management tasks.
