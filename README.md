# en-HU-keyboard-layout - Hungarian English Keyboard Layout

MacOS Installation:
---

The keyboard layout is created by  Ukelele 3.2.7 on MacOS High Sierra 10.13.1. It was tested and works with macOS 10.14.6 too.

0. Optional: If you modify the keyboard make sure it has a different version and name than the previous.

1. Remove keyboard layout(Input Source) using Keyboard Preferences.

2. Delete previous version of keyboard layout. 

sudo rm -rf /Library/Keyboard\ Layouts/en-HU.bundle

3. Reboot

4. Install keyboard layout from dmg file (Drag and Drop)

5. Reboot

6. Add keyboard layout using Keyboard Preferences.

Windows Installation:
---

The layout is defined by the Microsoft Keyboard Layout Creator 1.4 on Windows 10 Pro 1709 16299.19

1. Unselect the old version of the Keyboard Layout on the Language Bar if active and then uninstall the old version.

2. Reboot

3. Install new version.

4. In Settings / Region & language modify the options for the installed Languages and add the new keyboard. The old keyboard can be removed.

5. Open Control Panel\Clock, Language and Region\Language and select Advanced settings. Select the appropriate language from the list. Click on "Apply language settings to the welcome screen..." Select Copy Settings and check Welcome screen and New user accounts. Finally click OK.
If this is the only keyboard and language remaining then this step hides the "ENG", "HUN" and any other language icons in the notification area.

Linux Installation:
---

Everything is installed manually on Ubuntu 16.04.3 LTS. Instead of creating a new keyboard layout I have decided to customize the existing basic US layout to my needs.

1.) Add the contents of Compose.txt to

/usr/share/X11/locale/en_US.UTF-8/Compose

2.) Remove all lines containg dead_grave from Compose.txt. Maybe a bit overkill but this ensures that my grave accents never collide with official accents.

3.) Add the following line to

/usr/share/X11/xkb/symbols/us

    key <LSGT> {	[ dead_grave	]	};

4.) Select the English(US) layout.

5.) Reboot

Design:
---

I switch between MacOS, Windows and Linux multiple times a day. I also often type characters with accents and I like to use keyboard shortcuts very much.

I rarely have problem with keyboard shortcuts but sometimes I find a shortcut which cannot be pressed on an international keyboard layout. I believe the reason is that the shortcut was designed with the us keyboard in mind. Most application lets you change the shortcuts but it can be time consuming. When reinstalling the OS I would have to reconfigure every application. To make the configuration easier I decided to create a unified keyboard layout.

I wanted to have a consistent keyboard layout which can be used the same way no matter what operating system I use. For these reasons I have decided to create my own layout.

The Design Concept of the new Layout:

1.) It must work on international keyboards only. International keyboards have an
extra button compared to the ANSI keyboard which is used in the US. Since it is an 
additional button it is not usually used by keyboard shortcuts. So we can change it to anything
we want. 

2.) It must provide shortcuts for Hungarian accents I need no other accents.

3.) It must work on multiple operating systems: Linux, Windows, Mac.

4.) I want my keyboard to be as symmetrical as possible. So right modifier keys(alt, ctrl, shift and command) must do the same thing as their left modifier counterparts.

The basic us layout is:

|       |    |    |    |    |    |    |    |    |    |    |       |    |
|----   |----|----|----|----|----|----|----|----|----|----|----   |----|
| `~    | 1! | 2@ | 3# | 4$ | 5% | 6^ | 7& | 8* | 9( | 0) | -_    | =+ | 
| qQ    | wW | eE | rR | tT | yY | uU | iI | oO | pP | [{ | ]}    |
| aA    | sS | dD | fF | gG | hH | jJ | kK | lL | ;: | '" | \\ \| |
| \\ \| | zZ | xX | cC | vV | bB | nN | mM | ,< | .> | /? |

The second backslash button is changed to a dead key which provides the hungarian accents:

|     |    |    |    |    |    |    |    |    |    |    |     |    |
|---- |----|----|----|----|----|----|----|----|----|----|---- |----|
| `~  |    |    |    |    |    |    |    |    |    |    |     |    | 
|     |    | éÉ |    |    |    | úÚ | íÍ | óÓ |    |    |     |
| áÁ  |    |    |    |    |    | üÜ |    | öÖ |    |    |     |
|     |    |    |    |    |    | űŰ |    | őŐ |    |    |

Only normal and shift codes are shown on the diagramms above. Right alt key is not used because it is a windows only concept. Alt-and button press combinations to enter accents are not used either because it is a Mac only concept, these combinations are menu shortcuts in Windows.
