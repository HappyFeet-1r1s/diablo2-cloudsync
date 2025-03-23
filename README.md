# diablo2-cloudsync
A hacky DIY cloud sync setup for Diablo 2 on Linux.

## Setup Instructions

1. Setup rclone for syncing to cloud storage provider (e.g. Google Drive/whatever) with an alias of e.g. "gdrive" (the alias these scripts use). Running ```rclone config``` will walk you through this.
2. Create a folder on your cloud storage provider to store save files (e.g. "/diablo2saves/")
3. Install Diablo II under Linux as usual (with Wine/Bottles/whatever).
4. Link Diablo II Saves directory to "~/diablo2saves/" in your local home directory, e.g. ```ln -s "$HOME/diablo2saves/" "$HOME/.wine/drive_c/users/$USER/Saved Games/Diablo II/"```.
5. Run ```synctolocal.sh``` to sync your save files **FROM** your cloud storage provider **TO** your local Diablo II Saves directory. (you could, for example, run ```synctolocal.sh``` *BEFORE* each run of Diablo II)
6. Run ```synctocloud.sh``` to sync your save files **FROM** your local Diablo II Saves directory **TO** your cloud storage provider. (you could, for example, run ```synctocloud.sh``` *AFTER* each run of Diablo II)
