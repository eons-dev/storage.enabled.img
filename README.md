# Storage Enabled Image
This image adds storage capabilities to [eons/img_base](https://github.com/eons-dev/img_base).

So far, this image only includes `syncthing`, and `rclone` as the FUSE utility.

## Limitations

1. When using Rclone, you must use a cron job or equivalent to sync files with extended attributes or symlinks, as Rclone over FUSE does not support them.

## Storage Providers

### Syncthing

[Syncthing](https://syncthing.net/) provides the ability to clone and synchronize filesystems across multiple devices, in peer to peer fashion.

#### Usage
To use `syncthing`, you must do 1 thing: mount a valid syncthing config file to `/root/.config/syncthing/config.xml`.

### Rclone

[Rclone](https://rclone.org/) provides the ability to mount storage from many different clouds, technologies, etc. Rclone also includes a caching system that makes it perfect for use in containerized deployments.

#### Usage
To use `rclone`, you must do 1 thing: mount a valid rclone.conf file to `/root/.config/rclone/rclone.conf`

For how to configure `rclone`, see the official docs: [https://rclone.org/docs/](https://rclone.org/docs/).