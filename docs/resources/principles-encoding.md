# Principles of Encoding

The encoding of Ms. Fr. 640 was carried out by graduate students and
Making and Knowing team members in a series of Paleography and Text
Workshops held by the Making and Knowing Project from 2014 to 2018. It
was then checked and refined by the Digital Lead Terry Catapano and
Senior Team members, Clement Godbarge, Naomi Rosenkranz, Pamela Smith, Tillmann Taape, and Tianna Uchacz. The Project employed
XML markup based on the guidelines of the Text Encoding Initiative
(TEI), but customized to accommodate project needs.

Each Text Workshop and encoding campaign necessitated a protocol in
order to train team members and make consistent the multiyear efforts.
These encoding protocols included an introduction to XML and TEI markup, and the principles of encoding for
Ms. Fr. 640 developed over the five years of the Project, as detailed
practical instructions. They made clear our recognition that encoding a text is an interpretive act, thus all tags
and encoding principles were discussed, reviewed, and revised multiple
times over the five years of creating *Secrets of Craft and Nature in Renaissance France*. They also set out
the Project’s underlying goal as the effort to "achieve accurate and
consistent markup of all three text versions of the manuscript. This is
a very detail-oriented endeavor, but will enable future users to analyze
the text in ways we have not conceived. We seek to make possible new
questions and new analyses of the text."

