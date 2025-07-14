# cursor-in-browser
## Deploy and use **Cursor - The AI Code Editor** directly in a **web browser**!

This work have been **strongly** influenced by the following repo: https://github.com/sytone/obsidian-remote

Now available for version 1.2.0 of Cursor for x64 and arm64 architectures.

Images of older **Cursor** versions will also be provided.

### **• Maintained by:**

Forked from L'Arfo (arfo_dublo@boards.digital)⁠

### **• Where to get the image:**

https://hub.docker.com/r/arfodublo/cursor-in-browser

### **• Quick run :** 

```
docker run -d \
      -v your_path_to/cursor:/cursor \
      -v your_path_to/config:/config \
      -p 8050:8080 \
      -e CUSTOM_USER=cursor_user \
      -e PASSWORD=cursor_password \
arfodublo/cursor-in-browser:1.2.0
```

### **• Important notes :**

1. Some buttons are not directly clickable in the UI. **Log in** button is part of those, to use these buttons you will need to copy the link (right click on them then copy) and open them in a new tab. Then follow the log in procedure on Cursor official web site in this **Log in** button example.

2. If you closed Cursor you will be redirected to a black screen. To reopen Cursor right click on this screen a menu will appear with Cursor icon and name. You can simply click on it to open it back.

### **• Environment Variables :** 

|Environment Variable |	Description|
|---|---|
|PUID|	Set the user ID for the container user. 911 by default.|
|PGID|	Set the group ID for the continer user. 911 by default.|
|TZ|	Set the Time Zone for the container, should match your TZ. Etc/UTC by default. See List of tz database time zones for valid options.|
|DOCKER_MODS|	Use to add mods to the container like git. E.g. DOCKER_MODS=linuxserver/mods:universal-git See Docker Mods for details.|
|INSTALL_PACKAGES|	Use to add package for the container like language pack. E.g. INSTALL_PACKAGES=fonts-noto-cjk fonts-noto-extra And the docker mod linuxserver/mods:universal-package-install is required.|
|KEYBOARD|	Used to se the keyboard being used for input. E.g. KEYBOARD=en-us-qwerty or KEYBOARD=de-de-qwertz a list of other possible values (not tested) can be found at https://github.com/linuxserver/docker-digikam#keyboard-layouts|
|CUSTOM_PORT|	Internal port the container listens on for http if it needs to be swapped from the default 3000.|
|CUSTOM_HTTPS_PORT|	Internal port the container listens on for https if it needs to be swapped from the default 3001.|
|CUSTOM_USER|	HTTP Basic auth username, abc is default.|
|PASSWORD|	HTTP Basic auth password, abc is default. If unset there will be no auth|
|SUBFOLDER|	Subfolder for the application if running a subfolder reverse proxy, need both slashes IE /subfolder/|
|TITLE|	The page title displayed on the web browser, default "KasmVNC Client".|
|FM_HOME|	This is the home directory (landing) for the file manager, default "/config".|

### More details about the image here: https://hub.docker.com/r/arfodublo/cursor-in-browser

A particular thanks to Joe (Sytone) who did the same job for Obsidian that can be found here: https://github.com/sytone/obsidian-remote
