<h1>Work-Case№3</h1>

1. В робочому середовищі віртуальної машини Virtual Box, VMWare Workstation (або інший на Ваш вибір) необхідно виконати:

- Клонування вашої віртуальної робочої ОС (Work-case 2). Яким чином це можна зробити? Продемонструйте всі етапи;

1. Запускаємо Virtual Box.
2. Обираємо віртуальну машину.

3. На верхній панелі натиснути "Машина"

<img width="643" height="488" alt="image" src="https://github.com/user-attachments/assets/ee9b4f85-19c1-4938-9086-6315bdf7b7ec" />

4. Обрати "Клонувати"

<img width="251" height="465" alt="image" src="https://github.com/user-attachments/assets/ce14e37f-3f9b-44ce-bc8d-1070ed43b871" />

5 Налаштувати:
  * Назва
  * Розташування
  * Clone Type (Повний клон; Сполучений клон)
  * Зрізи (Current Machine State; Bre)
  * OS Installation Options (MAC Address Policy; OS Installation Options)
<img width="627" height="436" alt="image" src="https://github.com/user-attachments/assets/2aeb55bf-0805-4292-ab7c-994b0c0acb63" />

- Може виникнути необхідність перенесення (клонування) ОС у інше віртуальне середовище. Які треба виконати дії для експорту вашої віртуальної робочої ОС?

1. В верхній панелі обираємо "Файл"
2. Обираємо "Експортувати образ віртуальної машини"
<img width="364" height="173" alt="image" src="https://github.com/user-attachments/assets/8655add9-fb9e-4200-a74b-af80bcd4fd66" />

3. Налаштовувати:

<img width="625" height="487" alt="image" src="https://github.com/user-attachments/assets/6b5e4425-6a8f-42d7-8038-afd214689496" />
<img width="625" height="488" alt="image" src="https://github.com/user-attachments/assets/a351c0fe-5e21-42b7-9560-b5f600b9c3a8" />
<img width="627" height="491" alt="image" src="https://github.com/user-attachments/assets/f2305996-2ac6-42c3-8a1d-3fe35bc7b4e1" />


5. В ході роботи одна робоча віртуальна машина може взаємодіяти з іншою. Для цього необхідно між ними розгорнути мережу. Опишіть які типи організації мережевих з’єднань підтримуються в середовищі віртуальних машин, в чому особливість кожного з них:

- Трансляція мережевих адрес (NAT) -ВМ використовує IP хоста для виходу в Інтернет.
Найпростіший спосіб дати ВМ доступ до Інтернету, але не дозволяє іншим машинам бачити цю ВМ напряму.

- Мережевий міст (Bridged) - ВМ напряму підключена до реальної мережі (через адаптер хоста).
ВМ отримує IP від того ж роутера, що й хост. Доступна в локальній мережі.

- Віртуальний адаптер хоста (Host-only) - Створює ізольовану мережу між хостом і ВМ.
Без доступу до Інтернету, лише взаємодія між хостом і ВМ.

- Внутрішня мережа (Internal Network) - Повністю ізольована мережа між ВМ усередині VirtualBox.
Інтернету немає, лише внутрішній обмін між віртуальними машинами.

3. Розгорніть мережу між вашою робочою ОС та її клоном (завдання 1):

- Продемонструйте базові команди для налаштування мережевих параметрів ОС, поясніть, що вони виконують.

      Перегляд мережевих інтерфейсів:
      ip a — показує всі активні мережеві адаптери та їхні IP-адреси.

    <img width="725" height="446" alt="image" src="https://github.com/user-attachments/assets/f7c904cc-38d4-4395-a8e9-315c41af0eb2" />


      Перевірка зв’язку між машинами:
      ping 192.168.56.102
  
      (де 192.168.56.102 — IP другої ВМ)
  
    <img width="632" height="266" alt="image" src="https://github.com/user-attachments/assets/a9856cc8-a5d8-487d-b3bc-7abfce414f4e" />

      Перевірка виходу в Інтернет:
      ping google.com

    <img width="894" height="218" alt="image" src="https://github.com/user-attachments/assets/04038cbe-a0d0-42e1-8f3f-2679d44049a1" />

      Перегляд таблиці маршрутів:
      ip route

    <img width="721" height="66" alt="image" src="https://github.com/user-attachments/assets/d349f497-0d0f-446a-9769-5405eac49902" />


      Налаштування IP вручну (якщо потрібно):
      sudo ip addr add 192.168.56.101/24 dev eth1
      sudo ip link set eth1 up

- Обидві ОС мають мати вихід у мережу Інтернет. Відкрийте браузер та перегляньте будь-яке відео в youtube

Віртуальна машина 1:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c84e4ec6-33c4-4d96-93e8-8efcd7cffcc0" />

Віртуальна машина 2:

<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/23e029b4-1508-4bd8-950f-814a08dd7b7c" />

- Налаштуйте та продемонструйте обмін повідомленнями між двома ОС по локальній мережі. Які команди в терміналі при цьому необхідно ввести?

1. Запускаємо одночасно дві віртуальні машини.
2. В обох входимо в термінал
3. на першій віртуальній машині вводимо nc -l -p 1234 - задопомогою цієї команди віртуальна машина зможе прийняти повідомлення.
4. На іншій вводимо команду echo "*повідомлення*" | *ip адреса першої віртуальної машини* (Можна взнати задопомогою команди ip a)

Результат:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c1dad06d-6a59-435c-a6a6-05d5b170dcb1" />


- Налаштуйте спільну мережеву папку для обох ОС. Спробуйте скопіювати файли з цієї директорії в домашній каталог користувача (віртуальна робоча ОС) та на робочій стіл (клон віртуальної робочої ОС).

