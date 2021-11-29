# FFXIV-Crafting-Helper
AHK script for automating crafting tasks in FFXIV

![Example Crafting Helper Screenshot](https://user-images.githubusercontent.com/2283362/143943992-7d27c13d-18df-478e-bdbc-7dd46c828ddf.jpg)

## FFXIV Crafting.ahk
The main script. Requires AutoHotKey installed. Run the script then press ctrl+f12 to "start" (show UI).

Select the craft from the drop down, insert how many iterations you would like it to run for (0 means run until stopped), and click Craft
Pause - Pauses execution of the script immediately. Click again to unpause
Stop - Returns the script to an idle state after finishing the current craft
Run Simulation - Simulates the selected craft for testing. Will popup a message box with the craft data. Will also output hotkeys to Notepad.exe if it is running instead of the FFXIV client.
Reload Crafts - Reloads the crafts.json file. Useful for changing data without having to reload the script

## crafts.json
JSON file which contains crafting data

Example JSON:
This will add an item to the scripts dropdown named "3.5* 70D". When executed it will press hotkey 7 in FFXIV, wait 39s, then press 8 in FFXIV and wait 11s.
```
{
	"3.5* 70D": {
		"macros": [
			{
				"hotkey": "7",
				"duration": 39
			},
			{
				"hotkey": "8",
				"duration": 11
			}
		]
	}
}
```
