# Starting a New Plugin

1. Go to → `C:\xampp\htdocs\my-wordpress-org-approved-plugins`
2. Start Cmder & write this command → `svn co https://plugins.svn.wordpress.org/new-plugin-name`
3. Go new plugin folder → `cd new-plugin-name`
4. Now you've automaticaly generate 4 folders. Paste your plugin's files and folders in the `trunk` folder
5. Add all of your trunk → `svn add trunk\*`
6. Add a commit message → `svn ci -m "Adding first version of my plugin"`
7. Give credential if want.
8. Done!

# Updating an Existing Plugin

1. To check status → `svn st`
2. List out all the modified files → `svn st | grep "M "`
3. Commit through modified files → `svn commit -m "commit only modified files"`
4. Done!
