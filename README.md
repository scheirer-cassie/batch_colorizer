# batch_colorizer
A Google Colab program that automatically colorizes large amounts of black and white images.

# HOW TO USE
## Windows: Download 7zip
The colorizer requires a zip file containing an empty folder, and unfortunately Windows 10 automatically deletes empty folders in a zip file. The software 7zip overrides this.

* Windows 32-bit : https://www.7-zip.org/a/7z1900.exe
* Windows 64-bit : https://www.7-zip.org/a/7z1900-x64.exe

## Organize zips
Put all your black and white images into one directory, and make an empty folder in the directory titled "result_images". 

![prezip](images/prezip.PNG)

## Make zips
Windows: 
1. Open 7zip
2. Navigate to the directory with your images and the empty folder
3. Select all images and folder
4. Right click --> 7Zip --> Add to Archive
5. These settings can be changed to your liking if you want to compress the zip, but otherwise change the defaults to what is shown in the picture below.
6. Click OK.

![afterzip](images/sendtozip.PNG)

## Make Google Drive folders
Make two new folders on your Google Drive, one where you will upload the black and white zip, and one which will end up with a colorized zip. Upload the zip file into the black and white folder.

![folders](images/folders.PNG)

## Define folder variables
In the Google Colab program, navigate down to the bottom of the script and enter in the ID of the black and white folder, the title of the black and white folder, and the GDrive path of the colorized folder. The ID of the black and white folder is the series of numbers and letters after the last slash in the URL of that folder. The path of the colorized folder will always be "/content/gdrive/"My Drive"/" plus the title of the color folder.

![variablenames](images/variablenames.PNG)
![insidezipfolder](images/insidezipfolder.PNG)

## Run the program
On the top left of the Colab program, go to Runtime --> Run all and watch the magic! Just follow the prompts of the script from this point. In the beginning pyDrive and the Google Drive API will ask you to authenticate their use of your Google Drive files--make sure you authenticate the email that has the zip files on its drive. The program will print updates in the terminal as each photo/zip is being colorized, and it will print "COLORIZING COMPLETE!" when all zips have been colorized. If done correctly, all of your black and white zips will have converted to colorized zips, which can be found in your colorized folder.

# RESOURCES
* [DeOldify](https://github.com/jantic/DeOldify)
* [Golan Levin](https://github.com/golanlevin)
* [STUDIO for Creative Inquiry](https://github.com/creativeinquiry)
* [PyDrive](https://pythonhosted.org/PyDrive/)
* [Google Drive API](https://developers.google.com/drive/api/v3/about-sdk)
