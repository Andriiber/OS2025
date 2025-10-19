<h1>Work-Case№2</h1>

1. В ході роботи досить часто виникає необхідність встановлювати нові програми та додатки. Для цього необхідно в терміналі вміти працювати з менеджерами пакетів:

- Дайте розгорнуте визначення таким поняттям як «пакет» та «репозиторій».

      Пакет
      
      Пакет — це архів, який містить програмне забезпечення (виконувані файли, бібліотеки, конфігураційні файли, скрипти встановлення/видалення тощо), необхідне для встановлення програми в операційній системі Linux.
      Зазвичай пакет має розширення, яке залежить від сімейства дистрибутивів:
      
      .deb — для Debian, Ubuntu, Linux Mint;
      
      .rpm — для Red Hat, Fedora, CentOS, openSUSE;
      
      .pkg.tar.zst — для Arch Linux.
      
      Репозиторій
      
      Репозиторій — це віддалене сховище пакетів, доступне через інтернет або локальну мережу. Репозиторій містить:
      
      список доступних програм (метадані);
      
      самі пакети;
      
      інформацію про залежності;
      
      цифрові підписи для перевірки безпеки.
      
      Репозиторії бувають:
      
      Офіційні (надаються розробниками дистрибутиву);
      
      Неофіційні / сторонні (створені спільнотою або сторонніми розробниками);
      
      Локальні (використовуються у корпоративних мережах).

- Надайте короткий огляд існуючих менеджерів пакетів у Linux. Охарактеризуйте їх основні можливості.

| Менеджер                    | Використовується в        | Формат пакета              | Основні можливості                                                     |
| ----------------------------| --------------------------| ---------------------------|----------------------------------------------------------------------- |
| APT (Advanced Package Tool) | Debian, Ubuntu, Mint      | .deb                       | Автоматичне встановлення залежностей, пошук пакетів, оновлення системи |
| DNF (Dandified YUM)         | Fedora, RHEL, CentOS      | .rpm                       | Керування пакетами, репозиторіями, робота з кешем                      |
| Zypper                      | openSUSE, SUSE Linux      | .rpm                       | Простий синтаксис, підтримка шаблонів, управління репозиторіями        |
| Pacman                      | Arch Linux, Manjaro       | .pkg.tar.zst               | Проста структура, висока швидкість, ручний контроль                    |
| Snap                        | Ubuntu, інші дистрибутиви | універсальний формат .snap | Ізольовані пакети, автоматичні оновлення                               |
| Flatpak                     | Універсальний менеджер    | .flatpak                   | Пісочниця для програм, підтримка різних дистрибутивів                  |
| AppImage                    | Будь-який дистрибутив     | .AppImage                  | Не потребує встановлення, просто запускається                          |


2. Визначте який менеджер пакетів використовує ваш дистрибутив Linux. Опишіть основні команди для роботи з ним:

Щоб визначити менеджер пакетів терба відкрити термінал і ввести по черзі кілька команд. Якщо якась з них спрацює — значить, цей менеджер пакетів у тебе встановлений.

    apt --version
    dnf --version
    yum --version
    zypper --version
    pacman --version

В мене спрацювала ```apt --version```, отже мій менеджер пакетів

- Пошук, скачування та установка необхідних пакетів, яких у Вашій системі немає (зі сховища по замовчуванню, з нового репозиторію тощо).

      Пошук пакета в репозиторії
      apt search <назва_пакета>
      
      
      Наприклад:
      
      apt search vlc
      
      
      — знайде усі пакети, пов’язані з відеоплеєром VLC.
      
      
      Скачування та встановлення пакета
      sudo apt install <назва_пакета>
      
      
      Приклад:
      
      sudo apt install vlc

- Перегляд інформації про встановлені та доступні пакети.

      Детальна інформація про пакет
      apt show <назва_пакета>
      
      
      Наприклад:
      
      apt show vlc
      
      Список усіх встановлених пакетів
      apt list --installed
      
      Перевірити, чи встановлений пакет
      dpkg -l | grep <назва_пакета>

- Видалення непотрібних або застарілих пакетів.

      Видалення програми (залишає конфігураційні файли)
      sudo apt remove <назва_пакета>
      
      Повне видалення разом із налаштуваннями
      sudo apt purge <назва_пакета>
      
      Очищення системи від старих чи непотрібних пакетів
      sudo apt autoremove
      sudo apt clean
      
      
      autoremove — видаляє пакети, що більше не використовуються;
      
      clean — очищує кеш завантажених .deb файлів.
                          
