# 'svn' is not recognized?
1. Download Tortoisesvn from https://tortoisesvn.net/downloads.html and open the exe
2. Click next..
3. When you reach the screen at Custom Setup, you'll have found `command line client tools'
4. Click it and set `Will be installed on local hard drive`
5. Press "Next" and continue the installation.


# Starting a New Plugin

1. Go to → `C:\xampp\htdocs\my-wordpress-org-approved-plugins`
2. Start Cmder & write this command → `svn co https://plugins.svn.wordpress.org/new-plugin-name`
3. Go new plugin folder → `cd new-plugin-name`
4. Now you've automaticaly generate 4 folders. Paste your plugin's files and folders in the `trunk` folder
5. Add all of your trunk and assets → `svn add trunk\*` and `svn add assets\*`
6. Add a commit message → `svn ci -m "Adding first version of the plugin"`
7. Give credential if want. Or commit with credentials → `svn ci -m "Adding first version of my plugin" --username username --password password`
8. Done!

# Updating an Existing Plugin

1. To check status → `svn st`
2. List out all the modified files → `svn st | grep "M "`
3. Commit through modified files → `svn commit -m "commit only modified files"`
4. Tagging the version if need, create a folder named version like 2.0.0 in tags folder, then commit → `svn copy https://plugins.svn.wordpress.org/plugin-slug/trunk/ https://plugins.svn.wordpress.org/plugin-slug/tags/2.0.0 -m "Tagging version 2.0.0"`

# Other Commits

1. Recursively clean up the working copy → `svn cleanup`
2. Unstage(unadd) a file → `svn revert --recursive folder_or_file_name`
3. Rename Existing File/s → `svn rename old-filename.extension new-filename.extension`
4. To delete file/s → `svn delete assets\file-name.png` or `svn delete assets\*`
> You can use `svn update` when bunch of files have deleting.
> Error: svn: directory is out of date..

# SVN GUI

#### Commit changes,
- After creating/adding or updating someting,
- right click → SVN Update → SVN Commit...

#### To delete someting,
- Right click over the file or folder → TortoiseSVN → Delete
- Again right click → SVN Update → SVN Commit...

#### To rename someting,
- Right click over the file or folder → TortoiseSVN → Repo-browser → Rename the file/folder → OK
- Again right click over the file or folder → Rename
- Update → SVN Commit...

#### Clear Authentication Data,
- Right click → TortoiseSVN → Settings → Saved Data → Authentication Data → Clear/Clear All

> And finaly using a software https://tortoisesvn.net/downloads.html to quick action without comand.
