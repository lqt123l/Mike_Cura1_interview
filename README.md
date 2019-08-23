# Mike_Cura1_interview
This demo project is for Mike's interview.

Because this is a pretty simple page that only have limited functions, I decided just use a single page with jQuery to finish it.

The main process of this page is: Ajax get image data from the API and display these images in the webpage. Then when users click a specific image, the information of this image will display, and then user can close this display and choose other images.

There are three parts of this page: HTML JS and CSS. Additional Jquery are imported from third party sources.

For HTML, there is a gird to show the images list. 
Followed by the gird is a Wrapper division, and it includes several elements that enable users to futher discover an specific image when they click that image. And "X" button was added to close the wrapper.

For JS part, first of all, global variables were setted include images array and screen size variables.
Then is the Ajax part that call the unSplash API to get image array. The Access Key should be stored in the system environment variable for security reason, but can be ignored for this demo.
When the Ajax call success, it would return an array, and then use array.map() function to append image into the gird one by one and show these images, I also set the image id for future convenience.
When user click any of .image class image, the jQuery will get this image id, and search this id in the global image list, and  then get the image object which match this id. The object contains all the information we need, therefore a larger image would be displayed and a table was used to display these useful information.

For CSS part, there are two important part
The first one is the wrapper part, I set the wrapper full screen and z-index 100, therefore it can cover the image gird. 
For the mobile phone view, the width was set to 100% to ensure it look good.
