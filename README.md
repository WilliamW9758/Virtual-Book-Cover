# Virtual Book Cover
## Download link
https://drive.google.com/file/d/1I0_dHsES5VPaSDe_nsJA6GDtJg-dBWWd/view?usp=drive_link

## Setup
Unzip the file and open the Unity project under 2022.3.19 version. Play the project with a connected camera and aim at a *Math with Bad Drawings* book. 

## Details
The front cover has a portal effect, where the tracking image is used as a portal to a bigger space. This is achieved using the Vuforia Depth Mask material, which blocks all virtual objects behind it, leaving only the camera footage to go through. I then made a custom transparent cover with essential elements of the original book cover and placed it as the texture of a quad. Finally, I searched up some school supply models in the Unity asset store and placed them in the portal. 

The back cover consists of the book's description and a short book review. You can switch between the two texts by pressing a virtual button. The Vuforia virtual button function has been deprecated for a couple of versions, however, it is not yet fully removed. In order to add it, the image tracker has to be from a database instead of just from an image. The original book's back cover was just plain blue, which made tracking impossible. So I added a few stickers on it to help the feature detection algorithm. 

## Limitations
The registration is sometimes not great even with the additional stickers. If the camera is too close to the book, it won't be able to pick up enough features to place the virtual objects correctly. The virtual object is also twitching a lot sometimes, possibly due to the same reason. 

Lighting was also an issue. Since it is very difficult to emulate the real lighting of the environment, I opt for using unlit materials on most virtual objects. 

## Demo
Video demo: https://youtu.be/jvrVFExXME4

Front Cover:
![Front Cover](/Images/front_cover.png)

Back Cover:
![Back Cover](/Images/back_cover.png)


