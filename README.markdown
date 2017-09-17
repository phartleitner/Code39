# Code 39 Barcode generator

found and made a tiny bit more versatile on Sept, 17 2017 

Simple PHP class for generating Code39 barcode images.  Really simple stuff: just do 

	$yourBarcode = new Barcode('text to encode');

Optionally, add a height in pixels and/or a width multiplier:

	$yourBarcode = new Barcode('text to encode', $height_in_px, $width_multiplier);

To send the "Content-type: image/png" header and output the code do 

	$yourBarcode->getCode39Image();

To get the binary image data (jpg)  to be put in a file or database do
	
	$yourBarcode->getCode39Binary();
	
You may then store this in a file

	file_put_contents(<path to file>,<the data>);
	
	expl.:  file_put_contents("tmp/barcode/mybarcode.jpg",$yourBarcode->getCode39Binary() )
	
Can be changed to png output by using imagepng() isntead of imagejpg(), of course.
	
	
