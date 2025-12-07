# Tray Icon Power Plan Switcher App

A lightweight Windows tray application to switch between power plans instantly (usefull for laptops+docking stations) and tweak detailed per-plan settings (buttons, lid, display, and sleep timeouts).  
Includes **bilingual UI** (English / Español) and **theme-aware icons** for light/dark Windows modes.

---

## ⭐ Key Features

- Runs quietly in the **system tray**
- Lets you assign up to **4 power plan slots**:
  - **A** – Desktop icon  
  - **B** – Laptop icon  
  - **C** – Bolt icon  
  - **D** – Moon icon  
- **Left-click** the tray icon to cycle through assigned plans
- **Right-click** to open full settings and configuration
- Uses the **Windows PowrProf API directly** (no `powercfg.exe` calls)
- **Bilingual UI:** English / Español (MX)
- **Theme-aware icons:** Light/Dark variants adjust automatically to the Windows theme

---

## 🔌 Power Plan Slots

- Enumerates all existing Windows power plans using `powrprof.dll`
- Any plan can be assigned to slot A/B/C/D
- Switching plans updates the tray icon instantly
- Cycles only through assigned slots (1–4 plans depending on configuration)

---

## 🎛 Buttons & Lid Configuration (Per-Plan)

For each power plan, you can edit behaviors for:

- **Power button action**
- **Sleep button action**
- **Lid close action**

Each action can be set separately for:

- **On AC power**
- **On battery**

Available actions:

- Do nothing  
- Sleep  
- Hibernate  
- Shut down  

These settings map directly to the real Windows system power options.

---

## 🌙 Display & Sleep Timeouts (Per-Plan)

Independently for **AC** and **battery**, you can set:

- Display off timeout  
- Console lock display off timeout  
- Sleep after  
- Hibernate after  
- Unattended sleep timeout  

Timeout options include:

- Preset values: **1, 2, 3, 5, 10, 15, 20, 30, 60, 120 minutes**
- **Custom timeout** in minutes (0 = Never)

All changes apply instantly to the selected plan.

---

## 🌐 Language Support

- The UI can be switched manually between:
  - **English**
  - **Español**
- Language preference is saved to:

```

%APPDATA%\SwitchPowerTray\config.txt

```

On the first run, the app automatically detects your Windows UI language.

---

## 🎨 Icon & Theme Handling

The app includes embedded icons in light/dark variants for:

- Desktop  
- Laptop  
- Bolt  
- Moon  

Behavior:

- If Windows is in **light mode**, the app uses **dark icons** (higher contrast)
- If Windows is in **dark mode**, the app uses **light icons**
- Optionally, you can force:
  - **Auto**
  - **Light icons**
  - **Dark icons**

---

## 📂 Configuration Files

User configuration is stored in:

```

%APPDATA%\SwitchPowerTray\config.txt

```

This file keeps:

- Assigned power plan GUIDs (slots A/B/C/D)  
- Icon theme preference  
- Selected language  

A temporary log file is created at:

```

%TEMP%\SwitchPowerTray.log

```

---

# 🟦 Auto-Start the Application (Optional)

You can configure the application to run automatically each time Windows starts.

Choose one of the following options depending on whether you want auto-start for **all users** or **only your user account**.

---

## ▶ Auto-Start for ALL Users  
*(recommended if the PC is shared)*

Place the executable **or a shortcut to it** in the system-wide Startup folder:

```

C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup

```

✔ Automatically runs for **every user account**  
✔ Does not require reconfiguration per-user  
⚠ Requires administrator permissions  

---

## ▶ Auto-Start for Current User Only

Place a shortcut in your personal Startup folder:

```

%APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup

```

✔ Runs only when *your* user logs in  
✔ Does not require administrator rights  

---

### Notes

- The application runs silently from the **system tray**
- It uses negligible CPU and memory when idle
- Fully compatible with Windows 10 and Windows 11

---

## 📄 License

This project is licensed under the **MIT License**.  
See the included `LICENSE` file for details.

## 🙌 Contributions & Feedback

Feel free to open issues or submit pull requests!  
Suggestions, improvements, and feature requests are welcome.
