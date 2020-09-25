Digital Development of the Making and Knowing Website
======

* Markup and Encoding (TODO)
* Layout of the Diplomatic (Draft)
* Generating Entry Data (TODO)
* Static Site Generation (Draft)

Layout of the Diplomatic
----

The Making and Knowing Grid Layout is a rendering scheme is designed to faithfully render the layout of a single column of text, consisting of multiple entries, surrounded by marginalia. Each entry is given a unique id and may contain zero or more marginal notes. The marginal notes are wrapped in `<ab>` tags. The editor may specify the arrangement of these notes relative to the entry using the `<margin>` tag. Valid values for the margin tag are:

* top  note is above the entry and in the same column as the entry
* left-top note is above and to the left of the entry
* left-middle note is beside the entry to the left
* left-bottom note is below and to the left of the entry
* right-top note is above and to the right of the entry
* right-middle note is beside the entry to the right
* right-bottom note is below and to the right of the entry
* bottom note is below the entry and in the same column as the entry

These grid locations are relative to the entry. For example, in folio 4r, there are two entries. Both entries have notes in the left margin beside them. Each margin note is marked as "left-middle".

Additional Notes:

* If there are multiple notes with the same grid location, such as in folio 4v, they are rendered in the same grid location in the order they appear in the transcription.
* Content in the main entry div will take up both the middle and the right columns unless there are notes in the right column.
* Figures inherit the positioning of the `<ab>` block they are contained in.


Static Site Generation
------

In a typical website with a content management system, content is kept in a database and rendered into HTML when requested. With static site generation, pages are created beforehand. The content is already in its final form and can be sent as-is to the user.

Static sites generation has a number of advantages. One is that it responds really well with increased user traffic. Open source web servers like Apache and Nginx can very efficiently serve large amounts of static data. This leads to lower server costs. Because the technology is so fundemental to the web, techniques for serving static sites are likely to work well into the future and be universally understood by IT professionals tasked with keeping the assets online.

The biggest challenge in developing a website using this approach is that one needs to adopt or build an appropriate static site generator for the project. There are a number of existing projects in this space. Jekyll is the most well known, this project is built using the Ruby programming language.

Jekyll powers GitHub Pages, which allows a user to easily turn a GitHub repo into a static website. We looked at Jekyll initially for Making and Knowing but decided we need to build our own system based on the requirements of the project.

The content for the Making and Knowing project involved the scholarly work of a large team working over many years to explore the secrets of our text. The team kept most of this data on Google Drive. As the project evolved, more and more data was moved to GitHub repositories. So there was a need to draw content from both GitHub and Google Drive at build time.

In order to get the rendering of the transcription correct, we needed to be able to see how the transcribed XML looked in the diplomatic rendering on the website. A staging server was setup that would automatically regenerate the folio fews every few minutes. This real time look at the results was important to the workflow of the project.

Even though we were using very simple server technology, this did not proclude us using the latest client technology to render the site in the user's web browser. We used React and Material UI to develope the user interface. The static data was a mix of pre-rendered HTML pages and pre-rendered JSON data structures which were then processed by React to produce the final site.
