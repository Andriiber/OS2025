<h1>Work-Case№2</h1>

1. Встановіть на своїй домашній робочій станції гіпервізор ІІ типу – Virtual Box, VMWare Workstation, Hyper-V (або інший на Ваш вибір).
2. Опишіть набір базових дій в встановленому Вами гіпервізорі:
- Створення нової віртуальної машини;
  1. Запускаємо VirtualBox (Рис. 1)
     <p align="center"><img width="962" height="750" alt="image" src="https://github.com/user-attachments/assets/5a4cfdf9-e3fd-4329-86af-ac54ae5d9e8b" />
<p align="center">Рисунок 1 -меню VirtualBox
  
  2. Знаходимо кнопку створити в меню гіпервізора (Рис. 2)
     
     <p align="center"><img width="76" height="66" alt="image" src="https://github.com/user-attachments/assets/b573cdaf-db66-4c29-8b6d-b15efda64117" />
     <p align="center">Рисунок 2 - кнопка запустити


Вкажіть:

- Назву ВМ;

- Тип ОС (Windows, Linux, macOS тощо);

- Версію ОС.

- Задайте обсяг оперативної пам’яті.

- Створіть новий віртуальний жорсткий диск (формат VDI/VHD/VMDK, розмір і режим — фіксований чи динамічний).

- Вибір/додавання доступного для віртуальної машини обладнання;
  
- Налаштування мережі та підключення до точок Wi-Fi;
  
- Можливість роботи з зовнішніми носіями (flash-пам’ять).

<p align="center"><img width="764" height="584" alt="image" src="https://github.com/user-attachments/assets/4330a739-6e08-471a-9fa2-995cfcb01710" />
<p align="center">Рисунок 3 - створення нової віртуальної машини

Вибір/додавання обладнання:

    - У меню Settings → System можна налаштувати кількість CPU, RAM, порядок завантаження.
    
    - У Display – обсяг відеопам’яті.
    
    - У Storage – додати ISO-образ для встановлення ОС.
    
    - У USB – активувати підтримку USB (потрібно встановити VirtualBox Extension Pack).

Налаштування мережі:

    У Settings → Network можна вибрати режими:
    
        - NAT – інтернет працює "через хост".
        
        - Bridged Adapter – ВМ бачиться у тій же мережі, що і твій комп’ютер (корисно для Wi-Fi).
        
        - Підключення до Wi-Fi робиться через хостову ОС, а у ВМ воно виглядає як звичайний Ethernet.

Робота з зовнішніми носіями:

    - У меню Devices → USB → підключаєш флешку.
    
    - Якщо не працює – потрібно встановити Extension Pack та додати свій обліковий запис у групу vboxusers (на Linux-хості).
  
3. Встановіть в вашому гіпервізорі операційну систему GNU/Linux (будь-який зручний Вам дистрибутив) у базовій конфігурації з графічною оболонкою.

Виконав завантаження:

<p align="center"><img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/a56d652a-08a2-4af8-a205-0014a0a3648d" />
<p align="center">Рисунок 4 - Лінукс
   
4. Створіть другу віртуальну машину та виконайте для неї наступні дії:
   
- Встановіть у мінімальній конфігурації з термінальним вводом-виводом без графічного інтерфейсу операційну систему GNU/Linux;

      - Завантажуєш ISO-образ дистрибутиву (наприклад, Ubuntu Desktop).
      
      - У VirtualBox у налаштуваннях машини в Storage → Optical Drive додаєш цей ISO.
      
      - Запускаєш ВМ, далі йде стандартна установка Linux (вибір мови, диска, користувача)

<p align="center"><img width="1290" height="803" alt="image" src="https://github.com/user-attachments/assets/79b414c7-786b-4ebd-8c06-8d4323b44fc4" />
<p align="center">Рисунок 5 - лінукс без інткрфейса
  
- Встановіть графічну оболонку GNOME поверх встановленої в попередньому пункті ОС;

Щоб встановити графічну оболонку GNOME треба в командному рядку використати такі команди:

    Update package lists: sudo apt update
    Install a graphical shell: sudo apt install gnome
    Install a login manadger: sudo apt install lightdm
    Reboot server: sudo reboot

  <p align="center"><img width="1289" height="814" alt="image" src="https://github.com/user-attachments/assets/58d3b2f2-e154-4603-a926-fe97631d31fa" />
