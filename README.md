# Workadventure maps
Rules:
- Mapsize: 64x64 tiles
- Tilesize: 32x32 pixel

# Tiles
We decided to use the tiles you find in the "tiles" directory. Those are not all free, so please ensure not using them for externally available maps.

# How to
Hey together, this is a short guide how to make your self designed maps available to your t-systems collegues!

1. Design your own map with the Tiled editor. 
Take a look on the requirements for a workadventure map on the official WA "build your map" site.
(https://workadventu.re/map-building)
You should have all your dependencys in the project path or a subdirectory.

2. Export your Tiled project to a .json file (via Tiled editor) and upload it to the Magenta CI/CD on GitLab.
Also upload your folder with the dependencys (the folder with the tiles in .png or whatever) and make sure
you have the same dependency file paths as before on your machine.
(If you had your dependencys in the same folder as your project, your fine)

3. GitLab Pages is necassary. It should already be activated. Just use the link
https://play.workadventu.re/_/global/andreas.eisenreich.pages.devops.telekom.de/wamaps/[Your .json Filename]
and share it to your collegues.


-> Known Issues (and how you solve them ;))

1. Black tiles instead of the tiles you wanted to integrate:
When your tileset image source is to big, workadventure wont use it! Make sure the size of the tileset is not bigger than 640x5920.
At most time, the length of the picture is the problem. You can use image divider from the internet or just the common windows tool for
resizing images. I would recommend using some real image manipulation software like GIMP, because you should cut the picture in a 32x 
size and such softwares are more exact and better to handle.

2.You dont see any tile, although its embedded and visible in Tiled:
One Problem is using groups in Tiled. I dont know why, but workadventure cant handle it. Just put the layers out of the sub directory
into the main one!
