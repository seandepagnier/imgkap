## imgkap 1.11
Tool to manipuate raster nautical charts in KAP format

This repository is a Github clone of the original code created by M'dJ in 2011 and maintained by Pavel Kalian

```
Usage:
imgkap [option] [inputfile] [lat0 lon0 lat1 lon1 | headerfile] [outputfile]

imgkap Version 1.11 by M'dJ

Convert kap to img :
	imgkap mykap.kap myimg.png : convert mykap into myimg.png
	imgkap mykap.kap mheader.kap myimg.png : convert mykap into header myheader (only text header kap file) and myimg.png

Convert img to kap : 
	imgkap myimg.png myheaderkap.kap : convert myimg.png into myimg.kap using myheader.kap for kap informations
	imgkap myimg.png myheaderkap.kap myresult.kap : convert myimg.png into myresult.kap using myheader.kap for kap informations
	imgkap mykap.png lat0 lon0 lat1 lon2 myresult.kap : convert myimg.png into myresult.kap using WGS84 positioning
	imgkap -s 'LOWEST LOW WATER' myimg.png lat0 lon0 lat1 lon2 -f : convert myimg.png into myimg.kap using WGS84 positioning and options

Convert kml to kap : 
	imgkap mykml.kml : convert GroundOverlay mykml file into kap file using name and directory of image
	imgkap mykml.kml mykap.kap: convert GroundOverlay mykml into mykap file

WGS84 positioning :
	lat0 lon0 is a left,top point
	lat1 lon1 is a right,bottom point
	lat to be beetwen -85 and +85 degree
	lon to be beetwen -180 and +180 degree
	    different format are accepted : -1.22  1$B!k(B10'20.123N  -1d22.123 ...
Options :
	-n  : Force compatibilty all KAP software, max 127 colors
	-f  : fix units to FATHOMS
	-s name : fix souding datum
	-t title : change name of map
	-p color : color of map
	    - Kap to image color : ALL|RGB|DAY|DSK|NGT|NGR|GRY|PRC|PRG
		   ALL generate multipage image, use only with GIF or TIF	    - image or Kap to Kap color :  NONE|KAP|MAP|IMG
		   NONE use colors in image file, default
		   KAP only width KAP or header file, use RGB tag in KAP file
		   MAP generate DSK and NGB colors for map scan (< 64 colors) Black -> Gray, White -> Black
		   IMG generate DSK and NGB colors for image (photo, satellite...)

```