<p align="center">Рисунок 6 - GNOME
  
- Встановіть додатково ще другу графічну оболонку (їх можливий перелік можна знайти в лабораторній роботі №1) та порівняйте її можливості з GNOME.

<p align="center"><img width="718" height="404" alt="image" src="https://github.com/user-attachments/assets/319e4e19-7343-4de5-9545-7c0409dee3f6" />
<p align="center">Рисунок 7 - KDE Plasma




GNOME

* **Simplicity and minimalism**: main focus on an intuitive interface without overwhelming the user with settings.
* **Unified design concept**: all interface elements look consistent and follow strict guidelines.
* **Fewer customization options**: many things are set “by default” so the user doesn’t get confused.
* **Performance**: optimized for stability, but can be heavier on older PCs.
* **Window management**: relies on virtual desktops and the “Activities Overview” mode.
* **Applications**: standard set of apps (Files, Calendar, Settings) focused on simplicity.


KDE Plasma

* **High flexibility**: almost everything can be customized – panels, menus, animations, window behavior.
* **Windows-like design**: Start menu, taskbar, system tray – convenient for new users.
* **Performance**: recent versions are lightweight, use fewer resources, and run well on weaker hardware.
* **Window management**: advanced tools for arranging and managing windows.
* **KDE applications**: Dolphin (file manager), Konsole (terminal), Kate (code editor) – often more feature-rich than GNOME’s counterparts.
* **Aesthetics**: wide variety of themes, icons, and widgets.


GNOME vs KDE Plasma Comparison

| Criterion                 | GNOME                       | KDE Plasma                      |
| ------------------------- | --------------------------- | ------------------------------- |
| **Interface**             | Minimalistic, strict        | Classic, Windows-like           |
| **Customization**         | Very limited                | Extensive customization options |
| **Performance**           | Heavier on older PCs        | Lightweight, optimized          |
| **Window management**     | Focuses on virtual desktops | Flexible and powerful tools     |
| **Applications**          | Basic, simple               | Feature-rich, but more complex  |
| **Beginner-friendliness** | Easy to learn, intuitive    | Easy if familiar with Windows   |
| **Visual style**          | Unified and strict design   | Variety, widgets, themes        |

Ось перекладений на англійську **словник термінів** для цієї роботи:

---

Glossary of Terms

    * Hypervisor – software for creating and managing virtual machines.
    * Type 2 Hypervisor – a hypervisor that runs on top of the host operating system (e.g., VirtualBox, VMware Workstation).
    * Virtual Machine (VM) – a software emulation of a computer with its own OS and resources.
    * ISO image – a file containing a copy of an OS disk for installing on a VM.
    * GUI (Graphical User Interface) – an interface with windows, buttons, and menus for interacting with the OS.
    * Terminal / CLI (Command Line Interface)** – a text-based interface for entering commands in the OS.
    * GNOME – a Linux desktop environment focused on minimalism and ease of use.
    * KDE Plasma – a Linux desktop environment that offers high flexibility and interface customization.
    * RAM (Random Access Memory) – memory used for temporarily storing data currently in use.
    * Virtual Hard Disk (VHD/VDI/VMDK) – a file that emulates a hard disk for a virtual machine.
    * CPU (Central Processing Unit) – the main processing unit of a computer or VM.
    * NAT (Network Address Translation) – a network mode where the VM accesses the internet through the host.
    * Bridged Adapter – a network mode where the VM appears on the same network as the host.
    * Extension Pack – an additional VirtualBox package for USB, RDP, and other advanced features.
    * LightDM – a display/login manager for Linux desktop environments.
    * External storage – USB drives, external hard disks, and other devices that can be connected to a VM.


## Conclusion

In this practical work, I installed the VirtualBox hypervisor on my computer. First, I created the first virtual machine and installed Linux with a graphical interface. Then, I created a second virtual machine, installed Linux in a minimal configuration without a GUI, and later added GNOME. I also installed another desktop environment – KDE Plasma – and compared it with GNOME, paying attention to differences in interface and settings. During the work, I set up the network, Wi-Fi, and external storage access.
