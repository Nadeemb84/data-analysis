Markdown for READMEs 
====================

[Markdown][fireball] for readmes is pretty popular.  So, I've given you a demo
here of all the markup we support. In some cases, I copied the text entirely from the Fireball Markdown docs. 

I didn't copy everything tho. For the entire docs explanation, you still need to go to the Fireball site.

- - -

Bitbucket does NOT support
================================

Please note, we don't support arbitrary HTML in Markdown, for example `<table>` tags. Instead, we use 
[safe mode][http://pythonhosted.org/Markdown/reference.html#safe_mode]. Safe mode requires that you replace, remove, or escape HTML tags appropriately.

- - -

# Heading Examples
You can create Atx-style headings by prefixing with a # (hash mark)

# Heading 1 markup  `# Heading 1`
# 
## Heading 2 markup  `## Heading 2`
## 
### Heading 3 markup   `### Heading 3`
### 
#### Heading 4 markup  `#### Heading 4`
#### 
##### Heading 5 markup  `##### Heading 5`
##### 
###### Heading 6 markup  `###### Heading 6`
###### 
You can also create Setext-style headings which have two levels.

Level 1 markup use an equal sign = (equal sign) 
==============================


	 Level 1 markup use an equal sign = (equal sign)   	 
	 ==============================
	 
Level 2 markup uses - (dashes) 
-------------


	Level 2 markup uses - (dashes) 
	-------------


- - -

PARAGRAPHS and BLOCKQUOTES
===========================

A paragraph is one or more consecutive lines of text separated by one or more
blank lines. A blank line contains nothing but spaces or tabs. Do not indent
normal paragraphs with spaces or tabs.

This is one paragraph.

This is a second.

	This is one paragraph.

	This is a second.

Markdown uses email-style > (greater than) characters for blockquoting. If you’re familiar with quoting passages of text in an email message, then you know how to create a blockquote in Markdown. It looks best if you hard wrap the text and put a > before every line:

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.


	> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
	> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
	> 
	> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
	> id sem consectetuer libero luctus adipiscing.
	
Blockquotes can be nested (i.e. a blockquote-in-a-blockquote):

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

	> This is the first level of quoting.
	>
	> > This is nested blockquote.
	>
	> Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists, and code blocks:

> ## This is a header.
> 
> 1.   This is the first list item.
> 2.   This is the second list item.
> 
> Here's some example code:
> 
>     return shell_exec("echo $input | $markdown_script");


	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");
	

- - -

Lists
=====

Markdown supports ordered (numbered) and unordered (bulleted) lists.  List markers typically start at the left margin, but may be indented by up to three spaces. List markers must be followed by one or more spaces or a tab.

Form bulleted lists with any of * (asterisk), + (plus), or - (dash). You can one or any or mix of these to form a list:

* Red 
+ Green 
- Blue


		* Red
		+ Green
		- Blue
	
Ordered lists require a numeric character followed by a . (period).

1. Item one
1. Item two 
1. Item three

		1. Item one
		1. Item two 
		1. Item three
    
Notice the actual value of the number doesn't matter in the list result. However, for readability better to use this markup:

		1. Item one
		2. Item two 
		3. Item three
		
Lists can be embedded in lists. List items may consist of multiple paragraphs. Each subsequent paragraph in a list item must be indented by either 4 spaces or one tab:

* Red 
+ Green 
	* dark  green 
	* lime	
- Blue		
	1. Item one
		1. subitem 1 
		1. subitem 2
	1. Item two 
	
	    This is is a first paragraph. 
	    
	    * Green 
		* Blue
	    
	    This is a second paragraph.
	    
	1. Item three
	
The code for these embedded lists or paragraphs is:

			* Red 
			+ Green 
				* dark  green 
				* lime	
			- Blue		
				1. Item one
					1. subitem 1
					1. subitem 2
				1. Item two 
	
					This is is a first paragraph. 
		
					* Green 
					* Blue
		
					This is a second paragraph.
		
				1. Item three

You can also embed blockquotes in a list.

* Green
> What is this?  It is embedded blockquote.  Mix 'em and match 'em.
* Blue
* Red

		* Green
		> What is this?  It is embedded blockquote.  Mix 'em and match 'em.
		* Blue
		* Red

- - -

Tables
=======


Bitbucket does not support `<html>` so you need to use theh - (dash) and the | (pipe) symbols to construct a table. The first line contains column headers. Separate columns with the pipe symbol.

The  second line must be a mandatory separator line between the headers and the content. Subsequent lines are table rows. Columns are always separated by the pipe (|) character.  For example this table:

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

Comes from this code:

	First Header  | Second Header
	------------- | -------------
	Content Cell  | Content Cell
	Content Cell  | Content Cell
	
	
You can only put simple lines in a table.

You can specify alignment for each column by adding colons to separator lines. A colon at the left of the separator line, left-aligns the column. A colon on the right, right-aligns the column. Add colons to both sides to center the column is center-aligned.

Right     | Left  | Center 
---------:|:----- |:-----:
Computer  | $1600 | one
Phone     |   $12 | three
Pipe      |    $1 | eleven

	Right     | Left  | Center 
	:---------| -----:|:-----:
	Computer  | $1600 |one
	Phone     |   $12 |three
	Pipe      |    $1 |eleven



- -  -


Syntax highlighting
=====================

You can also highlight snippets of text (Bitbucket uses the excellent [Pygments][]
library).

Here's an example of some Python code:

```
#!python
#
def wiki_rocks(text): formatter = lambda t: "funky"+t return formatter(text) ```


You can check out the source of this page to see how that's done, and make sure
to bookmark [the vast library of Pygment lexers][lexers], we accept the 'short
name' or the 'mimetype' of anything in there.




[fireball]: http://daringfireball.net/projects/markdown/ [Pygments]:
http://www.pygments.org/ [lexers]: http://pygments.org/docs/lexers/
