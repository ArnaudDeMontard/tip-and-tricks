# How to open a database without executing the Startup method?

4D keep links to the recents opened databases into a folder named "Favorites vXX" where XX is the major 4D version number. This folder is in the current "4D folder" (<a href="How to locate the current 4D Folder.md">How to locate the current 4D Folder?</a>).

You should find into this folder a file named {database}.4dlink where database is the name of your database. This is the file you need to edit.
It is a XML structure that you can edit with a text editor.

Open the file and place the cursor at the end of the element `<database_shortcut` just before the `/>`. Type a _space_ then the the string `skip_onstartup_method="true"`

Save

Open 4D and select Open > Recent databases > your database.

**Note**: The .4dlink file will be automatically updated by 4D and the additionnal attribute will be removed.




