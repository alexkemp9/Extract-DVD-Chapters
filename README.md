# Extract-DVD-Chapters
A BASH Script to Rip Chapters from a DVD

## *Basics*
This BASH script file is designed for use by any-user (no root access required) within a Terminal. It’s principal purpose is to make it easy & reliable to rip Chapters from a DVD. It has been used under *Devuan* (a systemD-free version of *Debian*). In addition to BASH, the main utilities required are common items such as FFMPEG & MPLAYER. No attempt is made to test for existence of any requirement before use.

## *Extra*
It is a couple of years since I have used this. Try at your own discretion.

## *Begin*
The following will assume that you have created a dir `~/.local/sbin` within which you store the bash-file; this is to set the script as executable for current user only:

```bash
$ chmod 0700 ~/.local/sbin/extract-dvd-chapters
$ la ~/.local/sbin/extract-dvd-chapters
-rwx------ 1 user user 2976 Sep 10  2021 /home/user/.local/sbin/extract-dvd-chapters
```
## *Help*
Attempting to run the bare script with zero parameters shows a Help message:

```bash
$ ~/.local/sbin/extract-dvd-chapters

usage: extract-dvd-chapters DVD [TITLE] [CHAPTER_START] [CHAPTER_END]

Rips individual chapters in the given DVD title and encodes each to an x264/aac video.

   DVD              e.g. /dev/sr0 or ISO file. NOTE: don't use mounted ISO mountpoint, lsdvd doesn't like it
   TITLE            Title to rip (default 1)
   CHAPTER_START    Chapter to start with, use "-" to merge all chapters in the title to one video (default 1)
   CHAPTER_END      Chapter to end with, inclusive (default: all chapters in the title)
```
