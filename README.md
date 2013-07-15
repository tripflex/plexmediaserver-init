# Plex Media Server INIT Script

http://smyl.es/the-ultimate-nas-media-center-with-debian-based-openmediavault-and-plex-media-server/

This is the init script for Plex Media Server that should be located at /etc/init.d/plexmediaserver.   This is something I had to track down when setting up Plex Media Server with OpenMediaVault, as the default installer for PlexMediaServer seems to have a problem with creating the init script, so I had to manually add it.

## Installation
``` bash
wget https://raw.github.com/tripflex/plexmediaserver-init/master/plexmediaserver
mv plexmediaserver /etc/init.d/plexmediaserver
chmod +x /etc/init.d/plexmediaserver
```

## Usage
Using this should be just the same as you normally do, but as example

``` bash
/etc/init.d/plexmediaserver {start|stop|restart|status}
```

If you upgrade plex using the deb, the installer will rename the file to something like plexmediaserver.bkup, you will just need to remove the new /etc/init.d/plexmediaserver it created (should be blank), and move the backup back to it's original name.

Profit!