For more information on the process of encoding Ms. Fr. 640, see Celine
Camps and Margot Lyautey, [Ma\<r\>king and Knowing: Encoding BnF Ms. Fr.
640](/#essays/ann_335_ie_19).

In 2017 the emerging tagset was formalized as a RelaxNG schema and
maintained in the [Project’s data repository in Github](https://github.com/cu-mkp/m-k-manuscript-data/blob/master/schema/ms-transcription.md).

## Edition Tag Set

### Structural Tags

|  Tag |    Definition   |                        Description and Use                        |
|------|-----------------|-------------------------------------------------------------------|
| ab   | anonymous block | a block of text that belongs together semantically, or a unit within a longer entry indicated by the author-practitioner 
| div  | text division   | the span of a single, discrete entry                              |
| head | heading         | indicates the heading of a “recipe” or entry, classified as a div |
| id   | identifier      | a unique identifier for the text division                         |
| lb   | line break      | line break - only used in the French transcriptions               |

### Editorial Tags

|     Tag     |     Definition    |                                                                                                                    Description and Use                                                                                                                   | Rendering (when applicable)                                                                                            |
|-------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| add         | addition          | an addition made to the text by the writer in the original; renders in blue font of a smaller size. Passages were judged to be “additions” by: superscript in main body, significant changes in ink color, squeezed between other extant blocks of text. | ![howtouse-add](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-add.png)              |
| caption     | caption           | text descriptions of graphics provided by the author-practioner in the Ms.                                                                                                                                                                               |                                                                                                                        |
| comment     | comment           | anchors for commentary by the editors                                                                                                                                                                                                                    | ![howtouse-asterisk](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-asterisk.png)    |
| corr        | correction        | denotes an editorial correction by the Making and Knowing Project team; renders in square brackets                                                                                                                                                       | ![howtouse-square](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-square.png)        |
| del         | deletion          | denotes a deletion by the writer in the original; renders in struck-through red font                                                                                                                                                                     | ![howtouse-del](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-del.png)              |
| emph        | emphasis          | denotes italic French script                                                                                                                                                                                                                             | ![howtouse-bold](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-bold.png)            |
| exp         | expansion         | denotes use of abbreviation suspensions                                                                                                                                                                                                                  | ![howtouse-curly](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-curly.png)          |
| figure      | figure            | a sketch, drawing, diagram, etc. present in the source Ms.                                                                                                                                                                                               |                                                                                                                        |
| gap         | gap               | gap within the written text                                                                                                                                                                                                                              | ![howtouse-gap](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-gap.png)              |
| hr          | horizontal rule   | a horizontal line in the text                                                                                                                                                                                                                            | ![howtouse-hr](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-hr.png)                |
| ill         | illegible         | illegible                                                                                                                                                                                                                                                |  ![howtouse-illegible](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-illegible.png) |
| mark        | mark              | a mark in the text that has a corresponding unicode character                                                                                                                                                                                            |                                                                                                                        |
| sup         | supplied text     | editorial intervention by the Making and Knowing Project, supplying a word or correction for clarity in computational analysis of the text                                                                                                               | ![howtouse-square](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-square.png)        |
| underline   | underline         | underlining in the original                                                                                                                                                                                                                              |                                                                                                                        |
| superscript | superscript       | writing that appears in superscript in the original                                                                                                                                                                                                      |                                                                                                                        |
| ups         | under paper strip | parts of the text that were covered by the paper strips placed around each page of the manuscript during its seventeenth-century re-binding in the Bethune bindings                                                                                      | ![howtouse-ups](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-ups.png)              |

### Semantic Tags

| Tag |   Definition   |                                                                            Description and Use                                                                           |
|-----|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al  | animal         | denotes an animal                                                                                                                                                        |
| bp  | body part      | denotes a human body part                                                                                                                                                |
| cn  | currency       | a known coin or currency                                                                                                                                                 |
| df  | definition     | denotes where the author-practitioner defines or explains a term                                                                                                         |
| env | environment    | reference to a physical space or environment, such as workshop space, room, mountains, forest, etc                                                                       |
| m   | material       | a named physical material (e.g., “rose” but not “plant”), or a verb that implies a physical material, such as “to gild.”                                                 |
| md  | medical        | medical and health-related terms or phrases in an entry about some other topic. Medical recipes are categorized as such, but not marked with tags.                       |
| ms  | measurement    | units of measurement, including temporal, volume, mass, length                                                                                                           |
| mu  | music          | musical instrument                                                                                                                                                       |
| pa  | plant          | a named plant or part of a plant, not including plant gums                                                                                                               |
| pl  | place          | place name                                                                                                                                                               |
| pn  | personal name  | a name, including authors, mythical personages, or reference to a specific individual or entity, such as God, King, and "the one who taught me to mold" (110r)           |
| pro | profession     | denotes both a recognized trade, such as goldsmith, but also a social status or identity, such as peasant, or "rustic"                                                   |
| sn  | sensory        | use of the five senses to make a qualitative assessment                                                                                                                  |
| tl  | tool           | tool, including any instrument, and physical or material object used to perform a process, including body parts and verbs such as "piler" (to pestle) that imply a tool. |
| tmp | temporal       | references to time, including hour, day, season, holiday, span of time, time of day, etc.                                                                                |
| wp  | arms and armor | word or phrase referring to arms and armor                                                                                                                               |

### Foreign Languages

| Tag | Definition |                                                               Description and Use                                                               | Rendering (when applicable)                                                                                       |
|-----|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| de  | german     | denotes a word with a probable German origin                                                                                                    | ![howtouse-italics](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-italics.png) |
| fr  | french     | denotes a word left in French in the English translation because meaning is unclear or a translation does not exist, renders as italicized text | ![howtouse-italics](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-italics.png) |
| el  | greek      | a word or phrase in Greek (in Greek or Latin script)                                                                                            | ![howtouse-italics](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-italics.png) |
| it  | italian    | text in Italian                                                                                                                                 | ![howtouse-italics](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-italics.png) |
| la  | latin      | text in Latin                                                                                                                                   | ![howtouse-italics](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-italics.png) |
| oc  | occitan    | word or phrase in the Occitan language or of an Occitan root                                                                                    | ![howtouse-italics](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-italics.png) |
| po  | poitevin   | word in the Poitevin dialect                                                                                                                    | ![howtouse-italics](https://raw.githubusercontent.com/cu-mkp/edition-webpages/master/images/howtouse-italics.png) |

The Project used [unicode characters](http://unicode-table.com/en/) when they existed for the symbols used by the writer.

Project members worked in Google Drive to enable simultaneous work until
2018, when Project data, including all transcribed, translated, and
encoded versions of the folio pages, were transferred to GitHub. While
working in Google Drive, Text Workshop members used working tools
constructed by Project Assistant Philip Cherian, and are listed here in
case they are useful to users of *Secrets of Craft and Nature*.

Google Drive Add-on, **Tag Insertion** — a digital tool for quickly grabbing a tag and inserting into the text.    

Google Drive Add-on, **XML Validator** — a digital tool for validating markup before moving on to the next recipe or folio.
