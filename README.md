# edition-webpages
Explanatory and informational pages for M&amp;K online edition of BnF Ms. Fr 640

## How to Use

Files in the `docs` directory that have a '.md' extension are watched and processed by the MK Asset Server in HTML. The `menu_structure.json` file provides the layout of the top level menus on the website. Any routes defined in the JSON file that begin with `/content` will serve files with a matching path from this repository. Please note that the MK Asset Server copies all markdown files found in `docs` and its subdirectories, even if they are not referenced in the menu structure JSON.