- Оновлення менеджера пакетів.

      Оновлення списку доступних пакетів
      sudo apt update
      
      Оновлення усіх встановлених пакетів
      sudo apt upgrade
      
      Оновлення самого APT (менеджера пакетів)
      sudo apt install --only-upgrade apt
      
      Повне оновлення системи (якщо змінилася версія дистрибутиву)
      sudo apt full-upgrade

3. Встановіть у терміналі через менеджер пакетів на свою систему:

- Новий відео- чи аудіоплейер.

Встановлення відео-/аудіоплеєра

Наприклад, встановимо VLC Media Player:

sudo apt update
sudo apt install vlc

<img width="725" height="429" alt="image" src="https://github.com/user-attachments/assets/d5cdf4f4-9f9e-4dd2-9415-f8e7a5ea8186" />

Перевіримо чи встановилось задопомогою команди which vlc

<img width="339" height="39" alt="image" src="https://github.com/user-attachments/assets/f49f32e6-965b-4a8d-92aa-b2ac4dd10fb0" />


- Середовище для мови програмування, що ви вивчаєте.

Встановимо С++

<img width="722" height="210" alt="image" src="https://github.com/user-attachments/assets/e07e92b8-2443-485e-bc67-d1125ad86114" />

<img width="725" height="246" alt="image" src="https://github.com/user-attachments/assets/b80c8d65-77e8-48b4-9ed0-17aeae093a43" />

Перевіримо:

<img width="395" height="46" alt="image" src="https://github.com/user-attachments/assets/2b5a4687-7ea5-4a44-b684-838bee5a1247" />


4. Яким чином можна встановити нові програми через магазини додатків та менеджери пакетів у графічному середовищі. Наведіть свої приклади.

Окрім терміналу, програми можна встановлювати через графічні магазини додатків, наприклад в мене в віртуальній машині є App Center - ммагазтн для додатків.

<img width="641" height="483" alt="image" src="https://github.com/user-attachments/assets/35cf7d42-1c3d-47b3-a5ca-d57a45490223" />

Заавдяки ньому також можна встановлювати додатки:

<img width="800" height="599" alt="image" src="https://github.com/user-attachments/assets/92059870-c4a1-4c31-b5f0-b68b768dbccf" />

<h1>Glossary of terms</h1>

Package (Пакет) – an archive containing software (executables, libraries, configuration files, installation/removal scripts, etc.) required to install a program on a Linux system.

Repository (Репозиторій) – a remote storage of packages, available via the internet or a local network, containing available software, metadata, dependencies, and digital signatures.

Package manager (Менеджер пакетів) – a tool for installing, updating, removing, and managing software packages on a Linux system.

Dependencies (Залежності) – other software packages required for a program to work properly.

Cache (Кеш) – temporary storage of downloaded packages to speed up future installations.

Sandbox (Пісочниця) – an isolated environment where applications can run without affecting the rest of the system.

App store / Software center (Магазин додатків) – a graphical interface for browsing, installing, and managing software packages.

Package format (Формат пакета) – the specific file type in which software is packaged for installation (e.g., .deb, .rpm, .pkg.tar.zst).

System update (Оновлення системи) – the process of updating all installed packages to their latest versions.

Package removal (Видалення пакета) – the process of uninstalling a package, optionally keeping or removing its configuration files.

Package search (Пошук пакета) – looking for a specific package in repositories.

Package installation (Встановлення пакета) – downloading and installing a package from a repository or local file.

Cache cleaning (Очищення кешу) – removing temporary downloaded package files to free up space.

Automatic dependency resolution (Автоматичне встановлення залежностей) – installing all required packages automatically when installing a program.

Graphical environment (Графічне середовище) – a visual interface for interacting with the system, as opposed to the command line.

Terminal (Термінал) – a text-based interface for entering commands directly into the system.

Package metadata (Метадані пакета) – information about a package, such as version, dependencies, description, and maintainer.


<h1>Conclusion</h1>

In this work-case, I became familiar with the basics of working with packages and package managers in Linux. Key concepts were defined: a package as an archive containing software, a repository as a remote storage of packages, and a package manager as a tool for installing, updating, and removing programs.

Practically, new programs were installed via the terminal: the VLC media player and a programming environment for C++. I also explored installing programs through graphical app stores, which is convenient for users who prefer a visual interface.

Thus, knowledge of working with packages and package managers allows effective software management in Linux, keeps the system up-to-date, and helps avoid dependency issues. This is an important skill for any Linux user or administrator.
