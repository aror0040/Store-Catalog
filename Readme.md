
Store-Catalog

Task description
The task is to create a catalog web-page which gets the products loaded from the array stored in a separate PHP file. Catalog will contain at least 3 types of products. You need to have at least 6 products of each type.  On page load, all products will be loaded into your catalog as a set of thumbnails. Each product contains name and price.

Drop-down menu will be a part of the main navbar - use it for selecting desired type of product.



You may use Bootstrap for this project. Use custom fonts and color scheme appropriate for given topic. Make the site pop!

 

File Structure
The name of your project will be:  firstname-lastname-p1-1531.



 

Wireframe and Mockup

Do wireframe and mockup only for desktop view. Save wireframe and mockup inside the folder named "design" as .jpg, .png or .gif files.


Order of Operations
Complete PHP
Complete CSS

 

Fonts
You need to use serif/sans-serif Google font pair. Serif font is for headings and sans-serif font is for body text. Fall-back font is going to be default serif/sans-serif font.

References:

http://fontpair.co (Links to an external site.)Links to an external site.

https://fonts.google.com (Links to an external site.)Links to an external site.

Line height ratio has to be between 1.4 and 1.6. You need to use following font-sizes:

Mobile View: 0.75rem

Tablet/Desktop View: 1rem
 

Colors
Choose appropriate color scheme for chosen topic. List the hexadecimal values of colors (as CSS comment) inside CSS style-sheet. Reference: color.adobe.comLinks to an external site.

 

Images
Provide images. All images for your products need to be formatted to 400x400 and OPTIMIZED for web. You may use your own images or choose images from:

http://www.freeimages.comLinks to an external site.

http://www.morguefile.comLinks to an external site.

 

Mobile View < 36rem
Entire content is displayed in 1 column:


Tablet View



Desktop View



Coding Guidelines
stock.php
// Your array of products should look like:
$products = [
   [
      "prod-property-1" => "value-1",
      "prod-property-2" => "value-2",
      .
      .
      .
   ],
   [
      .
      .
      .
   ],
   .
   .
   .
];
index.php
This drop-down should be in the navigation bar. If you use Bootstrap, drop-down looks like this:


You can see the highlighted query string. When a link of drop-down menu is clicked, it calls index.php and passes a unique value of product-type to $_GET array.

// Have a PHP snippet above <!doctype html> where you are going to 
// include stock.php and collect-and-print-data.php. 

// Inside navbar, you will have a drop-down menu for selecting type 
// of a product. Drop-down has 3 items. These items are links. Href
// attribute of each link will point to index.php. 
// Each link will also contain a unique query-string-value. This value 
// is unique because it defines a type of a product.

// In short: When a link of drop-down menu is clicked, it calls index.php
// and passes a unique value of product-type to $_GET array. 

// Main-content of index.php is where you want to print the HTML content
// generated in collect-and-print-data.php. This HTML content is generated based on the 
// query string from selected link in the drop-down. 
collect-and-print-data.php
// COLLECT DATA
// Create the function collectArray.
// This function contains the parameter 
// that defines the required product-type. 

    // Make $products from your stock available 
    // inside this function.(use statement global)

    // Have a new empty array ready for 
    // collecting required products 
    
    // Check if $products array has any elements 
        
        // If so,
        // scan through $products array (foreach-loop) and check
        // each product if it contains the required product-code 
            // If the match is found, push the 
            // fitting product into $collect array. 
        // close if
        
        // If $collect is not empty,
            // return $collect.
        // otherwise:
            // return $products. 
        // close conditional

    // close if

// close collectArray


// PRINT HTML:
// Create function printHTML.
    // Check if a product-code is in $_GET array. If product code is 
    // in $_GET array, it means user selected it, and you will 
    // print only the products of the selected type, otherwise
    // print all products.

    // You need to loop through the array of selected products,
        // create HTML tags in the fly and extract values 
        // of each product into proper or corresponding HTML tag.
        // Print the HTML content.
    // Close loop.
// Close printHTML.

HTML Structure to be Created
The highlighted part of the html below is the "markup-shell" of a single product, and it has to be generated in the loop!
Sheenam Arora



