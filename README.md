# Fsl
Local GTAO saves
FSL: local GTAO saves
 Moderator note 
FSL: local GTAO savesI take zero credit for this release. It's posted on another user's behalf so all credit goes to them. Support "as is". Please do NOT DM me about updates. That is up to the author not me.


Please make sure to remove version.dll from the game directory if it exists!

-----------------

FSL

A tool that allows you to store your online save data locally, gain infinite money, and much more!

Setup

Download the WINMM.dll file and place it in your GTA folder. Turn off BE under SC settings otherwise FSL will not load. FSL should now load automatically whenever the game starts. Remove the "_unknowncheats_ part from the DLL so it is just called "WINMM.dll".

Saves

FSL will attempt to download your actual online save file when no local saves are found. All subsequent save and load requests will be redirected to your local hard drive. This means that your save data isn’t stored in Rockstar’s servers anymore; you would use your actual online save when you disable FSL, and your local save when you enable it again

All save data files are stored in %APPDATA%/FSL. While the tool creates backups regularly, you are strongly advised to maintain your own backups in a safe location. Be aware that everything inside %APPDATA% will be wiped during a Windows reset

Money

Cheat codes can now be entered by pressing the tilde (~) key while in an online session. FSL accepts the following codes:

1M: Adds $1M 10M: Adds $10M 100M: Adds $100M 1B: Adds $1B 10B: Adds $10B


Settings

FSL now generates a configuration file at %APPDATA%\FSL when you load it for the first time. Edits to this file require a game restart to apply. Some settings might depend on others; for example, you can't enable GTA+ or use money cheat codes without enabling local saves first


API (for developers)

FSL 2+ includes an API that allows other mods to interface with it easier. Current functions include: (more will be added later)
Code:
int LawnchairGetVersion(); // gets FSL version
bool LawnchairIsProvidingLocalSaves(); // returns true if local saves are enabled
bool LawnchairIsProvidingBattlEyeBypass(); // returns true if battleye bypass is enabled
To call these functions, you have to use GetModuleHandleA to find WINMM.dll, and then use GetProcAddress and cast the result to the proper function type


Frequently asked questions

Is this safe?

This should be (nearly) undetectable since your saves never reach Rockstar’s servers. That doesn’t stop them from trying to sig this tool, so it is recommended to load a menu with a working anti-cheat bypass whenever you go online

Can I edit my saves?

There are no tools to edit save files yet. You can, however, use CodeWalker to view them

I removed FSL, and the money I added disappeared!

This is because FSL stores your online save data locally on your hard drive. Re-enable FSL to load your modded save again

Can I bypass my ban with this?

While previous versions of FSL allowed you to bypass bans and play online with cracked game copies, this is no longer possible. Clients now require a P2P certificate signed by Rockstar to attest game ownership and ban status. You might still be able to play in solo sessions if you’re banned, but this has not been tested

Can I share my save files with other people?

Yes

How can I verify if FSL is loaded?

If FSL is loaded correctly, you will see "(with FSL)" next to the online version in the legals screen. If you do not see this, FSL might be outdated or not loaded correctly