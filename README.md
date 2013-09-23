Markdown for READMEs 
====================

[Markdown][fireball] for readmes is pretty popular.  So, I've given you a demo
here of all the markup we support.  In some cases words are taken directly from
the Markdown docs.

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

PARAGRAPHS
===========================

A paragraph is one or more consecutive lines of text separated by one or more
blank lines. A blank line contains nothing but spaces or tabs. Do not indent
normal paragraphs with spaces or tabs.

- - -

Lists
=====

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens — interchangably — as list markers:

* Red 
+ Green 
- Blude


		* Red
		+ Green
		- Blue
	
    
    


- - -

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