1. Створюємо папку в себе на комп'юторі (я створив папку й назвав її "Shared_Folder")

2. Заходимо в VirtualBox

3. Переходимо в налаштування

4. Відкриваємо вкладку Shared Folders

<img width="641" height="364" alt="image" src="https://github.com/user-attachments/assets/6725d623-d555-4d2c-8f03-c1ce3ab28d84" />

5. Натискаємо "*Add new shared folder*"

<img width="641" height="362" alt="image" src="https://github.com/user-attachments/assets/36144726-1b2d-45c5-b0f9-81607d618044" />

6. Налаштовуємо:
* Обираємо папку яку до цього створили
* Даємо будь яку назву текі
* Ставимо галочки напроти:

       Автоматичне монтування
       Make Machine-permanent

<img width="297" height="277" alt="image" src="https://github.com/user-attachments/assets/1755805c-aa42-4e57-b107-d350b5035b58" />

(Те ж саме я зробив для клона)

6. Для перевірки завантажуємо в обрану папку фото або якийсь інший файл щоб потім перенести його на віртуальні машини

Вводимо наступні команди для двох віртуальних машин:

<img width="664" height="65" alt="image" src="https://github.com/user-attachments/assets/62ce1d96-3551-4757-9c26-b023b3795aff" />

Тепер цей файл є на обох віртуальних машинах:

<img width="1919" height="1080" alt="image" src="https://github.com/user-attachments/assets/24ce30c1-fc81-4f8f-ba04-860450877763" />


4. Яким чином можна організувати обмін інформацією між вашою основною ОС (наприклад Windows) та віртуальними ОС? Скопіюйте довільний аудіо-файл з вашої основної ОС на робочий стіл віртуальної ОС та її клона. Як зробити зворотну дію, коли треба документ з робочого столу віртуальної ОС скопіювати до вашої основної робочої ОС?

Варіант 1 — Спільна папка VirtualBox

У налаштуваннях ВМ → Shared Folders → Add Folder

    Виберіть на Windows директорію (наприклад, D:\SharedFiles)
    
    У ВМ:
    
    sudo mount -t vboxsf SharedFiles ~/Desktop/
    
    
    Скопіюйте:
    
    Аудіофайл із Windows → D:\SharedFiles
    
    Він з’явиться на робочому столі ВМ.

Варіант 2 — Drag & Drop

    У налаштуваннях ВМ → General → Advanced
    
    Увімкніть:
    
    Shared Clipboard: Bidirectional
    
    Drag’n’Drop: Bidirectional
    
    Тепер можна просто перетягувати файли мишкою між вікнами Windows ↔ ВМ.

Варіант 3 — Через мережу
    
    Встановіть тип мережі: Bridged Adapter
    
    У Windows і ВМ відкрийте загальні папки через:
    
    Windows: \\192.168.x.x
    
    Linux ВМ:
    
    smbclient //192.168.x.x/Shared -U username
    
    
    Копіюйте файли в обидві сторони.

В мне виникли проблеми з іншими способами тому я переніс файл задопомогою спільної папки

<img width="799" height="674" alt="image" src="https://github.com/user-attachments/assets/a53d6fa9-22fe-43bf-b070-89936f0188e1" />


<h2>Glossary of terms</h2>


Virtual Machine (VM) — a software environment that emulates a physical computer and allows running another operating system inside the main one.

Host OS — the main operating system installed on the physical computer.

Guest OS — the operating system running inside the virtual machine.

VirtualBox — a program for creating, configuring, and managing virtual machines.

Virtual Machine Cloning — the process of creating an exact copy of an existing virtual machine with all its files and settings.

Full Clone — an independent copy of a virtual machine with its own virtual disk.

Linked Clone — a dependent copy that shares the base disk with the original virtual machine.

Virtual Machine Export — creating an OVA or OVF file for transferring or backing up a virtual machine.

Virtual Machine Import — restoring or deploying a virtual machine from an exported image.

NAT (Network Address Translation) — a network mode where the VM accesses the Internet through the host’s IP address but is not directly visible on the network.

**Bridged Adapter** — connects the VM directly to the host’s physical network, giving it its own IP address on the same subnet as the host.

Host-only Adapter — creates an isolated network between the host and the VM, without Internet access.

Internal Network — an isolated network used for communication between multiple VMs inside VirtualBox, without access to the host.

Shared Folder — a directory shared between the host and guest systems, used for file exchange.

Drag & Drop — a feature that allows dragging files between the host and the virtual machine using the mouse.

Shared Clipboard — allows copying and pasting text or objects between the host and the virtual machine.

OVF/OVA — file formats used for exporting and importing virtual machines (OVA is a single archive; OVF is a set of files).

VBox Guest Additions — a package of drivers and tools that improves integration between the host and guest OS (graphics, shared folders, clipboard, etc.).

Mounting — the process of attaching an external folder or device to the file system so it becomes accessible.

Bidirectional Mode — a mode where data transfer or clipboard sharing works both ways between the host and the VM.

IP Address — a unique identifier assigned to a device in a network, used for data exchange.

Port — a logical number that identifies a specific service or process in a network connection.

CLI (Command Line Interface) — a text-based interface used to control the system by typing commands.



<h2>Conclusion</h2>

During Work-Case №3, a clone of the virtual machine was created, network interaction between the original and the clone was configured, and Internet access was provided for both systems.
Different VirtualBox network modes (NAT, Bridged, Host-only, Internal Network) and their features were examined.
File sharing and message exchange between virtual machines and the host OS were successfully implemented.
As a result, practical skills in managing virtual environments, configuring networks, and organizing data exchange between systems were acquired.



