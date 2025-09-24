<h1>Work-Case№2</h1>
1. Встановіть на своїй домашній робочій станції гіпервізор ІІ типу – Virtual Box, VMWare Workstation, Hyper-V (або інший на Ваш вибір).

2. Опишіть набір базових дій в встановленому Вами гіпервізорі:

**1. Створення нової віртуальної машини**

- Запустіть Oracle VM VirtualBox.

- У головному меню натисніть Machine → New (або кнопку New).

**Вкажіть:**

- Назву ВМ;

- Тип ОС (Windows, Linux, macOS тощо);

- Версію ОС.

- Задайте обсяг оперативної пам’яті.

- Створіть новий віртуальний жорсткий диск (формат VDI/VHD/VMDK, розмір і режим — фіксований чи динамічний).

**2. Вибір/додавання обладнання для ВМ**

У налаштуваннях (Settings) обраної машини можна:

- Система (System) → задати кількість процесорів, обсяг RAM, порядок завантаження.

- Дисплей (Display) → обсяг відеопам’яті, 3D/2D прискорення.

- Носії (Storage) → додати ISO-образ, жорсткі диски.

- Аудіо (Audio) → увімкнути/вимкнути звуковий адаптер.

- USB → підключати USB-пристрої (флешки, периферію).

- Спільні папки (Shared Folders) → підключати каталоги з хост-системи.

**3. Налаштування мережі та підключення до Wi-Fi**

 У Settings → Network є режими:

- NAT – ВМ використовує інтернет через хост (простий доступ до мережі).

- Bridged Adapter – ВМ підключається як окремий пристрій у локальній мережі, у тому числі до Wi-Fi.

- Host-Only Adapter – тільки зв’язок між хостом і ВМ.

- Internal Network – мережа лише між ВМ.

**4. Робота з зовнішніми носіями (flash-пам’ять)**

- У меню Devices → USB можна підключити флешку до ВМ (попередньо додавши її в USB Filters у налаштуваннях).

- Також можна монтувати ISO-образи дисків через Storage.

- Для обміну файлами між хостом і ВМ зручно використовувати Shared Folders або Drag&Drop / Clipboard sharing (якщо встановлені Guest Additions).

3. Встановіть в вашому гіпервізорі операційну систему GNU/Linux (будь-який зручний Вам дистрибутив) у базовій конфігурації з графічною оболонкою.
   
   Щоб встановити ОС на гіпервізор треба:
   
<p align="center"><img width="923" height="568" alt="Снимок экрана 2025-09-24 в 12 45 37" src="https://github.com/user-attachments/assets/b72d960c-2918-41a9-abc3-eee3016121bb" /></p>
<p align="center">Створюємо нову ВР</p>
<p align="center"><img width="952" height="670" alt="Снимок экрана 2025-09-24 в 12 47 15" src="https://github.com/user-attachments/assets/f2502187-8312-4ee9-b9a2-b4afca11a5a4" /></p>
<p align="center">Вводимо початкові дані</p>
<p align="center"><img width="777" height="108" alt="Снимок экрана 2025-09-24 в 13 05 18" src="https://github.com/user-attachments/assets/6479aa2b-9b59-4cc9-aee5-c7ed439a1bc4" /></p>
<p align="center">Встановлюємо розмір ОЗУ</p>
<p align="center"><img width="705" height="310" alt="Снимок экрана 2025-09-24 в 13 15 49" src="https://github.com/user-attachments/assets/8fccd8cc-d870-4a3a-bb7e-345b09a7cc47" /></p>
<p align="center">Встановлюємо розмір HD та натискаємо "Закінчити"</p>
<p align="center"><img width="1435" height="743" alt="Снимок экрана 2025-09-24 в 12 44 36" src="https://github.com/user-attachments/assets/3caaa713-35ff-4e08-98c4-01a68acf0b5b" /></p>
<p align="center">Далі на офіційному сайті Лінукс треба завантажити ISO образ Ubuntu</p>
- Після того як завантажив образ з сайту, повертаємось в VirtualBox  
<p align="center"><img width="920" height="564" alt="Снимок экрана 2025-09-24 в 15 19 40" src="https://github.com/user-attachments/assets/16091527-8833-4386-9c67-ea25f425a08d" /></p>
<p align="center"><img width="1258" height="575" alt="Снимок экрана 2025-09-24 в 15 24 33" src="https://github.com/user-attachments/assets/a241a24f-d252-4e8c-9474-f764450276f8" /></p>
<p align="center">Після завантаження образу натискаємо ОК</p>
- Далі запускаємо віртуальну машину
<p align="center"><img width="915" height="563" alt="Снимок экрана 2025-09-24 в 15 40 21" src="https://github.com/user-attachments/assets/8c0ef229-3af0-4e18-9ff8-7856a6b52869" /></p>
- Після запуску у мене почалась процедура встановлення Linux Ubuntu, я пройшов регестрацію та встановив оновлення і на виході в мене вийшов повноцінний робочий Лінук у віртуальній машині.
<p align="center"><img width="1280" height="797" alt="image" src="https://github.com/user-attachments/assets/3640dd2c-f776-423c-b57b-f1a69869c86a" /></p>
<p align="center">Робочий стіл Лінукс</p>

