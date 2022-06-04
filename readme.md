![Awesome Exporter](https://modocodo.studio/work/awesome-exporter-logo.jpg)

<br />

Awesome Exporter for Adobe InDesign gives studios and creatives complete control over document exports via an intuitive UI and flexible template language – creating JPG, PDF, PNG, EPS and INDD assets for brand libraries, content for websites, and multilingual production artwork is now quick, simple and visual. Easily select pages, spreads, layouts and sections by their attributes, styles and content, then name and export them using a powerful template syntax.

[Download from Adobe Exchange](https://exchange.adobe.com)

<br />


![Awesome Exporter UI](https://modocodo.studio/hosted/awesome-exporter-ui-main-window-01.png)


<br /><br />


## Features

#### Range Queries
* Quickly select layouts, sections, spreads, pages and layers by name, attribute, style or content.
* Select exactly what you need using page numbers, ranges and new query tags.
* Layering tags allow you to export file variations and multiple languages from a single source file by selecting content from different base and variable layers.
* Query collections can be used to split content from a single InDesign document into multiple file exports.
* The range builder tool helps to create the accurate ranges.

#### Filename Templates
* Name each export using beautifully simple and flexible template tags.
* Conditional tags and 'look-backwards' tags offer fine control and cut down on duplicated content.
* The template builder tool helps to create perfect filenames.

#### Export Formatting
* All standard export format settings are available for JPG, PDF, PNG, EPS and INDD files.
* Settings have been extended to allow multiple version of resolutions, qualities and other settings.
* Export single pages, spreads and combined files.

#### Presets
* Save ranges, templates and settings as shareable JSON presets.
* Attach presets to documents using JSON sidecar files.
* Create local and remote presets – ideal for sharing among a creative team.
* Simple to use and linked directly to your workflow.
* Batch exports and detailed export reporting.

#### Live Previews & Tag Builders
* Live preview of exports as you create them.
* Range, filename and tag builder interfaces help build accurate range queries and filename templates.


<br /><br />


## User Guide

### Range Queries
Range queries can be standard ranges, absolute page references, query tags, or a mix of all three. The range builder dialog lists all available layouts, sections and pages along with a tag builder tool to quickly create custom queries based on page content and attributes.

![Awesome Exporter Range Builder UI](https://modocodo.studio/hosted/awesome-exporter-ui-range-builder-window-01.png)

<br />

#### Standard Range Queries

##### Select by Page Number

The simplest query is an absolute page number query. ```+6``` will select page 6. ```+3-``` selects page 3 to the end of the document and ```+5-+8``` selects pages 5 to, and including, 8.

##### Select by Layout

Layouts can be selected by entering the layout reference, for example; ```A4``` would export all pages from a layout named 'A4'.

##### Select by Section

Sections can be selected by entering the layout name and followed by the section name; ```A4:One``` will export all pages in a section named 'One' from the 'A4' layout.

When using layouts or sections the single dash character prefix/postfix extends to the start/end of that particular layout or section. Using a double dash character extends to the start/end of the document.

##### Select by Page Nane

Page name references like ```A4:One:2``` woulod select page 2 from section ```One``` in layout ```A4```

<br />

#### Advanced Queries & Tags

Query tags allow pages to be selected by attribute, item style and item content – introducing powerful new ways to filter pages and export only the content required, while retaining the integrity and simplicity of your source documents.

The following examples assume your test document has:

* A textframe named 'Code' somewhere on one or more pages and that textframe contains the characters '123' as content.
* An image named 'Cover' somewhere on one of your documents pages which links to a file named 'Cover Image.jpg'.
* A page with the colour label red and a page with the colour label green.
* A paragraph style named 'Title', applied to some text on your page.
* A layer named 'EN' with some content in English.
* A layer named 'FR' with some content in French.

If you're testing Awesome Exporter on your own existing document, you'll need to adjust the names of the example tags as required to fit your document. Or, download and jump right in to exporting your documents now.

Don't forget, the range builder and template builder interfaces help to take the guesswork out of tag creation by providing information based on the actual content inside your document.

<br />

##### Range Tag Comparison Operators

Operators are used with tags in range queries to compare tag data to a value you have specified. For example, ```<Page:T:Code:Text|=|'123'>``` grabs the text data from a textframe and checks to see if it matches '123'. ```<Page:Colour|[Any]>``` grabs the page colour and checks to see if it has been set to any colour iin the list.

Awesome Exporter supports the following data comparison operators:

##### Operator Reference

| Operator | Description | Text | Numeric | Layer | Attribute | Instance |
| - | - | - | - | - | - | - | 
| ```=``` | Equal to. | ✓ | ✓ | ✓ |  |  |
| ```!=``` | Not equal to. | ✓ | ✓ | ✓ |  |  |
| ```>``` | Greater than. | ✓ | ✓ |  |  |  |
| ```>=``` | Greater than or equal to. | ✓ | ✓ |  |  |  |
| ```<``` | Less than. | ✓ | ✓ |  |  |  |
| ```<=``` | Less than or equal to. | ✓ | ✓ |  |  |  |
| ```Includes``` | Does the tag include... | ✓ | ✓ | ✓ |  |  |
| ```!Includes``` | Does the tag not include... | ✓ | ✓ | ✓ |  |  |
| ```Starts``` | Does the value start with... | ✓ | ✓ | ✓ |  |  |
| ```!Starts``` | Does the value not start with... | ✓ | ✓ | ✓ |  |  |
| ```Ends``` | Does the value end with... | ✓ | ✓ | ✓ |  |  |
| ```!Ends``` | Does the value not end with... | ✓ | ✓ | ✓ |  |  |
| ```IsEven``` | Is the value an even number. |  | ✓ | ✓ |  |  |
| ```IsOdd``` | Is the value an odd number. |  | ✓ | ✓ |  |  |
| ```IsPrime``` | Is the value a prime number. |  | ✓ | ✓ |  |  |
| ```RegExp``` | RegExp value test is true. | ✓ |  |  |  |  |
| ```!RegExp``` | RegExp value test is false. | ✓ |  |  |  |  |
| ```Length=``` | Length equal to. | ✓ | ✓ |  |  |  |
| ```Length!=``` | Length not equal to. | ✓ | ✓ |  |  |  |
| ```Length>``` | Length greater than. | ✓ | ✓ |  |  |  |
| ```Length>=``` | Length greater than or equal to. | ✓ | ✓ |  |  |  |
| ```Length<``` | Length less than. | ✓ | ✓ |  |  |  | 
| ```Length<=``` | Length less than or equal to. | ✓ | ✓ |  |  |  | 
| ```[Any]``` | Attribute is set to anything. |  |  |  | ✓ |  |
| ```[None]``` | Attribute is set to '[None]'. |  |  |  | ✓ |  | 
| ```[Exists]``` | Referenced object instance found. |  |  |  |  | ✓ |
| ```[Missing]``` | Referenced object instance not found. |  |  |  |  | ✓ |

<br />

Page selection examples;

##### Select Page by Textframe Content

```<Page:T:Code:Text|=|'123'>``` - Selects pages with a textframe named 'Code' containing the value equal to '123'.

```<Page:T:Code:Text|!=|'123'>``` - Selects any pages with a textframe named 'Code' which don't contain the value of '123'.

##### Select Page by Image Link

```<Page:I:Cover:Filename|=|'Cover Image.jpg'>``` - Selects any pages with an image named 'Cover' whose filename is equal to 'Cover Image.jpg'

##### Select Page by Image Extension

```<Page:I:Cover:Extension|=|'tif'>``` - Exports all pages where the extension of an image frame named 'Cover' is a tiff file.

##### Select Page by Absolute Index and by Colour

```+3,<Page:Colour:Value|!=|'Red'>``` - This query selects page 3 plus any pages which don't have a red colour label.

##### Multilingual Layered Pages by Paragraph Style

```<Page:P:Title:Text|~|'ABC'>, <Layering|=|Green|=|'EN', 'FR'>```

Export any pages with a paragraph style named 'Title' where the content is similar to 'ABC'. Green layers will be used as the base layers and layers named 'EN' and 'FR' used as the variable layers. Layer EN could contain English copy and 'FR' could contain French copy to demonstrate a file with multilingual content.

##### Select by Parent Page

```<Page:Parent:Name|[Any]>```

Expor any pages with any parent page applied.

##### Select by Page Width

```<Page:Width:Value|>|'200'>```

Expor any pages with a width greater than 200 units of the document's specified unit.

<br />

#### Conditional 'And' Tags

Conditional tags give you finer control of range queries by allowing you to select content based on multiple elements being true. Conditional tags use braces ```{``` ```}``` to wrap multiple references. Here's an example:

Selects pages with the colour green **and** parent page 'A':
```<{Page:Colour:Value|=|'Green'}{Page:Parent:Reference|=|'A'}>```

Selects all spreads with a textframe called 'Title' (data is not important) **and** with a width less than 200:
```<{Spread:T:Title|[Exists]}{Spread:Width|<|'200'}>```

Conditional queries can be used with any tag. The range builder UI provides a simple way of creating conditional range query tags.

<br />

#### Base and Variable Layers

```<Layering>``` tags specify which base layers and variable layers should be exported in a query and allow you to create content variations and multilingual files from a single document.

In this example we first select all document pages with the ```<All>``` range query tag. We'll then create two separate exports for each selected page, one using the 'EN' layer and one using the 'FR' layer. The 'Background' layer is used in all exports: ```<All>, <Layering|=|'Background'|=|'EN','FR'>```

The ```<Layering>``` tag can also be used to select specific base layers without using variable layers. In this example we select all document pages and all layers coloured red for export: ```<All>, <Layering|=|Red>```

Layers can also be selected by name: ```<Layering|=|'Layer1'>``` and by colour: ```<Layering|=|Grey>```.


<br /><br />


#### Range Collections

Collections are a great tool to use when your document contains multiple or related versions of content which needs to be split at artworking/export stage.

Multiple range queries can be combined into collections using round brackets ```(``` ```)```. For example, two collections can be defined by wrapping page ranges inside round brackets: ```(+2)(+1,+3)```. This would return an export list containing page 2 and an export list containing page 1 and 3.

Collections can contain both ranges and tags. Here we create a collection which selects pages 1, 2 and 3 plus a collection which selects all pages with the parent named 'Square': ```(+1-+3)(<Page:Parent:Name|=|'Square'>)```

Collections can also be labelled by adding a label to the start of the collection. Collection labels are wrapped inside ```*``` characters as follows; ```(*Collection One* +1-+3) (#Collection Two# <Page:Parent:Name|=|'Square'>)```. These labels can then be used in the filename template using the ```<Collection:Label>``` tag.


<br /><br />


### Filename Templates

![Awesome Exporter Template Builder UI](https://modocodo.studio/hosted/awesome-exporter-ui-template-builder-window-01.png)

Filenames are built using the same syntax as range queries with just a few subtle differences and additional features. Each filename tag returns data which is applied to each page selected for export. The tags can refer to page data or page attributes, allowing you to use styled and named document data in your filenames.

Here's some examples:

```<Document:Name><|><Export:Index>``` - creates a filename using the documents name and a sequential export number. A spacer is used between the tags.

```Web</><Document:Name><|><Export:Index>``` - creates the same filename as above but this time places the export inside a folder named 'Web'.. A spacer is used between the tags and a slash separator is used to split the template into a folder and a file.

```<Page:T:Title:Text>``` - uses the content of a textframe named 'Title' for each filename.

<br />

##### Tag Data Lookback

Certain data, like chapter titles or section headers, likely won't appear on each page in your document, but you may want to use them in all of your filenames - this is where the tag lookback syntax ```^``` can help. By adding the lookback symbol to a tag, the most recent data found for that tag can be used by each subsequent export, even if a page doesn't contain data from the tag.

For example: 

```<^Page:T:Chapter:Text>``` - uses the content of a textframe named 'Chapter' for each filename. This textframe might only appear on certain pages, but each page can use the most recent data because the lookback symbol ```^``` has been added.

```<^Page:P:Section:Text>``` - uses the content of a paragraph style named 'Section' for each filename. Again, this style might only appear on certain pages, but each page can use the most recent data because the lookback symbol ```^``` has been added. The data used by the tag is updated each time actual data is found on a page.

<br />

##### Conditional Tags

Sometimes when tags don't return data you'll want to use an alternative, this is where conditional tags help. Similar to the conditional tags in range queries, conditional tags in filename queries use the same braces ```{``` ```}``` to wrap multiple references. This time however, the exporter tries to use each part of the tag until it finds some data - referred to as an 'or', i.e use part one **or** part two, depending on the data.  

Examples:

```<{Page:T:Code:Text}{Page:Parent:T:Code:Text}>``` – uses the page textframe named 'Code' if it exists, or uses the parent page textframe named 'Code' as a fallback.

```<{Page:T:Code:Text}{'Missing'}+>``` - uses the page textframe named 'Code' if it returns data, or uses the string 'Missing' as a fallback.

<br />

##### Tag Labelling

Any filename template tag can be lablled using the asterix ```*``` wrapper at the start of the tag as follows: ```<*NAME*Document:Name>``` - this tag would have the id of ```NAME```. Lables give tags unique identities which can be used later by modifier queries to run functions against the tags value. 

<br />

##### Validity Checking (Tag Linking)

Tags can check surrounding tags for validity using the ```+``` modifier. This allows you to only use a tag if the tag next to it has been used. You can use this functionality to 'chain' tags together and build filenames depending on the data available. 

Examples:

```<Document:Name><+|+><Page:T:Code:Text>``` – here the spacer is only used if the tags to both the left and right are valid and contain data. If the ```<Document:Name>``` or ```<Page:T:Code:Text>``` don't return data, the spacer tag is ignored. Spacer tags can check to the left ```<+|>```, to the right ```<|+>``` and to both sides ```<+|+>```. All other tags just check to the left side ```<+File:Name>```.

Here we build a filename where each tag checks the previous tag: ```<Document:Name><+|><+Page:T:Part1:Text><+|><+Page:T:Part2:Text><+|><+Page:T:Part3:Text>```. If part one of the tag is missing, the export won't use the separators or tags which come after that tag.

Validity checkers can be used with conditional tags too 


<br /><br />


### Filename Modifier Queries

![Awesome Exporter Range Builder UI](https://modocodo.studio/hosted/awesome-exporter-ui-modifiers-builder-window-01.png)

Modifier tags allow functions to be run against filename template tags, letting you manipulate and fine tune the data used in the filename. Tags can be targetted by Multiple modifiers can be run against each tag, giving complete control over filename formatting.

The filename template can be targetted in a number of ways and functions can be applied to tags, labels, folders, files or the full path. Each function performs a modification of the data returned by it's target:

<br />

##### Modifier Targets

| Target  | Description |
| - | - |
| ```<Path>``` | Apply a modifier to the full export path. |
| ```<Folder>``` | Apply a modifier to just the folder part of the export path. |
| ```<File>``` | Apply a modifier to just the file part of the full export path. |
| ```<Tag>``` | Apply a modifier to a specific tag reference. |
| ```<*Label*>``` | Apply a modifier to a specific labelled tag. |

<br />

##### Modifier Function Reference

| Function | Description | Parameters |
| - | - | - |
| ```Replace``` | Replace a string with another string. |
| ```Split``` | Split tag value by delimeter and return part of it. |
| ```Pad``` | Pad the tag value using a specified amount of characters. |
| ```Insert``` | Insert data at a specified point. |
| ```Prefix``` | Add to the start of a tag value. |
| ```Suffix``` | Add to the end of a tag value. |
| ```Uppercase``` | Convert tag or label to uppercase. |
| ```Lowercase``` | Convert tag or label to lowercase. |
| ```Titlecase``` | Convert tag or label to titlecase. |
| ```Increase``` | Increase the numeric value of a tag. |
| ```Decrease``` | Decrease the numeric value of a tag. |
| ```AsWord``` | Convert a numeric tag value to a word. |
| ```Add``` | Add to the numeric value of a tag. |
| ```Subtract``` | Subtract from the numeric value of a tag. |
| ```Multiply``` | Multiply the numeric value of a tag. |
| ```Divide``` | Divide the numeric value of a tag. |
| ```Length``` | Get the length of the tags value. |

<br />

##### Examples

Convert the file name to uppercase ```<File|Uppercase>```.
Convert the folder name to uppercase ```<Folder|Uppercase>```.
Convert the entire file path to uppercase ```<Path|Uppercase>```.
Convert a labelled tag to uppercase ```<*ABC*|Uppercase>```.
Convert any occourance of ```<Document:Name>``` tags to uppercase ```<Document:Name|Uppercase>```

Some functions can also take parameters. The replace function takes three; (1) an operator, (2) a string to find and (3) a replacement string.

* Replace '72' with 'Web' for all ```<JPG:Resolutions>``` tags: ```<JPG:Resolution|Replace|=|'72'|'Web'>```
* Replace '300' with 'Web' for all ```<JPG:Resolutions>``` tags: ```<JPG:Resolution|Replace|=|'300'|'Print'>```
* Replace '72' with 'Web' for all tags labelled 'ABC': ```<*ABC*|Replace|=|'72'|'Web'>```

Another function, Split, works well to extract and use specific parts of a tags data. In this example we assume the document name is 'Web Assets - July - Creative Team' and we only want to use the first part of the document name. We would use the ```<Document:Name>``` tag in the filename template, and use the split function to modify it: ```<Document:Name|Split|' - '|'1'>```. This query would return 'Web Assets' from the document name. Changing the modifier argument from '1' to '2' would return 'July'.

<br />

#### Indexed Labels

Indexed labels allow you to target specific exports with modifier functions. To create an indexed lablel simple add the ```#``` character to the end of any filename template tag label. You can then use variations of this 

Let's assume we have the following filename template ```<*Tag-#*Document:Name>```. This indexed tag allows us to run the following modifiers:

* Uppercase the tag labeled 'Tag-#': ```<*Tag-#*Uppercaase>```
* Uppercase all exports in collection 1 for the tag labeled 'Tag-#': ```<*Tag-1*Uppercaase>```
* Uppercase the single export in collection 1, page 3 for the tag labeled 'Tag-#': ```<*Tag-1-3*Uppercaase>```
* Uppercase the single export in collection 1, page 8 for the tag labeled 'Tag-#': ```<*Tag-1-8*Uppercaase>```

<br />

#### Counters

Counters are a special type of function which can be applied to labelled filename tags only. They are used to return a numeric value based on the occurrence of objects, attributes or content in the document, allowing exports to be dynamically numbered and indexed based on any document content. 

In the following examples we will assume the document has a textframe named 'Chapter', it will be referenced in the filename and labelled for use as a counter. *Filename*: ```<*Chapter*Page:T:Chapter:Text>```. *Modifier*: ```<*Chapter*|Counter>```

We'll use the labeled tag ```<*Chapter*>``` in the template.

And modify the labeld tag in the modifiers: ```<*Chapter*|Counter>```

Counters can also use the value of tags:

Again we'll use the labeled tag ```<*Chapter*>``` in the template.

This time modify the labeld tag every time a different text value is encountered: ```<*Chapter*|Counter>```

Counters can be applied to any tag or label in the filename template.

<br />

#### Modifier If Conditions

Modifier tags can be extended further but adding an 'if condition' to the end, causing modifiers to run only when specific conditions are met. In this example we'll convert the ```<Document:Name>``` tag to uppercase **only if the document file name is 'BrandAssets.indd'**: ```<Document:Name|Uppercase|If|Document:File|=|'BrandAssets.indd'>```

In this example we append the word 'Web' to the end of the template path, **only if the file being exportd is a JPG with the resolution of '72'**: ```<Path|Suffix|'Web'|If|JPG:Resolution|=|'72'>```


<br /><br />


### Presets and Preset Locations

![Awesome Exporter Range Builder UI](https://modocodo.studio/hosted/awesome-exporter-ui-save-preset-window-01.png)

Awesome Exporter contains a fully featured preset system allowing presets to be created, modified, moved and deleted all from the UI. Presets allow range, format, template and modifier configurations to be saved globally, against a specific document or in a custom location to be used at a later date. All presets are stored in JSON format to allow easy editing and portability.

<br />

##### Preset Locations

| Location | Description |
| - | - |
| Quick Exports | Default quick exports. Can be added and modified. |
| Document Sidecars | A JSON preset file with the same name as your document, in the same folder. |
| Custom Location | A local or remote JSON file, manually added by you. |

<br /><br />


### A Note on File Structure

![Awesome Exporter Example Page Structure](https://modocodo.studio/hosted/awesome-exporter-ui-textframe-tag-in-page-slug-01.png)

There's no one-fit-all solution to creating 'taggable' content in your files and Awesome Exporter doesn't require you to change the structure or layout in your document. For some use-cases though it is worth considering how you will structure your document.

One example would be if you're creating images for asset libraries; each page or spread could contain a variable segment of the final filename in a textframe. Placing these textframes in a page or spread slug would allow them to be used as tags without appearing in your exports. Another solution would be to add them to a hidden layer which can be ignored when exporting.




<br /><br />


### Tag Reference

A list of tags avaialble in Awesome Exporter available for range queries and filename templates. Some tags can only be used in range queries and some only used in filename queries. The tick marks show where each tag can be used. Remember the range query builder ui and filename template builer ui can be used to build the tags you need.

##### Selectors
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<All>```	| Select all pages in the document | Page Range | ✓ | |
| ```<Even>``` | Select all even numbered pages | Page Range | ✓ | |
| ```<Odd>```	| Select all odd numbered pages | Page Range | ✓ | |
| ```<Prime>```	| Select all pages with prime numbers | Page Range | ✓ | |

##### Folder
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Document:Folder>``` | Document folder path | String | ✓ | ✓ |
| ```<Document:File>``` | Document file path | String | ✓ | ✓ |
| ```<Document:Name>``` | Document name | String | ✓ | ✓ |
| ```<Document:Extension>``` | Document extension | String | ✓ | ✓ |
| ```<Document:Created>``` | Document creation date/time. | String | ✓ | ✓ |
| ```<Document:Modified>``` | Last modified date/time | String | ✓ | ✓ |

##### File
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<File:Name>``` | File name | String | ✓ | ✓ |
| ```<File:Extension>``` | File extension | String | ✓ | ✓ |
| ```<File:Created>``` | File creation date/time. | String | ✓ | ✓ |
| ```<File:Modified>``` | File modified date/time | String | ✓ | ✓ |

##### System
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Folder:Name>``` | Folder name | String | ✓ | ✓ |
| ```<Folder:Created```> | Folder creation date/time. | String | ✓ | ✓ |
| ```<Folder:Modified>``` | Last modified date/time | String | ✓ | ✓ |

##### User
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<File:Name>``` | File name | String | ✓ | ✓ |
| ```<File:Created>``` | File creation date/time. | String | ✓ | ✓ |
| ```<File:Modified>``` | File modified date/time | String | ✓ | ✓ |

##### Variables
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<File:Name>``` | File name | String | ✓ | ✓ |
| ```<File:Created>``` | File creation date/time. | String | ✓ | ✓ |
| ```<File:Modified>``` | File modified date/time | String | ✓ | ✓ |

##### Content Containers
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Layouts:Count>``` | Number of layouts in the doucment. | String | ✓ | ✓ |
| ```<Sections:Count>``` | Number of sections in the document. | String | ✓ | ✓ |
| ```<Spreads:Count>``` | Number of spreads in the document. | String | ✓ | ✓ |
| ```<Pages:Count>``` | Number of pages in the document. | String | ✓ | ✓ |

##### Layering
| Reference | Description | Range | Template |
| - | - | - | - |
| ```<Layering|=|XXX|=XXX>```<br />```<Layering|=|XXX>``` | Specify base and variable layers.<br />Specify base layers. | ✓<br />✓ |  
| ```<Layering:Base:Name>``` | Base layers query, comma separated. |  | ✓ |
| ```<Layering:Variable:Name>``` | Variable layers query, comma separated. |  | ✓ |

##### Preset Details
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Preset:Name>``` | Preset name. | String | ✓ | ✓ |
| ```<Preset:Description>``` | Preset description. | String | ✓ | ✓ |
| ```<Preset:Author>``` | Preset author. | String | ✓ | ✓ |
| ```<Preset:Modified>``` | Is the preset modified? | Y/N | ✓ | ✓ |
| ```<Preset:Location:Label>``` | Preset location label. | String | ✓ | ✓ |
| ```<Preset:Location:Type>``` | Preset location type. | String | ✓ | ✓ |
| ```<Preset:Location:Path>``` | Preset location path. | String | ✓ | ✓ |
| ```<Preset:Folder:Name>``` | Preset folder name. | String | ✓ | ✓ |
| ```<Preset:Folder:Created>``` | Preset folder creation date. | String | ✓ | ✓ |
| ```<Preset:Folder:Modified>``` | Preset folder modification date. | String | ✓ | ✓ |
| ```<Preset:File:Name>``` | Preset file name. | String | ✓ | ✓ |
| ```<Preset:File:Created>``` | Preset file creation date. | String | ✓ | ✓ |
| ```<Preset:File:Modified>``` | Preset file modification date. | String | ✓ | ✓ |

##### Collections and Exports
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Range:Index>``` | Position in the range query | Number | 

##### Page Attributes
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Page:Name>``` | Page name. | String | ✓ | ✓ |
| ```<Page:Number>``` | Page number. | Number | ✓ | ✓ |
| ```<Page:Reference>``` | Page reference. | String | ✓ | ✓ |
| ```<Page:Index>``` | Page index. | Number | ✓ | ✓ |
| ```<Page:Layout>``` | Page layout. | String | ✓ | ✓ |
| ```<Page:Bookmark:Name>``` | Bookmark name. | String | ✓ | ✓ |
| ```<Page:Parent:Reference>``` | Parent page reference, (combination of prefix and name). | String | ✓ | ✓ |
| ```<Page:Parent:Prefix>``` | Parent page prefix. | String | ✓ | ✓ |
| ```<Page:Parent:Name>``` | Parent page name. | String | ✓ | ✓ |
| ```<Page:Colour:Value>``` | RGB colour value of the page. | String | ✓ | ✓ |
| ```<Page:Colour:Type>``` | Returns 'UI' if the colour is a colour label or 'User' if the colour has been set to a custom RGB value. | String | ✓ | ✓ |
| ```<Page:Layout:Name>``` | Parent page reference, (combination of prefix and name). | String | ✓ | ✓ |
| ```<Page:Section:Name>``` | Parent page reference, (combination of prefix and name). | String | ✓ | ✓ |
| ```<Page:Section:Prefix>``` | Parent page prefix. | String | ✓ | ✓ |
| ```<Page:Section:Marker>``` | Parent page name. | String | ✓ | ✓ |
| ```<Page:Width:Value>``` | Numeric page width value. | Number | ✓ | ✓ |
| ```<Page:Width:Unit>``` | Page width unit (i.e. px or mm). | String | ✓ | ✓ |
| ```<Page:Height:Value>``` | Numeric page height value. | Number | ✓ | ✓ |
| ```<Page:Height:Unit>``` | Page height unit (i.e. px or mm). | String | ✓ | ✓ |

##### Spread Attributes
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Spread:Pages>``` | Number of pages in the spread. | ✓ | ✓ |
| ```<Spread:Index>``` | Current spread number. | ✓ | ✓ |

##### Date and Time
| Reference | Description | Range | Template |
| - | - | - | - |
| ```<Date:Weekday>``` | Number | Name of the day. | ✓ | ✓ |
| ```<Date:Day>``` | Number | Numeric day of the month. | ✓ | ✓ |
| ```<Date:Month>``` | Number | Numeric month number. | ✓ | ✓ |
| ```<Date:Year>``` | Number | Numeric year. | ✓ | ✓ |
| ```<Time:Millisecond>``` | Number | Current millisecond. | ✓ | ✓ |
| ```<Time:Second>``` | Number | Current second. | ✓ | ✓ |
| ```<Time:Minute>``` | Number | Current minute. | ✓ | ✓ |
| ```<Time:Hour>``` | Number | Current hour. | ✓ | ✓ |

##### Textframes
| Reference | Description | Data| Range | Template |
| - | - | - | - | - |
| ```<Document:T:XXX:Text>```<br />```<Layout:T:XXX:Text>```<br />```<Section:T:XXX:Text>```<br />```<Spread:T:XXX:Text>```<br />```<Page:T:XXX:Text>``` | Named text frame text. | String | ✓ | ✓ |

##### Images
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Document:I:XXX:Name>```<br />```<Layout:I:XXX:Name```><br />```<Section:I:XXX:Name>```<br />```<Spread:I:XXX:Name>```<br />```<Page:I:XXX:Name>``` | Named image file name. | String | ✓ | ✓ |

##### Paragraphs
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Document:P:XXX:Text>```<br />```<Layout:P:XXX:Text>```<br />```<Section:P:XXX:Text>```<br />```<Spread:P:XXX:Text>```<br />```<Page:P:XXX:Text>``` | Styled paragraph text. | String | ✓ | ✓ |

##### Characters
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Document:C:XXX:Text>```<br />```<Layout:C:XXX:Text>```<br />```<Section:C:XXX:Text>```<br />```<Spread:C:XXX:Text>```<br />```<Page:C:XXX:Text>``` | Styled character text. | String | ✓ | ✓ |

##### JPG Related Tags
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<JPG:Resolution>``` | JPG resolution setting. | Number |  | ✓ |
| ```<JPG:Quality>``` | JPG quality setting. | Number |  | ✓ |
| ```<JPG:Colour Space>``` | JPG colour space setting. | String |  | ✓ |
| ```<JPG:Encoding>``` | JPG encoding setting. | String |  | ✓ |
| ```<JPG:Anti Alias>``` | JPG anti alias setting. | Y/N |  | ✓ |
| ```<JPG:Use Document Bleed>``` | JPG document bleed setting. | Y/N |  | ✓ |

##### PDF Related Tags
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<PDF:Preset>``` | PDF preset name. | String |  | ✓ |

##### PNG Related Tags
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<PNG:Resolution>``` | PNG resolution setting. | String |  | ✓ |
| ```<PNG:Quality>``` | PNG quality setting. | Number |  | ✓ |
| ```<PNG:Colour Space>``` | PNG colour space setting. | String |  | ✓ |

##### EPS Related Tags
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<EPS:PostScript Level>``` | EPS PostScript level setting. | String  |  | ✓ |
| ```<EPS:Colour>``` | EPS colour setting. | String |  | ✓ |
| ```<EPS:Embed Fonts>``` | EPS embed fonts setting. | Y/N |  | ✓ |
| ```<EPS:Data Format>``` | EPS data format setting. | Y/N |  | ✓ |

##### Preset Tags
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Preset:Name>``` | Preset name. | String | | ✓ |
| ```<Preset:Location>``` | Preset location name. | String | | ✓ |
| ```<Preset:Description>``` | Preset description. | String | | ✓ |
| ```<Preset:Modified>``` | Is the preset modified? | String | | ✓ |

##### Collection
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Collections:Count>``` | Number of collections. | Number | | ✓ |
| ```<Collections:Exports>``` | Number of exports in all collections. | Number | | ✓ |
| ```<Collection:Label>``` | Current collection label. | String | | ✓ |
| ```<Collection:Index>``` | Current collection number. | Number | | ✓ |
| ```<Collection:Exports>``` | Number of exports in the current collection. | Number | | ✓ |

##### Export Tags
| Reference | Description | Data | Range | Template |
| - | - | - | - | - |
| ```<Exports:Count>``` | Total number of exports. | Number | | ✓ |
| ```<Export:Type>``` | Current export type. | String | | ✓ |
| ```<Export:Format>``` | Current export format. | String | | ✓ |
| ```<Export:Layout>``` | Current export layout. | String | | ✓ |
| ```<Export:Index>``` | Current export number. | Number | | ✓ |

##### Spacers
*Spacers can be defined by each preset and changed in the modifier UI*
| Reference | Description | Range | Template |
| - | - | - | - |
| ```<|>```	 | One spacer. |  | ✓ |
| ```<||>``` | Two spacers. |  | ✓ |
| ```<|||>``` | Three spacers. |  | ✓ |
| ```<||||>``` | Four spacers. |  | ✓ |
| ```<|||||>```	 | Five spacers. |  | ✓ |

##### String Wrapper
*String tags allow strings to be wrapped inside a tag making them editable my modifier queries.*
| Reference | Description | Range | Template |
| - | - | - | - |
| ```<''>``` | String tag. |  | ✓ |


<br /><br />


### Application Options

<img src="https://modocodo.studio/hosted/awesome-exporter-ui-options-window-01.png" width="600" />

##### General Options

| Name | Description |
| - | - |
| Document Pages Threshold | The number of document pages can slow down performance once the document page count reaches a high number (depending on complexity). This number will depend on your system configuration. This setting lets you control or turn off an alert for high document pages. |
| Selected Pages Threshold | Selected pages can slow down performance once the document page count reaches a high number. This number will depend on your system configuration. This setting lets you control or turn off the selected pages feature. |
| Live View Threshold | Live previewing changes in real time can slow down performance once the export preview count reaches a high number. This number will depend on your system configuration. This setting lets you control or turn off the live view feature. |
| Export Threshold | Exporting a large number of files can take a long time. This setting lets you control or turn off an alert for high number of file exports. |

##### Export Options

| Name | Description |
| - | - |
| Show Message When Exports Finish | Turn on/off the message displayed when exports have completed. |
| Save and Close Documents After Export | If enabled, Awesome Exporter will save and close the document once exports have completed. |

##### Filename Options

| Name | Description |
| - | - |
| Remove Invalid Characters | If enabled, all invalid characters will be removed from all export filenames |

##### Preset Options

| Name | Description |
| - | - |
| Label Recently Exported Preset | If enabled, and if the preset exists, the most recently exported preset for the active document will be labelled in the preset selection list |
| Preferred Preset Location on Startup | When starting Awesome Exporter you can select the default preset location:<br /><br />Auto: The app will select the most recent and relevant.<br />Document Recent: The most recent document location, if available.<br />Sidecar Recent: The most recent location listed in the document sidecar file, if available.<br />Options Recent: The most recent locations listed in the globals options file.<br />Quick Exports: Always show the Quick Export list at startup.<br /><br />If the option you select doesn't return a list of presets, Awesome Exporter will display the most relevant presets for you. |

<br /><br />


### Problems and Bug Reports

New versions of Awesome Exporter are in active development and if you're using the extension then I'd love to hear your feedback, suggestions and bug reports. If somethings not working, please get in touch before posting a review and hopefully I'll be able to help: [hello@modocodo.studio](mailto:hello@modocodo.studio?subject=Awesome%20Exporter%20Customer%20Feedback).

<br /><br />


### Thank you

[Built by Tim Rickaby](https://timrickaby.com) at [Modocodo Studio](https://modocodo.studio)
[hello@modocodo.studio](mailto:hello@modocodo.studio?subject=Awesome%20Exporter).

© 2022