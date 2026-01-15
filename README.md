# C++ Universal DLL Injector Base

A clean, lightweight, and modular C++ implementation of a Windows DLL injector. This project serves as a robust template for **LoadLibrary-based injection**, designed to be easily adapted for any 64-bit process and DLL.



## 🛠 Overview

This utility automates the process of injecting a dynamic-link library into a target process. While originally developed for the [Vampire-Survivors-X](https://github.com/KingsleydotDev/Vampire-Survivors-X) project, the codebase is generalized to work with any Windows executable.

### Core Logic
* **Process Enumeration:** Uses `CreateToolhelp32Snapshot` to find the target Process ID (PID) without requiring manual user input.
* **Dynamic Pathing:** Automatically resolves the absolute path of the DLL based on the injector's location.
* **Remote Thread Injection:** Uses the standard Windows API pattern: `OpenProcess` -> `VirtualAllocEx` -> `WriteProcessMemory` -> `CreateRemoteThread`.

---

## ⚙️ Configuration

The code is designed for easy modification. To target a different application, simply update these values in `main()`:

ai ahh readme btw. i aint even read this.
is this code the best? no. Does it do what it say on the tin? yes.

```cpp
// Update these to match your specific target
const char* targetDllName = "YourLibrary.dll"; 
const wchar_t* targetProcess = L"TargetApp.exe";