4. Створіть другу віртуальну машину та виконайте для неї наступні дії:
   
- Встановіть у мінімальній конфігурації з термінальним вводом-виводом без графічного інтерфейсу операційну систему GNU/Linux;
  
 - Щоб встановити Лінукс у мінімальній конфігурації треба:
 1. Скачати с офіційного сайту Лінукс, версію server, для того щоб встановити тільки командний рядок;
 2. Завантажити цю версію в VisualBox;
 3. Запустити ВМ;
 4. Пройти реєстрацію, встановити пароль, імя, логін;
 5. Тепер ми потрапили в Термінал.
   <p align="center"> <img width="1281" height="800" alt="image" src="https://github.com/user-attachments/assets/22b4f02b-6b19-4e2a-a154-99b647c570b9" /> </p>

     
- Встановіть графічну оболонку GNOME поверх встановленої в попередньому пункті ОС;
  
  Щоб встановити графічну оболонку GNOME треба в командному рядку використати такі команди:
  
  1. Update package lists: ``` sudo apt update ```
  2. Install a graphical shell: ``` sudo apt install gnome ```
  3. Install a login manadger: ``` sudo apt install lightdm ```
  4. Reboot server: ``` sudo reboot ```
   <p align="center">   <img width="1280" height="807" alt="image" src="https://github.com/user-attachments/assets/c359128f-92de-481b-ae23-e6dd0ae9ca50" /> </p>
    <p align="center">Встановленна графічна оболонка GNOME за допомогою командного рядка</p>

- Встановіть додатково ще другу графічну оболонку (їх можливий перелік можна знайти в лабораторній роботі №1) та порівняйте її можливості з GNOME.
  
  Другу оболонку я вибрав XFCE, щоб її встановити я ввів наступні команди:
  
  1. Install a graphical shell: ``` sudo apt install xfce4 ```
  2. Install a login manadger: ``` sudo apt install lightdm ```
  3. Reboot server: ``` sudo reboot ```
        <p align="center"><img width="1287" height="811" alt="image" src="https://github.com/user-attachments/assets/9bdc1b4c-5776-4399-921f-90838fdb3899" /></p>
           <p align="center"> Встановленна графічна оболонка XFCE за допомогою командного рядка</p>
Порівняння графічних оболонок:
# Comparison of Linux Desktop Environments: GNOME vs Xfce

Below is a comparison of two popular Linux desktop environments (DEs) — **GNOME** and **Xfce** — with pros and cons for each. This may help if you’re deciding which one to use.

---

## What are GNOME and Xfce?

