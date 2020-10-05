Digital Development of the Making and Knowing Website
======

* Facsimile Images of Ms. Fr. 640 (Draft)
* Markup and Encoding of the Text of Ms. Fr. 640 (Draft)
* \[Use of the XML in the Edition\] (TODO) - Nick?
* Layout of the Diplomatic (Draft)
* Other Resources and Derivative Versions (Draft)
* Research and Scholarly Essays (Draft)
* Static Site Generation (Draft)

Facsimile Images of Ms. Fr. 640
---

The digital facsimile images of Ms. Fr. 640 are provided by the BnF’s digital library, [Gallica](https://gallica.bnf.fr/ark:/12148/btv1b10500001g). They are integrated into the Edition through its IIIF Manifest, which relates the Project's transcription and translation of the manuscript to the corresponding Gallica folio images via the IIIF Presentation API.

Markup and Encoding of the Text of Ms. Fr. 640
---

The [texts of Ms. Fr. 640](/#folios) are encoded in XML format and available in the [Project's Github repository](https://github.com/cu-mkp/m-k-manuscript-data). Each folio of the manuscript is represented as individual XML files in three versions: 
1. Diplomatic: diplomatic (verbatim) transcription of the original French text
2. Normalized: lightly normalized French transcription (with punctuation and diacritical marks added)
3. Translation: English translation

The transcription, translation, and encoding of the manuscript were primarily carried out in a series of paleography and text workshops (2014–2018) that brought together graduate students (already in possession of advanced French) to learn to read middle French script and gain experience in textual encoding. For more detail and a discussion of this process, please read Celine Camps and Margot Lyautey, [Ma<r>king and Knowing: Encoding BnF Ms. Fr. 640](/#essays/ann_335_ie_19). The XML files were then revised and finalized by Senior Project team members and the Digital Lead. Please also see Terry Catapano and Naomi Rosenkranz, [BnF Ms. Fr. 640 as a Digital Text](/#essays/ann_310_ie_19) and [Pamela H. Smith, Making the Edition of Ms. Fr. 640](/#essays/ann_329_ie_19).

The texts conform to a schema developed iteratively by the Project as the transcriptions and translation were revised and completed. While aimed to meet the specific needs of the Project, the custom schema is influenced by and derives much of its tagset from the [Text Encoding Initiative (TEI) Guidelines](https://tei-c.org/guidelines/P5/). The [schema](https://github.com/cu-mkp/m-k-manuscript-data/blob/master/schema/ms-transcription.rng) is maintained in the Project repository. The [Principles of Encoding](/#content/resources/principles-encoding) provide a full description of the Project's tagset.

\[Use of the XML in the Edition\] -- TO DO
---

Layout of the Texts of Ms. Fr. 640
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

Other Resources and Derivative Versions
---

A number of supplementary resources are maintained in the Project's Github repository:
- The content of the Editorial Comments are edited in a spreadsheet table by the Editorial Team and exported in CSV format for integration into the static-site-generated Edition. Each comment is anchored at the appropriate location in the XML folio files by use of an XML element which contains the ID for the corresponding record in the comment table.
- The [Glossary](/#folios/1r/f/1r/glossary) is similarly edited in a spreadsheet table by the Editorial Team and exported in CSV format for integration into the Edition.
- The source bibliographic metadata for the [Bibliography](/#content/resources/bibliography) is maintained in BibTeX and HTML formats in the Project’s [GitHub repository](https://github.com/cu-mkp/m-k-manuscript-data/tree/master/bibliographies).

To facilitate reuse and analysis of the Project's edited and encoded text of Ms. Fr. 640, files are provided in alternative formats including:
- [allFolios](https://github.com/cu-mkp/m-k-manuscript-data/tree/master/allFolios): for each version of the manuscript (diplomatic transcription, normalized transcription, and English translation), a single XML file containing each folio concatenated together
- [entries](https://github.com/cu-mkp/m-k-manuscript-data/tree/master/entries): for each version, every entry as a single file in both XML and TXT formats
- [ms-txt](https://github.com/cu-mkp/m-k-manuscript-data/tree/master/ms-txt): for each version, every folio as a single file in TXT format. 

Research and Scholarly Essays
---

All [essays](/#essays) are edited and maintained in the Project's Google Drive in order to best faciclitate the collaborative process. Each essay in the Drive has uniform organization and style to ensure consistency and allow for conversion to HTML and integration into this Edition. The Research and Scholarly Essays are supplemented with additional information (including Project-assigned themes, associated entries, and citation information) in a spreadsheet table and exported in CSV format for integration into the Edition.

For persistent access, each essay has been assigned a Digital Object Identifier (DOI) and will also be archived in Columbia University [Academic Commons](https://academiccommons.columbia.edu/) and downloadable as standalone publications.

Static Site Generation
------

In a typical website with a content management system, content is kept in a database and rendered into HTML when requested. With static site generation, pages are created beforehand. The content is already in its final form and can be sent as-is to the user.

Static sites generation has a number of advantages. One is that it responds really well with increased user traffic. Open source web servers like Apache and Nginx can very efficiently serve large amounts of static data. This leads to lower server costs. Because the technology is so fundemental to the web, techniques for serving static sites are likely to work well into the future and be universally understood by IT professionals tasked with keeping the assets online.

The biggest challenge in developing a website using this approach is that one needs to adopt or build an appropriate static site generator for the project. There are a number of existing projects in this space. Jekyll is the most well known, this project is built using the Ruby programming language.

Jekyll powers GitHub Pages, which allows a user to easily turn a GitHub repo into a static website. We looked at Jekyll initially for Making and Knowing but decided we need to build our own system based on the requirements of the project.

The content for the Making and Knowing project involved the scholarly work of a large team working over many years to explore the secrets of our text. The team kept most of this data on Google Drive. As the project evolved, more and more data was moved to GitHub repositories. So there was a need to draw content from both GitHub and Google Drive at build time.

In order to get the rendering of the transcription correct, we needed to be able to see how the transcribed XML looked in the diplomatic rendering on the website. A staging server was setup that would automatically regenerate the folio fews every few minutes. This real time look at the results was important to the workflow of the project.

Even though we were using very simple server technology, this did not proclude us using the latest client technology to render the site in the user's web browser. We used React and Material UI to develope the user interface. The static data was a mix of pre-rendered HTML pages and pre-rendered JSON data structures which were then processed by React to produce the final site.
