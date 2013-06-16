Dropbox Uploader Compress
-------------------------
v0.1.3 - Current Develop Release (2013-06-13).  
Certain feature may not work.  Please see the master branch for latest working version.

Author
------
Author: Dan Bough  
Email:  daniel.bough@gmail.com  
Web:    http://www.danielbough.com  

Dropbox Uploader Author  
-----------------------
Author: Andrea Fabrizi  
Email:  andrea.fabrizi@gmail.com  
Web:    http://www.andreafabrizi.it  
Readme:  RM.ORIG

Introduction
------------
Dropbox Uploader Compress is a fork of Andrea Fabrizi's Dropbox-Uploader (https://github.com/andreafabrizi/Dropbox-Uploader).  It's native purpose is to allow folder & file compression (tar / gzip) prior to uploading to dropbox.  

It does not change (and has no intentions of changing) Dropbox-Uploader.

Requirements
------------
- Perl v5

Instructions
------------
1) First time only:  Run `./dropbox_uploader.sh` & follow the instructions.  
2) Run `./db_uploader_compress.pl --help`

    Usage:  ./db_uploader_compress.pl [OPTIONS]
    Example:  ./db_uploader_compress.pl     --bu_source='/home/bar/foo' --bu_target_folder='baz'

    --bu_source          Required:  Folder of file to back up.  Do NOT use full paths or slashes.
    --bu_prefix          Optional:  Backed up file/folder filename prefix. (Defaults to 'default').  This is not applicable if the --nocompress flag is set.
    --bu_staging_folder  Optional:  Folder to stage backkup file / folder (it gets compressed here & then gets removed after it's uploaded.  Defaults to /tmp/.)
    --bu_target_folder   Optional:  Folder on dropbox to back up to.
    --compression_type   Optional:  Valid compression types:  tar (tar/gzip), zip (zip)
    --compression_path      Optional:  Path to compression file.  Default:  /bin/tar (tar), /usr/bin/zip (zip).
    --file_suffix        Optional:  Custom file suffix.  Used to obfuscate file types.
    --encrypt            Optional:  Encrypt file
    --help               Optional:  Display this message.
    --nocompress         Optional:  Do not compress file (tar and gzip). Folders HAVE to be compressed!
    --rm                 Optional:  Path to rm (defaults to /bin/rm).
    --script_name        Optional:  Name of Dropbox Uploader shell script (defaults to dropbox_uploader.sh).
    --script_path        Optional:  Path where dropbox_uploader.sh lives (defaults to local directory).

Tested On
---------
- Ubuntu Linux 12.04
- Raspberri Pi Linux 3.6.11

TODO
----
- Enable encryption

Changelog
---------
- v0.1.3 - Current develop release.  
-- Uses Dropbox Uploader v0.11.8  
-- Adds support for ZIP copmression.  
-- Adds ability to specify file extension (for file type obfuscation.)  
-- Adds option to encrpyt file / folder.  
-- Removes required flags (makes them optional) for easier use.
- v0.1.2 - Current beta release.  Uses Dropbox Uploader v0.11.6.
- v0.1.1 - More stable release.  Operates under normal conditions.
- v0.1 - Unstable release.  Active development.  