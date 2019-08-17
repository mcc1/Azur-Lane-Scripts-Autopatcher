# Azur-Lane-Scripts-Autopatcher
Automated tool that will help you to save your precious time when modifying Azur Lane scripts.

## System Requirements
1. NET Framework 4.5.1 or newer https://www.microsoft.com/en-us/download/details.aspx?id=40779
2. Python 3.7.0 with "Add Python 3.7 to PATH" option enabled https://www.python.org/ftp/python/3.7.0/python-3.7.0.exe
3. (Skip if "Add Python 3.7 to PATH" option is enabled) Added Python's directory into System Environment Variables named **Path** https://docs.python.org/3/using/windows.html#configuring-python)

## Download
You must be new to the internet if you don't even know where to get the binary. Listen here you dipshit, do me a favor by fucking fuck yourself and begone from this github at once.

I've had enough of spoonfeeding a fucking brainlet who couldn't even find the solution by themself.

## How to Use
Open `Azurlane.exe` and import *Azur Lane AssetBundle file* named **scripts**

You can obtain Azur Lane AssetBundle file named scripts from:
  - Japan: Android/data/com.YoStarJP.AzurLane/files/AssetBundles
  - China (bilibili): Android/data/com.bilibili.azurlane/files/AssetBundles
  - Korean: Android/data/com.txwy.and.blhx/files/AssetBundles

## Known Issues
### System Locale
AssetBundle extractor (UnityEx.exe) will not working properly when your System Locale is not English.

### Game Stuck onload
This issue will only happens if you're playing China (bilibili) version of the game, simply do the following step to fix this issue.

Use DnSpy to import game's dll file named Assembly-CSharp.dll, then search LuaScriptMgr and edit a method named Load(Action) and remove lines shown in the picture (see below).

![DnSpy](https://a.safe.moe/OQevw5S.png)

# Original repo
https://github.com/jmk5544/Azurlane-scripts-autopatcher

# Original readme
# Azurlane-scripts-autopatcher
A tool to automatically modify *Azurlane scripts* and generate several modified scripts, a.k.a *modded scripts* to obtain unfair gameplay.

## Download
You can grab the binary from the [releases page](https://github.com/k0np4ku/Azurlane-scripts-autopatcher/releases), also take a look at [Azurlane-LuaHelper](https://github.com/k0np4ku/Azurlane-LuaHelper) if you want to do it **manually**.

## Requirements
1. Python 3.0 or newer
2. NET Framework 3.5 or newer

## Usage and Examples
Open `Azurlane.exe` and select *Azurlane AssetBundle* file named **scripts**, or by command `Azurlane.exe <path-to-scripts>`

You can obtain Azurlane AssetBundle file named scripts from:
- Japan: Android/data/com.YoStarJP.AzurLane/files/AssetBundles
- China (bilibili): Android/data/com.bilibili.azurlane/files/AssetBundles
- Korean: Android/data/com.txwy.and.blhx/files/AssetBundles

### Examples
```
$ azurlane scripts-jp
[+] Copying AssetBundle to temp workspace...<done>
[+] Decrypting and Unpacking AssetBundle...<done>
[+] Decrypting and Decompiling Lua...1/3...2/3...3/3...<done>
[+] Cloning Lua and AssetBundle...1/6...2/6...3/6...4/6...5/6...6/6...<done>
[+] Rewriting Lua...1/6...2/6...3/6...4/6...5/6...6/6...<done>
[+] Recompiling and Encypting Lua...1/6...2/6...3/6...4/6...5/6...6/6...<done>
[+] Repacking and Encrypting AssetBundle...1/6...2/6...3/6...4/6...5/6...6/6...<done>
[+] Copying all modified AssetBundle to original location...1/6...2/6...3/6...4/6...5/6...6/6...<done>
[+] Cleaning...

Everything is ok, we're done.
Press any key to exit.
```
