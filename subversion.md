# Starting a New Plugin

1. Go to → `C:\xampp\htdocs\my-wordpress-org-approved-plugins`
2. Start Cmder & write this command → `svn co https://plugins.svn.wordpress.org/new-plugin-name`
3. Go new plugin folder → `cd new-plugin-name`
4. Now you've automaticaly generate 4 folders. Paste your plugin's files and folders in the `trunk` folder
5. Add all of your trunk and assets → `svn add trunk\*` and `svn add assets\*`
6. Add a commit message → `svn ci -m "Adding first version of the plugin"`
7. Give credential if want.
8. Done!

# Updating an Existing Plugin

1. To check status → `svn st`
2. List out all the modified files → `svn st | grep "M "`
3. Commit through modified files → `svn commit -m "commit only modified files"`
4. Done!

# Other Commits

1. Recursively clean up the working copy → `svn cleanup`

# Delete Existing File/s

1. To delete file/s → `svn delete assets\file-name.png` or `svn delete assets\*`
2. `svn ci -m "message for the commit like deleted folder delete-me"`

# SVN GUI

- After creating/adding or updating someting,
- right click → SVN Update → SVN Commit...

- To delete or rename someting,
- right click over the file or folder → TortoiseSVN → Rename.../Delete
- Again right click → SVN Update → SVN Commit...

> And finaly using a software https://tortoisesvn.net/downloads.html to quick action without comand.
