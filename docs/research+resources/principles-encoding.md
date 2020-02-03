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
640](/#essays/ann_331_ie_19).

In 2017 the emerging tagset was formalized as a RelaxNG schema and
maintained in the [Project’s data repository in Github](https://github.com/cu-mkp/m-k-manuscript-data/blob/master/schema/ms-transcription.md).

## Edition Tag Set

<table>
<thead>
<tr class="header">
<th><strong>Tag</strong></th>
<th><strong>Definition</strong></th>
<th><strong>Description and Use</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>al</td>
<td>animal</td>
<td>denotes an animal</td>
</tr>
<tr class="even">
<td>bp</td>
<td>body part</td>
<td>denotes a human body part</td>
</tr>
<tr class="odd">
<td>caption</td>
<td>caption</td>
<td>text descriptions of graphics provided by the author-practioner in the Ms.</td>
</tr>
<tr class="even">
<td>cn</td>
<td>coin</td>
<td>a known coin or currency</td>
</tr>
<tr class="odd">
<td>df</td>
<td>definition</td>
<td>denotes where the author-practitioner defines or explains a term</td>
</tr>
<tr class="even">
<td>env</td>
<td>environment</td>
<td>reference to a physical space or environment, such as workshop space, room, mountains, forest, etc</td>
</tr>
<tr class="odd">
<td>m</td>
<td>material</td>
<td>a named physical material (e.g., “rose” but not “plant”), or a verb that implies a physical material, such as “to gild.”</td>
</tr>
<tr class="even">
<td>md</td>
<td>medical</td>
<td>medical and health-related terms or phrases in an entry about some other topic. Medical recipes are categorized as such, but not marked with &lt;md&gt; tags.</td>
</tr>
<tr class="odd">
<td>ms</td>
<td>measurement</td>
<td>units of measurement, including temporal, volume, mass, length</td>
</tr>
<tr class="even">
<td>mu</td>
<td>music</td>
<td>musical instrument</td>
</tr>
<tr class="odd">
<td>pa</td>
<td>plant</td>
<td>a named plant or part of a plant, not including plant gums</td>
</tr>
<tr class="even">
<td>pl</td>
<td>place</td>
<td>place name</td>
</tr>
<tr class="odd">
<td>pn</td>
<td>personal name</td>
<td>a name, including authors, mythical personages, or reference to a specific individual or entity, such as God, King, and &quot;the one who taught me to mold&quot; (110r)</td>
</tr>
<tr class="even">
<td>pro</td>
<td>profession</td>
<td>denotes both a recognized trade, such as goldsmith, but also a social status or identity, such as peasant, or &quot;rustic&quot;</td>
</tr>
<tr class="odd">
<td>sn</td>
<td>sensory</td>
<td>use of the five senses to make a qualitative assessment</td>
</tr>
<tr class="even">
<td>tl</td>
<td>tool</td>
<td>tool, including any instrument, and physical or material object used to perform a process, including body parts and verbs such as &quot;piler&quot; (to pestle) that imply a tool.</td>
</tr>
<tr class="odd">
<td>tmp</td>
<td>temporal</td>
<td>references to time, including hour, day, season, holiday, span of time, time of day, etc.</td>
</tr>
<tr class="even">
<td>wp</td>
<td>arms and armor</td>
<td>word or phrase referring to arms and armor</td>
</tr>
<tr class="odd">
<td>ab</td>
<td>anonymous block</td>
<td>a block of text that belongs together</td>
</tr>
<tr class="even">
<td>add</td>
<td>addition</td>
<td><p>an addition made to the text by the writer in the original; renders in blue font of a smaller size. Passages were judged to be “additions” by:</p>
<ul>
<li><blockquote>
<p>superscript in main body</p>
</blockquote></li>
<li><blockquote>
<p>significant changes in ink color</p>
</blockquote></li>
<li><blockquote>
<p>squeezed between other extant blocks of text</p>
</blockquote></li>
</ul></td>
</tr>
<tr class="odd">
<td>comment</td>
<td>comment</td>
<td>anchors for commentary by the editors</td>
</tr>
<tr class="even">
<td>corr</td>
<td>correction</td>
<td>denotes an editorial correction by the Making and Knowing Project team; renders in square brackets</td>
</tr>
<tr class="odd">
<td>del</td>
<td>deletion</td>
<td>denotes a deletion by the writer in the original; renders in struck-through red font</td>
</tr>
<tr class="even">
<td>div</td>
<td>text division</td>
<td>the span of a single, discrete entry</td>
</tr>
<tr class="odd">
<td>emph</td>
<td>emphasis</td>
<td>denotes italic French script</td>
</tr>
<tr class="even">
<td>exp</td>
<td>expansion</td>
<td>denotes use of abbreviation suspensions</td>
</tr>
<tr class="odd">
<td>figure</td>
<td>figure</td>
<td>a sketch, drawing, diagram, etc. present in the source Ms.</td>
</tr>
<tr class="even">
<td>fr</td>
<td>french</td>
<td>denotes a word left in French in the English translation because meaning is unclear or a translation does not exist, renders as italicized text</td>
</tr>
<tr class="odd">
<td>gap</td>
<td>gap</td>
<td>gap within the written text</td>
</tr>
<tr class="even">
<td>de</td>
<td>german</td>
<td>denotes a word with a probable German origin</td>
</tr>
<tr class="odd">
<td>gk</td>
<td>greek</td>
<td>a word or phrase in Greek (in Greek or Latin script)</td>
</tr>
<tr class="even">
<td>head</td>
<td>heading</td>
<td>indicates the heading of a “recipe” or entry, classified as a div</td>
</tr>
<tr class="odd">
<td>hr</td>
<td>horizontal rule</td>
<td>a horizontal line in the text</td>
</tr>
<tr class="even">
<td>id</td>
<td>identifier</td>
<td>a unique identifier for the text division</td>
</tr>
<tr class="odd">
<td>ill</td>
<td>illegible</td>
<td>illegible</td>
</tr>
<tr class="even">
<td>it</td>
<td>italian</td>
<td>text in Italian</td>
</tr>
<tr class="odd">
<td>la</td>
<td>latin</td>
<td>text in Latin</td>
</tr>
<tr class="even">
<td>lb</td>
<td>line break</td>
<td>line break - only used in the French transcription</td>
</tr>
<tr class="odd">
<td>mark</td>
<td>mark</td>
<td>a mark in the text that has a corresponding unicode character</td>
</tr>
<tr class="even">
<td>oc</td>
<td>occitan</td>
<td>word or phrase in the Occitan language or of an Occitan root</td>
</tr>
<tr class="odd">
<td>po</td>
<td>poitevin</td>
<td>word in the Poitevin dialect</td>
</tr>
<tr class="even">
<td>sup</td>
<td>supplied text</td>
<td>a word or heading supplied by Making and Knowing Project editors for clarity in computational analysis of the text</td>
</tr>
<tr class="odd">
<td>underline</td>
<td>underline</td>
<td>underlining in the original</td>
</tr>
<tr class="even">
<td>superscript</td>
<td>superscript</td>
<td>writing that appears in superscript in the original</td>
</tr>
<tr class="odd">
<td>ups</td>
<td>under paper strip</td>
<td>parts of the text that were covered by the paper strips placed around each page of the manuscript during its seventeenth-century re-binding in the Bethune bindings</td>
</tr>
</tbody>
</table>

The Project used unicode characters when they existed for the symbols
used by the writer.

Project members worked in Google Drive to enable simultaneous work until
2018, when Project data, including all transcribed, translated, and
encoded versions of the folio pages, were transferred to GitHub. While
working in Google Drive, Text Workshop members used working tools
constructed by Project Assistant Philip Cherian, and are listed here in
case they are useful to users of *Secrets of Craft and Nature*.

Google Drive Add-on, **Tag Insertion** — a digital tool for quickly grabbing a tag and inserting into the text.    

Google Drive Add-on, **XML Validator** — a digital tool for validating markup before moving on to the next recipe or folio.
