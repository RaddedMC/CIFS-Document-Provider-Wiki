# Manual

## Screen layout

### Main screen

The main screen displays a list of registered shared folders.

<img src="https://raw.githubusercontent.com/wiki/wa2c/cifs-documents-provider/locale/ja/images/screen_main_1.png" width="200px" />

**Details:**

* List items
  * Displays the registered shared folder name and connection destination URL.
  * Tap an item to move it to the edit screen and edit the corresponding shared folder settings.
* Add button
  * Appears at the end of the list items.
  * Tap an item to move it to the edit screen and register a new shared folder setting.
* Share button
  * Open a file from the registered shared folder and share it with other apps.
  * An error will occur if you select from a folder other than the registered shared folder.

### Editing screen

The edit screen is used to register and edit shared folder connection information.

<img src="https://raw.githubusercontent.com/wiki/wa2c/cifs-documents-provider/locale/ja/images/screen_edit_1.png" width="200px" />

**Details:**

* Identification name
  * Enter a name to identify the connection info.
  * If not entered, the hostname will be used instead.
  * It is irrelevant whether the connection is possible or not.
* Domain
  * Enter the domain to connect to.
  * Leave blank if you don't use domain information.
* Host
  * Enter the host to connect to.
  * Enter an IP address or hostname. (If your network does not use DNS, you should enter the IP address.)
* Username
  * Enter the username to log in with.
  * No username is required if you're connecting anonymously.
  * This field will be disabled if you check "Anonymous".
* Password
  * Same idea as above, enter the password to log in.
  * No password is required if you're connecting anonymously.
  * This field will also be disabled if you check "Anonymous".
* Anonymous
  * Check this if you don't connect with a username and password.
* Folder
  * Enter the destination folder path.
* Folder selection button
  * Select a destination folder from the folder picker.
  * If connection information is not entered above, an error will occur.
  * If you select a folder that is not at the destination (or otherwise not accessible), an error will occur.
  * You can also leave this field blank, which will just use '/'
* Add extension when saving
  * Adds file extensions automatically based on the file type, when a file is saved.
  * If the extension to be given matches the current file extension, this does nothing.
  * This is used when you want to add an extension automatically when saving manually, or when an application that automatically determines the file name does not add an extension.
* SMB URI
  * Displays the connection destination URI that will be created, based on your previous input. The app uses this URI to connect to the shared folder.
* Shared URI
  * Displays the shared URI that will be created, based on your previous input. This URI is used in other apps.
* Confirm connection button
  * Tests that a connection can be established with the entered info. Notifies you whether the connection test was successful or not.
  * If you entered a folder other than '/', make sure that the folder is accessible. (You may need to check permissions)
* Save button
  * Saves the information you entered and returns to the main screen.
  * Saving fails if a host is not entered.
* Delete button
  * Displays a confirmation dialog. Press OK on this dialog to delete the connection information.
* Back button
  * Returns to the main screen.
  * If editing, a confirmation dialog will be displayed. If you press OK, any changes will be discarded and you will be returned to the main screen.

## Registering and managing shared folder connection information

### Procedure to register shared folder connection information

The procedure to register a shared folder is described below:

1. Press the Add button on the main screen to open the edit screen.
2. Enter the shared folder info of the destination on the edit screen. The hostname is mandatory, as well as other fields.
3. Press the save button on the edit screen

The connection info to the shared folder is now registered. This info will be added to the main screen.

### Procedure to change shared folder connection info

The procedure to edit a shared folder's connection information is described below:

1. On the main screen, tap the connection information you want to edit. This will open the edit screen.
2. Edit the items you wish to change.
3. Press the save button on the edit screen.

This changes the connection information of the shared folder.

### Procedure for deleting shared folder info

The procedure to delete a shared folder's connection info is described below:

1. On the main screen, tap the connection info you want to delete. This will take you to the edit screen.
2. Press the delete button (top-right) to open the confirmation dialog
3. Press the OK button in the confirmation dialog

The connection information of the shared folder is deleted. It will be removed from the main screen.

## Using the shared folders

CIFS Documents Provider has the following two functions:

* Use shared folders in external apps
  Access shared folders from an external application through this one.
  Supports file read/write and folder access.
* File sharing in shared folders.
  Use this application to share files saved in shared folders with external applications (i.e, through the Android share sheet)

**[NOTE]**
* To use this functionality, you must register a shared folder.

### Procedure for using shared folders in external applications

The procedure to use a shared folder in another app is described below:

1. From an external app, open the Storage Access Framework file picker.
2. Select "CIFS Documents Provider" from the providers menu.
3. Select the desired file or folder.

With this operation, you will be able to access the corresponding file / folder from an external application.

<img src="https://raw.githubusercontent.com/wiki/wa2c/cifs-documents-provider/locale/ja/images/screen_provider_1.png" width="200px" />

### File sharing procedure in the shared folder

The procedure for sharing files in a shared folder is as follows:

1. Press the share button on the main screen to open the file picker.
2. Select the desired file from the registered shared folder (You can also multi-select).
3. The Share Sheet will be displayed, where you can select the desired application.

This action allows you to share the selected file to the desired app.

**[NOTE]**
If you select a file from a folder that is not a registered shared folder, it will be invalid.