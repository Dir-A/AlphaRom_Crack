# AlphaRom_Crack
a project to show how to crack a alpharom protected game

## Quick Start
check [test/quick-start](https://github.com/Dir-A/AlphaRom_Crack/tree/main/test/quick-start)

## How AlphaRom works？
first we need to know the game that protected by alpharom uses themida protection, at game's exe startup use winapi VirtualAlloc to allocate memory used to load a dll from memory instead of loading from dll file, and this dll named sarcheck.dll. alpharom's validation algorithm is placed in sarcheck.dll, so alpharom is actually a dll named sarcheck.dll, the reason why we don't see sarcheck.dll file in game directory is because it's using themida to bind the dll in to game's exe and load this dll at startup from memory.  
So if we can prevent the loading of sarcheck.dll we can bypass alpharom，or just modify the dll to disable alpharom's checker.
 
## Guide to remove Alpharom from executable:
Run game.exe with compiled `version.dll`, then use [Magicmida](https://github.com/Hendi48/Magicmida) to unpack the execuatable.
[Example video](https://mega.nz/file/euwWFLpZ#N_3AtnjEzjuPy3hhaLHr-Xg7B0FvHBoNWsatX1lz7_k)
+ Optional: You can shrink the executable back to smaller size after unpacking.

## Tested games:
+ パサージュ！ ～passage of life～
+ Kajiri Kamui Kagura Akebono no Hikari
+ Aonatsu Line
