## Overview ##

The Wordpress Google calendar plugin allows for the integration of a Google calendar into a Wordpress blog.

We are currently at release 0.8.5. You can download it at the right ===>.

For release notes, please see the [change log](ChangeLog.md).

## Installation ##

This section describes how to install the plugin and get it working.

  1. Request Google GDATA API key (see link below)
  1. Upload the contents of the ZIP file to the `/wp-content/plugins/` directory
  1. Activate the plugin through the Plugins menu
  1. Configure your GDATA API key in the plugin options panel
  1. Configure a Google calendar in the plugin options panel
  1. Configure the option to render the description field as Wiki markup
  1. Create a page and add the 'show-wpng-calendar' custom field with the number of weeks you want to be displayed
  1. Add the widget to your sidebar and configure the title and number of events to display

The plugin-in requires a valid [Google GDATA API key](http://gd.google.com/html/signup.html). Only one calendar can be associated with the plug-in (want more?, request an enhancement).

_NOTE: The API key must correspond to your domain URL. Read this snippet from the Google API site for more information:_

_A key is associated with a website. If you want to use the JavaScript client library on another site, you should obtain another key for that site. More specifically, a key is associated with the URL that you enter on the signup page; the key applies to all URLs under the domain or directory that you specify._

_NOTE: It is also important to note that you **must** use the **full** version of the Google calendar. By default, the address to the calendar will point to the **basic** format. Change basic to full in the URL in order to have the plugin work correctly._

## Displaying The Calendar ##

Calendar data can be displayed in three ways:

### As a widget in the sidebar ###

The simplest way to incorporate the calendar is to use the WPNG Calendar widget. The widget is installed as a part of the plugin-in, so you already have it. Use this widget like any other widget, drag-n-drop it into the sidebar where you want the calendar to appear.

Once the widget is there, you can customize the Title shown in the sidebar and the number of events that are displayed. Access these values in the widget's options panel.

#### As a page ####

Calendar data can also be embedded within a Page. The page will initially list data starting with the current date. The amount of data shown in the page will depend on the value you enter in the custom fields' value box. At the bottom of the page, links
will be displayed to allow the user to navigate to the next interval of data. To embed a calendar into a page, follow these steps:

  1. Create a page, give it any title you desire
  1. Add the following as a custom field: **show-wpng-calendar**
  1. In the value field enter the **number of weeks** of data you wish to display at one time
  1. Uncheck "Allow Comments" in the Discussion settings for the page

#### Displaying an event ####

Whether clicked from the side bar or from a page, each event can be displayed within its own modal DIV. The event view will show all details that are available from the Google calendar for that particular calendar entry. As an option, you can choose to render the description field of an event using [wiki markup](WikiFormatting.md). The markup syntax is similar to most common wiki markup languages. For more information, see the [Wiki formatting](WikiFormatting.md) page.

## Formatting ##

We made every attempt to make the calendar integrate with themes as much as possible. If you do have a need to edit the style of event lists or the ThickBox dialog, you can use the following:

  * wpng-calendar/css/style.css
  * wpng-calendar/css/thickbox.css

You can update the size of the modal, but alter this line in the functions.js:

```
/* add the div to my modified ThickBox function */
tb_show_inner("",entryDiv.innerHTML,"height=500&width=500");
```

## Screenshots ##

**Calendar In A Page & As A Widget**

![http://lh3.google.com/l1jockeys/R9sZBkG5m4I/AAAAAAAAABc/UA0cVH2zp_Q/s400/wpng-cal1.png](http://lh3.google.com/l1jockeys/R9sZBkG5m4I/AAAAAAAAABc/UA0cVH2zp_Q/s400/wpng-cal1.png)


**Displaying An Event**

![http://lh3.google.com/l1jockeys/R9sgCkG5m7I/AAAAAAAAACE/mbvw7mA4JwI/s400/wpng-cal4.png](http://lh3.google.com/l1jockeys/R9sgCkG5m7I/AAAAAAAAACE/mbvw7mA4JwI/s400/wpng-cal4.png)


**Plugin Configuration**

![http://lh3.google.com/l1jockeys/R9sZBkG5m5I/AAAAAAAAABk/QRdkWVGGCTk/s400/wpng-cal2.png](http://lh3.google.com/l1jockeys/R9sZBkG5m5I/AAAAAAAAABk/QRdkWVGGCTk/s400/wpng-cal2.png)


**Widget Configuration**

![http://lh4.google.com/l1jockeys/R9sZB0G5m6I/AAAAAAAAABs/GTEiEXgEE-0/s400/wpng-cal3.png](http://lh4.google.com/l1jockeys/R9sZB0G5m6I/AAAAAAAAABs/GTEiEXgEE-0/s400/wpng-cal3.png)


## Special Thanks ##

This is our first plug-in and required a lot of Google time. A few articles and sites really helped to get this going. We would like to point out those brave individuals who blazed the Wordpress plug-in trail long before us:

#### Creating A Plug-In ####

Ronald Huereca - http://www.devlounge.net/extras/how-to-write-a-wordpress-plugin

#### Creating A Widget ####

Mason Wolf - http://hiremasonwolf.com/plugin-to-widget/36

#### Date Maniuplation Magic ####

The Coolite Crew - http://www.datejs.com

#### Wiki Rendering With JavaScript ####

Stefan Goessner - http://goessner.net/articles/wiky/

#### Thickbox ####

Cody Lindley - http://jquery.com/demo/thickbox/