### Download and install from the [Visual Studio Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/)
Run Installer: Open the installer and select the following workload:
- Desktop development with C++
### Check Individual Components: On the right-hand side (or in the "Individual components" tab), ensure these are checked:
- MSVC v143 - VS 2022 C++ x64/x86 build tools (Latest)
- Windows 10 SDK (or Windows 11 SDK)
- C++ CMake tools for Windows

### Click Start and search for "x64 Native Tools Command Prompt for VS 2022". Run it as Administrator.
### Prevents your PC from running out of RAM during the long compile
set MAX_JOBS=2
### Tells Python to use the installed Build Tools
set DISTUTILS_USE_SDK=1
set FLASH_ATTENTION_FORCE_BUILD=TRUE
### NVIDIA's CUDA compiler (nvcc) currently only recognizes up to Visual Studio 2022. If using newer versions such as Visual Studio 2025 (v18)
set NVCC_APPEND_FLAGS=--allow-unsupported-compiler

pip install flash-attn --no-build-isolation
