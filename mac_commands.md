# Mac
Here I gathered some of important commands in mac.

## View ip address
```
ipconfig getifaddr en0
```

or type following command and see the ip in the `en0` section
```
ifconfig
```

## `ctrl+D` equivalent in mac
`command + L`

`command` key is the same as `ctrl` key in windows command like copy, paste and cut.


## Screenshot 

press `command+shift+3` for capturing whole of the screen and press `command+shift+5` for capturing porsion of the screen.


## Half Space in Mac
presss `shift+space`


## Cut in mac
Select your desired file or folder and press `command+c` then in target path press `command+option+v`


## Show hidden files in mac
press `command+shift+.`


## Disable Gatekeeper
you can temporarily disable Gatekeeper, which is Apple's security feature that prevents the installation of apps from unidentified developers. Open Terminal and enter the following command:
```
sudo spctl --master-disable
```

## Enable Gatekeeper
After installing your desired program, it is advisible that enable gatekeeeper with following command:
```
sudo spctl --master-enable

```
