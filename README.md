# Storage Enabled Image
This image adds storage capabilities to [eons/img_base](https://github.com/eons-dev/img_base).

So far, this image only includes `rclone` as the FUSE utility.
[Rclone](https://rclone.org/) provides the ability to mount storage from many different clouds, technologies, etc. Rclone also includes a caching system that makes it perfect for use in containerized deployments.

## Limitations

No known limitations at this time.

## Storage Providers

### Rclone

#### Usage
To use `rclone`, you must do 1 thing: mount a valid rclone.conf file to `/root/.config/rclone/rclone.conf`

For how to configure `rclone`, see the official docs: [https://rclone.org/docs/](https://rclone.org/docs/).