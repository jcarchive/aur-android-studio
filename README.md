# AUR package for Android Studio
This repos contains an Arch User Repository package for flutter following the next standard for the installation:

1. App files directory: `/usr/share/studio`
2. Executable `studio` directory: `/usr/share/bin/studio`
3. .desktop file directory: `/usr/share/applications`

* The executable in `/usr/share/bin` is installed as symbolic link to the `studio` bin inside the app files.

## * Notes
This package may differ from the "official" in the AUR repository in the directories used for the installation and the steps used. The purpose of this package and others 
ones in this account is for install all the programs that I used following certains standard (ie. using `/usr/share/{pkgname}` for app files and `/usr/share/bin/{execname}`
for executable) and in some cases clean the installation steps from some bloat.