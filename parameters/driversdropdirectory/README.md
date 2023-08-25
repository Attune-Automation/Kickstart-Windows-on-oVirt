Put any extra drivers you want used by WinPE and the Windows installer here.

This can contain subfolders.

These are the "*.inf" files.

WinPE's startnet.cmd will recursively search for the "*.inf" files to install.

autounattend.xml will do the same.

This folder path relative to "{ksAttuneBaseDir}/build-{targetServer.fqn}".

Example: Setting this as "drop_in_drivers" will mean the drivers drop in directory will be at "{ksAttuneBaseDir}/build-{targetServer.fqn}/drop_in_drivers".

If "drop_in_drivers" exists, it's contents will be copied to "Drivers" folder.

If "drop_in_drivers" does not exist, it is ignored.

The contents of the Drivers folder will eventually seen at "X:\attune_drivers" by WinPE and the Windows installer.