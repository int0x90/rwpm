# RWPM - Read/Write 64bit process memory on Linux. 
##### Super simple CLI program written in C++ that enables you to manipulate another processes memory address space.

# Want something similar on Windows?
##### You can replicate this program very easily with the help of WinAPI.
##### Links to documentation of the functions used:
- [OpenProcess](https://docs.microsoft.com/en-us/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess "OpenProcess")
 
```cpp
#include <windows.h> // Remember to include this, it gives us access to the Windows API.

int main(){

  HWND handle_window = FindWindowA("Window class", "Window name"); // Get a handle to our target process by it's window name.
  DWORD pid;
  GetWindowThreadProcessId(handle_window, &pid); // Get processID from the window and store it in $pid;
  HANDLE open_proc = OpenProcess(PROCESS_ALL_ACCESS, FALSE, pid); // Open our target process with maximum priviliges.
  
  // We're now ready to start reading/writing.
  
  return 0;
}

```
