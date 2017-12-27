=======================================================================
Importing New Fonts in HTML & CSS
=======================================================================

There are two methods to importing new fonts:
1. Download the font file online and include in the root file and then link to the file using stylesheet.
2. Link to an online font inside an online library (e.g. Google Fonts).


=======================================================================
Method 1:
=======================================================================

The font must be downloaded and the TTF file must be placed within the root file. You may wish to organise your font by adding a Fonts folder to the root folder.
We do not need to do anything within the HTML file.
At the top of the stylesheet (.css file) we need a link to the font using @font-face{}. 

@font-face requires two attributes: 
1. A link to the font file within the root file - {src: url();
2. A font name that we would like to refer the font to when we want to refer to this font in our CSS - font-family: "font-name";}.

We would need to add this to all the stylesheet that requires this font.

=======================================================================
Method 2:
=======================================================================

In the HTML file we must create a link href tag to link the online font (we will be using Google Fonts: https://fonts.google.com/).

It is important that the link href tag for the online font is placed above the css stylesheet link tag this is because the browser reads the HTML document line by line from top to bottom and so we must load/read the font file in order for it to be used in the style sheet.

We can use the font-family in the CSS styesheet.

Some google fonts have different weights and style to them and we can generate the Google Font link by selecting the font we wish to use and then in the Customise Tab select the different weights we wish to use. We can then use the newly generated font link in our HTML page. in order to use the different weight/style, we must enter the font-weight: and font-style: in our CSS - for example:
<link href="https://fonts.googleapis.com/css?family=Spectral+SC:300,300i,400,700,700i" rel="stylesheet">
In order to use the Bold Italic weight style we must have the CSS code of:
   font-family: 'Spectral SC', serif;
   font-weight: 700i;
   font-style: italic;

(The numbers relate to the font wieght e.g. 700=bold, the i relates to which font-weight can be italic using the font-style property. 
Important Note: a font-weight selected that does not have an italic weight-style but the weight-style property was used to make the font italic, the font will default to a font-weight that has an italic weight-style for example 400 weight cannot be italic as there is no 400i and so 300/300i will be used as default for italic the font-style property)

Please refer to the Example provided in the method 2 Folder.

=======================================================================
Method 1 vs Method 2
=======================================================================
Method 1 allows you to view the font used in the website without internet connection however takes slightly longer for the website to load the font (wont be noticable but slight delay due to loading of the font). 

C.f 
Method 2 will not allow you to view the font if you do not have internet connection but it is faster to load inside the web browser as well as fast for developers to include the font within a link.


=======================================================================
Font-Websites
=======================================================================
https://fonts.google.com/ (Free)
https://www.dafont.com/ (Free)
http://www.fontspace.com/popular/fonts (Free)
https://typekit.com/fonts (Paid)

When using free fonts be careful with licenses to use for commercial purposes (i.e. not all free fonts will allow for commercial use)