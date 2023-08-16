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

   `R3nzSkin` is an internal skin changer for League of Legends.

</div>

- Change the skin of your champion, your ward, other champions, towers, minions, and jungle monsters in the game.
- Automatic skin database update.
- Support for spectator mode.
- Change skins anytime and unlimited times in a single game.
- Supports all popular languages ​​in the world.
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
      - League client can crash if injected before going into game.
         - A workaround is to not inject until you are in the game (you will need to be fast to not disrupt the game).
   3. Press <kbd>Insert</kbd> to bring up the menu.
   4. Select the skin for you, your teammates, enemies, and wards.

# How to run R3nzSkin on un*x/linux based systems
If u already have managed to get League installed on your un*x/linux based system then u probably already know about Lutris. Lutris makes use of a Wine feature to run .exe files in the same Wine prefix as League is running in and this is how we are going to make R3nzSkin work. To start off R3nzSkin is just a simple .dll injection at its core so any .dll injector will work. Atleast thats the case on Windows, I have tried many .dll injectors on Arch Linux (yes I use Arch btw blablabla funny meme) and only actually found one that works so we will be using that one.
<a href="https://github.com/andrewbae/windows-dll-injector">

Now to use this we just click the triangle button besides the wine icon in Lutris and click "Run EXE inside Wine prefix". 
Then choose the dllRifle-x64.exe. 
In dllRifle we choose "League of Legends.exe" as our "Victim process"
Then for our "Payload Dll" we choose "R3nzSkin.dll"

Remember this has to be done in the loading screen or when u are already ingame since League actually needs to be running its not automatic like the R3nzSkin Injector that only targets this one process and sits and waits for it to start.

Now, we can make this even simpler so that we dont have to click "Run EXE inside Wine prefix" every time having to go thru all that. So what we are going to do is to make a seperate Lutris entry and add dllRifle as a game running under the same prefix as League.

So to do this we click the plus at the top left in Lutris then click "Add locally installed game"
Here u can choose anything for the name, then we pick "dllRifle-x64.exe" for our executable.
Then the only thing that matters for the rest is that u choose the same directory for "Wine prefix" as League. Its 
usually "~/Games/league-of-legends".

I have the same settings as league for the rest but honestly I dont think any of that matters it will just work anyways. Just click save when u are done.
Now u can right click your new "game" and click "Create Desktop shortcut" aswell as "Create application menu shortcut".

Now if u are running a desktop enviroment with icons u can now launch dllRifle straight from there and have it run in the same prefix as League right away. If u are not running a desktop enviroment with icons or u are running a tiling window manager or anything that does not have icons, then u can still just launch it directly from Lutris or in my case I just add the desktop entry to my dock (Plank). Really any way u have of launching desktop entries and u can launch it directly.

# Further optimizations
   If your CPU supports AVX / AVX2 / AVX-512 instruction set, you can enable it in project settings. This should result in more performant code, optimized for your CPU. Currently SSE2 instructions are selected in project settings.

# Credits
   This program is an improved and updated version of the <a href="https://github.com/B3akers">B3akers</a>/<a href="https://github.com/B3akers/LeagueSkinChanger">LeagueSkinChanger</a> project.
