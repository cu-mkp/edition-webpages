# edition-webpages
Explanatory and informational pages for M&amp;K online edition of BnF Ms. Fr 640

_Secrets of Craft and Nature in Renaissance France. A Digital Critical Edition and English Translation of BnF Ms. Fr. 640_ 
https://edition640.makingandknowing.org/

## How to Use

Files in the `docs` directory that have a '.md' extension are watched and processed by the MK Asset Server into HTML. The `menu-structure.json` file provides the layout for the main menu on the MK website. Any routes defined in the JSON file that begin with `/content` will serve files with a matching path from this repository. Please note that the MK Asset Server copies all markdown files found in `docs` and its subdirectories, even if they are not referenced in the menu structure JSON.
