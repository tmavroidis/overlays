# overlays
Creating printer overlays with free tools
If you are constantly creating or modifing templates I recommed you purchase a commercial tool like TL Ashford (https://tlashford.com/), but if you only need a template or two you can create them using freely available tools.
You need to download the latest APF driver from Ricoh https://dl.ricohsoftware.com/eid/download/OTI4MzY2MDE1NDY%3D/aa9a248e-101c-4aa6-b109-1cf7403f3b4f  https://dl.ricohsoftware.com/downloads/aa9a248e-101c-4aa6-b109-1cf7403f3b4f
Might as well download the APF viewer https://dl.ricohsoftware.com/eid/download/OTI4MzQzODQxNTQ2/aa9a248e-101c-4aa6-b109-1cf7403f3b4f
If my links have stopped working google "ricoh afp workbench"
Once installed you will find a printer installed called "Generic infoprint 300dpi"
Create the overlay in whatever program you like and then choose the infoprint printer.
Its important to adjust your margins, (I usually make them 0 all around) so it doesn't make the overlay fit by shrinking the print. You cant go right to the margin so be aware.

Select ![image](https://github.com/user-attachments/assets/71bd1af6-984f-4307-a893-98e278ffd90a)

In output type select overlay and in image options select full color.

On your IBM i create a library for the overlays, I created a library called overlays. 

Print to a file with the extension .ovl
Change directory on your PC to where the .ovl resides. CD source
From the command line ftp to your IBM i and signin 
Change to binary mode - BIN
CD to overlays - CD OVERLAYS
transfer the ovl - put xxxx.ovl overlays/xxxx.

On the ibm i crtovl ovl(overlays/xxxx) file(overlays/xxxx)
You now have an overlay in libray overlays called xxxx.

You can use the overlay when creating your printer file or use an override when printing.