| DE | Description |
|----|-------------|
| **GNOME** | A free desktop environment developed by the GNOME Project. Based on GTK, with a modern interface, strong focus on design, usability, and accessibility. |
| **Xfce** | A lightweight desktop environment, also built on GTK. Focused on low resource consumption, modularity, customizability, and simplicity. |

---

## Comparative Characteristics

| Aspect | GNOME | Xfce |
|--------|-------|------|
| **Resource Usage** | Higher RAM and CPU usage. Includes animations, modern interface, and effects which increase demand. | Lightweight — runs faster on older or weaker hardware. Minimal animations, simpler interface. |
| **Interface & UX** | Modern, minimalist, beginner-friendly. Focused on simplicity and reducing advanced settings. Includes *Activities Overview* and integrated search. | Classic desktop layout with panels, icons, and more flexible workspace design. User can tweak nearly everything. |
| **Customization & Flexibility** | Offers extensions and themes, but users are often limited to what the project provides. Some tweaks require extensions or additional tools. | Highly customizable: panels, menus, shortcuts, themes, plugins. Modular design allows removing unneeded components. |
| **Appearance / Modernity** | Very modern look, smooth animations, Wayland support, HiDPI-friendly, polished UI/UX. | More traditional and restrained design. Effects are minimal or absent. |
| **Hardware Support (Old / Weak PCs)** | Heavier for older machines with limited RAM or weak GPUs. Requires disabling effects for smoother performance. | Excellent for older computers or low-resource devices — fast and responsive. |
| **User Experience (Workflows)** | Emphasis on smooth out-of-the-box user experience, accessibility, and system integration. | Requires more manual tweaking to achieve desired workflow. Out-of-the-box setup is simpler but less feature-rich. |
| **Community & Adoption** | Very widespread, default DE in many distributions (Ubuntu, Fedora, Debian, etc.). | Popular in lightweight distros (Xubuntu, Manjaro Xfce, MX Linux, etc.). |

---

## Plus and Minuses

### GNOME

**+:**
- Modern, polished interface, user-friendly for beginners.  
- Many features out-of-the-box: search, virtual desktops, accessibility, integration.  
- Supports new technologies: Wayland, HiDPI, gestures, smooth animations.  

**-:**
- Higher demand on RAM, CPU, and GPU.  
- Less flexibility without installing extensions.  
- Extensions can break after updates.  

---

### Xfce

**+:**
- Lightweight and fast on old or weak hardware.  
- High customizability: panels, plugins, menus, themes, shortcuts.  
- Very stable and reliable.  

**-:**
- Simpler visuals; may feel less “modern.”  
- Some GNOME features require manual setup or may be missing.  
- Less focus on modern UX trends (gestures, HiDPI polish).  

---

## When to Choose Which?

- **Choose GNOME** if you have a modern PC/laptop and value convenience, modern design, virtual desktops, integration, and want most features ready to use “out-of-the-box.”  

- **Choose Xfce** if you want maximum performance on older or resource-limited machines, or if you prefer a highly customizable, classic desktop environment that you can tweak to your liking.  

---
## Conclusion

During this work, a Type II hypervisor (VirtualBox) was installed, which made it possible to create and configure virtual machines for different purposes. We practiced the basic functions of the hypervisor: creating new virtual machines, adding hardware, configuring the network (including Wi-Fi connection), and connecting external storage devices.

On the first virtual machine, the GNU/Linux operating system was installed with a graphical desktop environment, which provides user-friendly interaction even for beginners. The second virtual machine was deployed in a minimal configuration with terminal access only, after which the GNOME desktop environment was installed, along with an additional environment (XFCE).

The comparison between GNOME and XFCE showed that GNOME focuses on a modern interface and usability, but requires more system resources. XFCE, on the other hand, proved to be lightweight and fast, making it an optimal choice for less powerful machines, though its interface is less modern.

Thus, during this work we consolidated skills of working with the VirtualBox hypervisor, learned the peculiarities of Linux installation in different configurations, and gained practical experience with multiple desktop environments, which allowed us to compare their advantages and disadvantages.
