# googleimages
Populates the active Google Sheet with the names, direct URLs, file size & owner of all images in a defined Google Drive folder.

## Guide
1. Insert the folder ID of a given Google Drive folder (i.e. for https://drive.google.com/drive/folders/2q_moO0wARD6_NUnd7RoOrAY1pKSZXZn5, the ID would be 2q_moO0wARD6_NUnd7RoOrAY1pKSZXZn5) into cell A1
2. Copy the contents of script.js
3. In a Google Sheet, go to the Script Editor (in the _Tools_ menu).
4. Paste the contents of script.js
5. Run the script
6. If prompted, allow any permissions prompts (only required on first run)

Note that the script relies upon the contents of cell A1 to determine which folder to process.

It is recommended to clear the sheet before repeating this process, and only having cell A1 populated with the Google Drive folder's ID.

## Todo
1. Add support for multiple folder processing
