# Blogger templates

Blogger templates are used to render html content in [Blogger](https://www.blogger.com) pages. This section describes how to create blogger templates with step by step guide.

> Note: Tips to create blog templates are provided based on experience only. You can improvise the blogger template by adding more custom sections and widgets on your own.

## Basic template

Blogger template is an xml format style HTML code. Below is the example to start with basic blogger template with Header and main section.

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
 	<b:widget id='Header1' locked='true' title='Header Template (Header)' type='Header'></b:widget>
    </b:section>
    
    <b:section class='main' id='main'>
    	<b:widget id='HTML1' locked='true' title='Blog content' type='HTML'></b:widget>
    </b:section>
  </body>
</html>
  ```

## <b:section> tag

<b:section> is used to create a div section in blog page. Blogger website will expect atleast one <b:section> to compile the template. Refer [Blogger book](https://bloggerbook.blakbin.com/2018/11/blogger-bsection-tag.html) to know more about <b:section>

#### syntax:
```
<b:section  cond='EXPRESSION'
            class='STRING'
            id='STRING'
            name='STRING'
            preferred='BOOLEAN'
            showaddelement='BOOLEAN'
            maxwidgets='NUMBER'>
 
</b:section>
```

## <b:widget> tag

<b:widget> tag is used to customise the blogger page. Using <b:widget> we can configure the properties and display content based on user selection. Refer [Blogger book] (https://bloggerbook.blakbin.com/2018/11/blogger-bwidget-tag.html) to know more about widgets.

Widgets have [<b:widget-settings>](https://bloggerbook.blakbin.com/2018/11/blogger-bwidget-settings-tag.html) and [<b:includable>](https://bloggerbook.blakbin.com/2018/11/blogger-binclude-and-bincludable-tag.html) tags. <b:widget-settings> have the [<b:widget-setting>](https://bloggerbook.blakbin.com/2018/11/blogger-bwidget-settings-tag.html) which holds the customer specified fields.

> Note: Blogger html editor will create the <b:widget-settings> and <b:includable> for the provided widget. Editor will use the default content and values to generate these fields. We can modify them based on our design.

#### syntax
```
<b:widget id='STRING'
          cond='EXPRESSION'
          locked='BOOLEAN'
          version='NUMBER'
          title='STRING'
          type='WIDGET_TYPE'
          mobile='BOOLEAN'
          visible='BOOLEAN'>
 
</b:widget>
```

Widget have many types, Below are the possible [types](https://sites.google.com/site/templateofdoom/Home/blogger-template-widget-tag) of widget,
* BlogArchive
* Blog
* Feed
* Header
* HTML
* SingleImage
* LinkList
* List
* Logo
* BlogProfile
* Navbar
* VideoBar

Just add a widget with each type in Blogger template editor to understand more about widgets.



