# How To Build With Unity PS4 8.00
A slightly modified version of the original guide. For the most part, follow along with this guide if you have version 8.00 rather than 4.50 of the S*D*K.

Setup
=====

1.- Install PS4 S*D*K. There are a lot of versions, look for 8.008.

2.- Install Unity 2021.2.0b11.

3.- Install Unity PS4 2021.2.0b11 for the same release as Unity 2021 release.

4.- You can also install Monodevelop from the preferences menu option within Unity Editor. You can, anyway, install Visual Studio as IDE.

5.- Use unihacker to patch the Unity Hub and Unity installation after installing or PS4 target won't appear in Build Settings.

6.- Download Fake PKG tools here: "https://github.com/CyB1K/PS4-Fake-PKG-Tools-3.87/releases" (7.0 at time of writing) and copy/replace it in "SCE_PATH/ORBIS/Tools/Publishing Tools/bin"

Building
========

1.- Create a new project, or open an existing one.

2.- When you're ready to build the project select File -> Build Settings.

3.- Set the settings in the window as show in this image.


![PC Hosted](https://github.com/RetroGamer74/HowToBuildWithUnityPS4FakePKG/blob/master/Captura1.PNG "Set PC Hosted")

4.- Now click in Player Settings button on the bottom left side of the Build Settings window.

![Other Settings](https://github.com/RetroGamer74/HowToBuildWithUnityPS4FakePKG/blob/master/Captura3.PNG "Other Settings")

5.- Usually the environment variables of the S*D*K are set in the system, and Unity does not require you set the S*D*K path, but I prefer to set it.

6.- Now press build Button. Take in mind, this build won't work. We do this build to retrieve 2 files we need for the final build. So in the File Dialog, create a new folder out of the project and set it a name. For example Build. And then select the folder and continue.

![Open Dialog](https://github.com/RetroGamer74/HowToBuildWithUnityPS4FakePKG/blob/master/Captura5.PNG "Open Dialog")

7.- When the built is complete browse the folder Build or the name you set and go to the sce_sys folder.

![Build Folder](https://github.com/RetroGamer74/HowToBuildWithUnityPS4FakePKG/blob/master/Captura6.PNG "Build Folder")

8.- Copy these two files from sce_sys folder.

![Build Folder](https://github.com/gamecoreSRC/HowToBuildWithUnityPS4800FakePKG/blob/master/image_2025-08-09_014511621.png "Build Folder")

9.- Paste the files into the root project folder

![Build Folder](https://github.com/gamecoreSRC/HowToBuildWithUnityPS4800FakePKG/blob/master/image_2025-08-09_014645480.png "Build Folder")

But we still need the shareparam.json file - in later S*D*K versions (or at least for Unity's case from my experience), it isn't automatically generated, so you will need to create it manually.

10.- Navigate to where your S*D*K is installed, and go to "ORBIS > Tools > Publishing Tools > bin". You should see something similar to this image.

![Publishing Tools](https://github.com/gamecoreSRC/HowToBuildWithUnityPS4800FakePKG/blob/master/image_2025-08-09_015015867.png "Publishing Tools")

11.- Open "Share_File_Editor.exe" you should see this window open up. You don't need to change any of the settings here.

![Publishing Settings](https://github.com/gamecoreSRC/HowToBuildWithUnityPS4800FakePKG/blob/master/image_2025-08-09_015148470.png "Publishing Tools")

12.- Click "File(F)" and then click "Save As".

![Publishing Settings](https://github.com/gamecoreSRC/HowToBuildWithUnityPS4800FakePKG/blob/master/image_2025-08-09_015527733.png "Publishing Tools")

13.- In the new window it opened, save it to your project folder.

![Publishing Settings](https://github.com/gamecoreSRC/HowToBuildWithUnityPS4800FakePKG/blob/master/image_2025-08-09_015614164.png "Publishing Tools")

14.- There should now be a "shareparam.json" where you saved it.

![Build Folder](https://github.com/gamecoreSRC/HowToBuildWithUnityPS4800FakePKG/blob/master/image_2025-08-09_015711184.png "Build Folder")

15.- Back in Unity, go back again to the Build Settings window. Press Player Settings button, and in the Inspector select the Publishing Settings. Now you have to use those 3 files in the options: Share parameter file to set shareparam.json, pronunciation.xml set to pronunciation.xml, and pronunciation.sig to pronunciation.sig. We have to do this because we're going to build a non development package, and to use that we have to set those 3 files.

![Publishing Settings](https://github.com/RetroGamer74/HowToBuildWithUnityPS4FakePKG/blob/master/Captura2.PNG "Publishing Settings")

16.- Finally set Build Settings -> Build Type: PS4 Package and remove any check from the checkboxes.

![Build Settings](https://github.com/RetroGamer74/HowToBuildWithUnityPS4FakePKG/blob/master/Captura.PNG "Build Settings")

17.- Set parental control to 1 in Publishing Settings. If you keep in value 11 which is default you will get an error about invalid parental control number.

18.- Now you can click Build, and you can do more builds without repeating all the steps shown here. You have to do this only once for the project. Remember you empty the folder Build before you try to compile again, because Unity requires build folder be empty if you are going to create a different Build Type, which is the case. We changed Build Type from PC Hosted to PS4 Package. After that you can build more times without clean folder while you create always PS4 Packages.
