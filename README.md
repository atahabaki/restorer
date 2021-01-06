# Restorer

Restorer is a flashable zip file for all Android devices. It is 
designed to restore your data.

Below explains how it can be used...

## Usage

First, you need your backups..

You can backup just one package by:

```
adb pull /data/data/name.package
```

Or you could also: backup the entire `/data`:

```
adb pull /data/
```

Actually you can use your phone to take backup, but you know
how you can do (with root file manager, of course)...

Then paste them into corresponding `data/` folder. If you
pulled backup from `/data/app` you need to make `app` folder
in `data` directory.

Finally, you need update-binary for your device, you can 
extract that from OTA update. 'Cause `update-binary` file is
designed specifically for your device. So make sure to grab it,
or make an issue to let me which device you're using.

Final file hierarchy of the zip file should be:

```text
|-- META-INF
| |-- com
|   |-- google
|     |-- android
|       |-- update-binary
|       |-- updater-script
|-- data
```

Currently included device specific `update-binary`s listed below:

* Google GM5+ (shamrock)

But if you've your `update-binary` file you can use this still.

