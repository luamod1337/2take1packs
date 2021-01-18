<!-- ABOUT THE PROJECT -->
## About 2take1pack

```2take1pack``` is a filetype for <a href="https://github.com/luamod1337/2Take1Tool">2Take1Tool</a>. \
It can contain every file you want, including directorys which should be copied.\

### Installation
There are two ways to install a 2take1pack

Automatic:

> Packets will be installed through <a href="https://github.com/luamod1337/2Take1Tool">2Take1Tool</a> 


Manual:

> - download the wanted pack
> - copy it to **%appdata%/2Take1Tool/\<type\>**
> -  Packet will be displayed inside 2take1tool as installed



## Packet Creation
A 2take1pack is basicly a renamed ```zip```  file with a diffrent file extension.\
This means you can open it with any ```zip``` compatible File explorer.\
Examples are Winrar, 7Zip or even the Windows Explorer.\
Either rename the file to ```xyz.zip``` or open it with a zip program.

![example of an opened pack with 7zip](/images/7zip.png)


it is **required** that a 2take1pack contains an **install.yml** file

### ```install.yml File```

#### Compatible install sections:

You can use this configuration sections to mark the installation of a 2take1pack

- CopyFiles
  - Here you can List every file which should be copied to the root directory of the
- CopyFolder
  - Here you can List every Directory which should be copied to the root directory of the pack
- Description
  - A list of descriptions, can contain images with ```Image: img/image.png```
  - **optional**, but needs to exists with an **empty** first item
- Version
  - a string equivalent to the version of the pack
- Name
  - a string with the name of the pack
- Logo
  - a path to the logo of the pack
- updateCheckUrl
  - a url to an update.yml file
  - **optional**

#### Example ```install.yml```

```
CopyFiles:
  - main.lua
CopyFolder:
  - lib
  
Description:
  - '- Hello World #1'
  - '- Hello World #2'
  - Image: img/feature1.png
  - '- Hello World #3'
Version: '0.1'
Name: Pack1
Logo: img/Logo.png
updateCheckUrl: 'https://raw.githubusercontent.com/luamod1337/ZeroMenu/master/update.yml'
```

On installation:

- copy main.lua
- copy lib and every file in that directory

On display:
- display the Name ```Pack1``` with the version ```0.1```
- display the Logo ```img/Logo.png```
- display ```- Hello World #1```
- display ```- Hello World #2```
- display the image in ```img/feature1.png```
- display ```- Hello World #3```
- display an update Check Button

On update:

**On startup** and if the user wishes, there will be an update check for a pack, if an ```updateCheckUrl``` got provided. \
An example for such a file can be found here, https://github.com/luamod1337/ZeroMenu/blob/master/update.yml.

















