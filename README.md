# edition-webpages
Explanatory and informational pages for M&amp;K online edition of BnF Ms. Fr 640

_Secrets of Craft and Nature in Renaissance France. A Digital Critical Edition and English Translation of BnF Ms. Fr. 640_ 
https://edition640.makingandknowing.org/

## How to Use

Files in the `docs` directory that have a '.md' extension are watched and processed by the MK Asset Server into HTML. 

### menu-structure.json
The `menu-structure.json` file provides the layout for the main menu on the MK website. Any routes defined in the JSON file that begin with `/content` will serve files with a matching path from this repository. Please note that the MK Asset Server copies all markdown files found in `docs` and its subdirectories, even if they are not referenced in the menu structure JSON.

Routes in `menu-structure.json` with a `sections` property will populate that page's side navigation bar w/ top level scroll links (see pictured). Each section in `sections` may have `sub_sections` which are the second level scroll links in the page's side navigation bar (see pictured). Both sections and sub_sections need a `title` and `id` property. 

The `title` is what you want the actual link to say. The `id` must match the `id` that will be generated when the markdown file is converted to html. This `id` will be the same text as is in the header in the markdown file but converted to kebab-case. For example, if the markdown file has the following:

```
...
## This is The Heading
...
```
The html `id` will look like this: `this-is-the-heading`. So you'd put that as the `id` for the relevant section or sub_section.


