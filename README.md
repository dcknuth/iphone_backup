# Backing up Photos and Video from the iPhone
How to backup an iPhone's pictures to a PC

First, go into the phone settings and then photo settings. You should turn all the places possible to "Save original format". Then use a standard lightning cable to plug the phone into the PC and allow the PC access to the phone on the phone via the pop-up that occurs when you plug it in. If you don’t do these two things in order, you may get random errors while copying and Windows will say "An error occurred", but nothing more helpful.

Next, you should be able to just open both the phone and the place you want to put the backup copy with Windows File Explorer. Drag and drop everything over you want to backup to the PC. Since we said to save the original file format in the last step, we avoided errors, but now have some Apple file formats to deal with. The main problem is the .heic format files as Windows does not have a decoder for these out-of-the-box. Image Magic will convert these fine to jpeg or png for you. If space is not an issue, you can convert to jpeg, but leave the heic originals in case you want to try to do a better conversion later or if it is an image sequence file and you want to choose a different one. This command will do that for all the heic files in a directory:
```
magick mogrify -format jpg *.HEIC
```
It will take some time if there are a lot of images.