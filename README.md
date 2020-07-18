# Blogger templates

Blogger templates are used to render html content in [Blogger](https://www.blogger.com) pages. This section describes how to create blogger templates with step by step guide.

## Basic template

Below is the example to start with basic blogger template with Header and main section.

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr' xmlns:og='http://ogp.me/ns#'>
  <head>

    <meta content='width=device-width, initial-scale=1, minimum-scale=1, maximum-scale=1' name='viewport'/>
    <b:include data='blog' name='all-head-content'/>

    <b:skin><![CDATA[
    /* Variable definitions
    =======================*/

    ]]></b:skin>

    <b:if cond='data:view.isLayoutMode'>
      <b:template-skin>
        <![CDATA[
        /*------Layout (No Edit)----------*/

        /*------Layout (end)----------*/
        ]]>
      </b:template-skin>
    </b:if>
  </head>
  <body>
    <b:section class='header' id='header' maxwidgets='1'>
		<b:widget id='Header1' locked='true' title='Basic Blogger Template (Header)' type='Header'></b:widget>
	</b:section>
    
    <b:section class='main' id='main'>
    	<b:widget id='HTML1' locked='true' title='Blog content' type='HTML'></b:widget>
    </b:section>
  </body>
</html>
  ```
