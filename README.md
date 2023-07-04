<div align="center">

   [![C++](https://img.shields.io/badge/Language-C%2B%2B-%23f34b7d.svg?style=plastic)](https://en.wikipedia.org/wiki/C%2B%2B)
   [![LOL](https://img.shields.io/badge/Game-League%20of%20Legends-445fa5.svg?style=plastic)](https://na.leagueoflegends.com)
   [![Windows](https://img.shields.io/badge/Platform-Windows-0078d7.svg?style=plastic)](https://en.wikipedia.org/wiki/Microsoft_Windows)
   [![x64](https://img.shields.io/badge/Arch-x64-red.svg?style=plastic)](https://en.wikipedia.org/wiki/X86-64)
   [![License](https://img.shields.io/github/license/R3nzTheCodeGOD/R3nzSkin.svg?style=plastic)](LICENSE)
   [![Issues](https://img.shields.io/github/issues/R3nzTheCodeGOD/R3nzSkin.svg?style=plastic)](https://github.com/R3nzTheCodeGOD/R3nzSkin/issues)
   ![Windows](https://github.com/R3nzTheCodeGOD/R3nzSkin/workflows/Windows/badge.svg?branch=main&event=push)

   # **R3nzSkin**

   ## Announcement
   I am not doing any military service unlike the original creator :D (this is a fork)

   <img src="https://user-images.githubusercontent.com/58574988/134170370-c827d712-fcc7-432f-b9f8-96678b0c9bf6.gif">

   `R3nzSkin` is internal skin changer for League of Legends.

</div>

- Change the skin of your champion, your ward, other champions, towers, minions and jungle monsters in the game.
- Automatic skins database update.
- Support for spectator mode.
- Change skins anytime and unlimited times in single game.
- Supports all Popular languages ​​in the world.
- In-game configuration with <a href="https://github.com/ocornut/imgui">ImGui</a>.
- <a href="https://github.com/nlohmann/json">JSON</a> based configuration saving & loading

# Building
   1. Clone the source with `git clone --recursive https://github.com/ISAKEM/R3nzSkin-ISAKM-fork.git`
   2. ~~Build in Visual Studio 2017/19 with configuration "Your Region - x64"~~  
	DO NOT USE VISUAL STUDIO 2017/19 IT WILL NOT WORK.  
	VS19 does not have MSVC v143 since the latest for VS19 is v142. I have not tested VS17 but since its older I can guarantee it will not work either.  
	Minimum installation to be able to build is VS22 installer -> select "Desktop development with C++" -> select these packages:  
	(or components as Microsoft like to call it)

- MSVC v143
- C++ ATL
- C++ profiling tools
- C++ CMake tools for Windows
- IntelliCode
- C++ Modules
- Windows 11 SDK (10.0.22621.0)
  
U dont actually need everything here but personally I think these are the minimum. Difference in size is minimal so its w.e.
	  

# Usage
   1. Compile source or <a href="https://github.com/ISAKEM/R3nzSkin-ISAKM-fork/releases/latest">download</a> compiled version.
   2. Use `R3nzSkin_Injector` or inject the resulting DLL into the game yourself.
      - *Administrator* privilege may be needed if failed to inject.
      - League client can crash if injected before going into arena.
         - A workaround is to not inject until you are in the arena (you will need to be fast to not disrupt the game).
   3. Press <kbd>Insert</kbd> to bring up the menu.
   4. Select skin for you, your teammates, enemies, wards.

# Further optimizations
   If your CPU supports AVX / AVX2 / AVX-512 instruction set, you can enable it in project settings. This should result in more performant code, optimized for your CPU. Currently SSE2 instructions are selected in project settings.

# Credits
   This program is an improved and updated version of the <a href="https://github.com/B3akers">B3akers</a>/<a href="https://github.com/B3akers/LeagueSkinChanger">LeagueSkinChanger</a> project.
