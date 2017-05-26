# intoCareers Portal Reference #

*Last updated May 12,2017*

### Table of Contents ###
1. [Getting Started](#getting-started)  
  a. [Introduction](#introduction)  
  b. [Terms and Jargon](#terms-and-jargon)    
  c. [Logging In](#logging-in)    
  d. [Umbraco Backoffice Overview](#umbraco-backoffice-overview)         
  e. [User Types and Permissions](#user-types-and-permissions)
2. [Umbraco Components](#umbraco-components)   
  a.  [Media](#media)   
  b.  [Data Types](#data-types)    
  c.  [Document Types](#document-types)    
  d.  [Templates](#templates)   
  e.  [Macros](#macros)
3. [Creating an intoCareers Site](#creating-a-site)   
  a.  [Page Hierarchy](#page-hierarchy-and-navigation)  
  b.  [Root Node](#root-node)      
  c.  [Adding Settings](#adding-settings)   
  d.  [Culture and Hostnames](#culture-and-hostnames)
4. [Managing Pages](#managing-pages)   
  a.  [Add a Page](#add-a-page)   
  b.  [Remove a Page](#remove-a-page)   
  c.  [Move a Page](#move-a-page)   
  d.  [Copypaste a Page](#copypaste-a-page)    
5. [Grid Layouts and Classes](#grid-layouts-and-classes)   
  a.  [Grid Layout Overview](#grid-layout-overview)   
  b.  [Grid Layout Classes](#grid-layout-classes)   
    * [IC Portal Home 2 Classes](#ic-portal-home-2-classes)
6. [intoCareers Page Types](#intocareers-page-types)   
  a.  [Settings Page ("IC Portal Settings")](#settings-page)    
  b.  [Home Page ("IC Portal Home 2")](#home-page)              
  c. [Standard Page ("IC Portal Standard Page")](#standard-page)   
  d. [No View Folder ("IC Portal No View")](#no-view-folder)   
  e.  [External Link Page ("IC Portal External")](#external-link-page)  
  f.   [PDF Page ("IC Portal PDF")](#pdf-page)  
  g. [Q and A Page  ("IC Portal Q and A Page")](#q-and-a-page)  
  h.  [Contact Page  ("IC Portal Contact Page")](#contact-page)   
  i. [Thumbnail List Page ("IC Portal Thumbnail List Page")](#thumbnail-list-page)   
  j.  [Parchment Page ("IC Portal Static Parchment Page")](#parchment-page)   
  k.  [Fancy Page ("IC Portal Fancy Page")](#fancy-page)  
  l.  [Clever Page](#clever-page)
7. [intoCareers Macros](#intocareers-macros)   
  a.  [ContactFormFrame](#contactformframe)   
  b.  [FontAwesomeLargeIcon](#fontawesomelargeicon)
  c.  [LoginBox2](#loginbox2)   
  d.  [LoginBoxLinked1](#loginboxlinked1)   
  e.  [LoginBoxLinked2](#loginboxlinked2)   
  f.  [LoginTabs2LinkedTab](#logintabs2linkedtab)   
  g.  [LoginTabs2LinkedPlus](#logintabs2linkedplus)   
  h.  [LoginTabs2TabLink](#logintabs2tablink)     
  i.  [LoginTabs2TabLinkPlusClever](#logintabs2tablinkplusclever)   
  j.  [ParchmentForm](#parchmentform)   
  k.  [SidebarFoldedImageTop](#sidebarfoldedimagetop)   
  l.  [SmallCarousel](#smallcarousel)   
  m.  [SmallCarouselLinkable](#smallcarousellinkable)   
  n.  [SmallCarouselLinkable4Items](#smallcarousellinkable4items)     
8. [Advanced Customization Options](#advanced-customization-options)   
  a.  [Change Color Picker Colors](#change-color-picker-colors)  
  b.  [Add New Stylesheets](#add-new-stylesheets)   
  c.  [Change Stylesheet Picker Dropdown](#change-stylesheet-picker-dropdown)
9. [Examples](#examples)   
10. [URL Rewriting](#url-rewriting)
11. [Accessibility](#accessibility)
12. [Frequently Asked Questions](#frequently-asked-questions)   
13. [What Next](#what-next)   
14. [Additional Resources](#AdditionalResources)

### Getting Started ###
#### Introduction ####
The new intoCareers portal sites are built and managed within the [Umbraco][1] content management system, a content management system for [ASP.NET MVC][2].

This guide pulls together the scattered and often highly-technical, developer-oriented information about using Umbraco in addition to offering specific information on managing (and creating) intoCareers Umbraco portal sites.

> FYI: Throughout this guide, menus involved in creating and managing pages from within the Umbraco "backoffice" (the management user interface) will be referred to as ellipsis menus (as the menu is accessed by clicking on an ellipsis). The menu accessed by *left-clicking* on the ellipsis will be referred to as **ellipsis create menu**, while the menu accessed by *right-clicking* the ellipsis will be referred to as the **ellipsis options menu**. The menu appears when there are options available for a given item. The menu looks like this:

>![Ellipsis menu](/images/ellipsis-menu-1.png).

[Return to Table of Contents](#table-of-contents)

#### Terms and Jargon ####
**Backoffice**:  The Umbraco Backoffice is an interface for creating, updating, removing, and managing sites. It allows developers to customize the content-creation and management tools and allows content managers to…manage content.

**Document Type**: (Per [OurUmbraco.org][3]) “A Document Type is a data container in Umbraco where you can add data fields/attributes where the editor user can input data and Umbraco can use it to output it in the relevant part of a template.” In other words, a document type is an archetype of a kind of document that defines a set of properties or attributes that will be used by content managers for adding content to the document. For example, a document type for a home page might have properties like Page Title, Banner Image, and Background Color Picker.

**Dynamic**: In this context, dynamic is generally used to note that data is subject to change and is not hard-coded. Dynamic data and content can be added, changed, or removed without requiring the code that renders that content to be changed.

**Macro**: (Per [OurUmbraco.org][3]) “A macro is a reusable piece of functionality that you can re-use throughout your site. Macros can be configured with parameters and can be inserted into a Rich Text Editor. You can define what macros are available for your editors to insert into the rich text editor. When an editor inserts a macro into the rich text editor, it will prompt them to fill out any of the defined parameters for the macro.” Translation: A macro is a widget of sorts that you can plop into any parts of any pages that are configured to allow them. The same macro/widget may be reused across the site and many macros/widget are customizable (and will prompt the user to enter values for the custom bits).

**Node**:  A node is a point on a larger network of points. In this context, it is generally used to refer to a page or document in a site tree/hierarchy.

**Razor**: Razor is a server-side markup language and not a programming language. It allows ASP.NET MVC developers to use C# and/or Visual Basic code with HTML to create dynamic web pages.
Root Node: The root node is the page at the top of a site’s page hierarchy.

**Umbraco**: An open-source content management system for ASP.NET MVC.

[Return to Table of Contents](#table-of-contents)

#### Logging In ####
In order to access the intoCareers Umbraco "Backoffice" (the management interface), open a web browser and navigate to  <https://portal.intocareers.org/umbraco/#/login>. Once there, log in using the login credentials created for you by a site administrator (or by you, if you are that administrator):

![Log In To Umbraco](/images/log-in.png)

A successful login will immediately take you to the intoCareers Umbraco backoffice.

[Return to Table of Contents](#table-of-contents)

#### Umbraco Backoffice Overview ####
**Content Tab** – The Content tab is the first tab on the Backoffice navigation bar. This is where content managers can create, update, and remove sites and pages (and the content therein). It shows the sites created and the sites’ respective page hierarchies. The hierarchies can be collapsed and uncollapsed as desired.

![Content Tab](/images/backoffice-content-tab.png)

**Media Tab** – The Media tab is the second tab from the top on the Backoffice navigation menu. Media like images and PDFs can be added, removed, and organized here.

![Media Tab](/images/backoffice-media-tab.png)

**Settings Tab** – The Settings tab is the third tab from the top on the Backoffice navigation menu. This is where document types, templates, partial views, stylesheets, and scripts can be added, removed, changed, and managed by developers.  This tab is unlikely to be displayed for non-administrator or non-editor accounts.

![Settings Tab](/images/backoffice-settings-tab.png)

**Developer Tab** – The Developer tab is the fourth tab from the top in the Backoffice menu. This is where data types, macros, packages, and partial views (for macros that require them) can be created, updated, and removed. Non-developers will almost certainly not see this tab. Developers are advised to become familiar with data types and macros before using this tab, as data types and macros can sometimes become irreparably broken if the developer is not careful. (Grid data types are particularly easy to break.)

![Developer Tab](/images/backoffice-dev-tab.png)

**Users Tab** – The Users tab is the fifth tab in the Backoffice menu.  User types such as “Editor,” “Writer,” or “Admin” can be created, changed, and deleted here. Users can be added and user permissions can be assigned here. Non-administrator accounts will almost always be unable to see or work with this tab.

![Users Tab](/images/backoffice-user-tab.png)

**Members Tab** – The Members tab is the sixth tab in the Backoffice menu.  Site users who have access to the site can be managed here. These member users should not be confused with the internal users in the Users tab (who are a part of the management of the site).  The intoCareers portal does not make use of this Umbraco feature at this time and the tab will probably not be visible for any non-administrator user.

![Members Tab](/images/backoffice-member-tab.png)

Additional information about the Umbraco Backoffice can be found [here][4].

[Return to Table of Contents](#table-of-contents)

#### User Types and Permissions ####
Some of the tabs in the Umbraco backoffice may not be visible to all users. The permissions set by an administrator determine what a user can and cannot do and what the user can and cannot see in the backoffice. Don't be alarmed if something discussed in this documentation is invisible or disabled for you. Contact a site administrator if you think you need more generous permissions.

[Return to Table of Contents](#table-of-contents)

### Umbraco Components ###
#### Media ####
Working with Umbraco’s Media through the media tab is fairly straightforward.

To work with Media through the Media tab, first navigate to the Media tab. Inside the Media section is a collection of media files and folders used to organize those files.

One nice thing about the way Umbraco implements folders in its Media section is that those folders do not affect the path of the filename. In other words, you can move a file around from one folder to another, move it outside of folders altogether, place it in a subfolder of a folder, etc. and the file’s actual location in the file structure doesn’t change. The folders are there to help you, the content manager, find and access the files that you need. For this reason, you are free to organize your Media files however you like, without worrying about having to go back and re-add your media file to the page or pages on which it lives in order to correct the path. The actual path never changes. It only *looks* like it does.

If you want to add some more organization to your media files, hover over the item you want to contain your item, then create (or move) your item by accessing the ellipsis options menu (by right-clicking) or the ellipsis create menu (by left-clicking). If you want your folder to be at the top level of the hierarchy, the "folder" that will contain your folder will be the Media folder:

![Create Media Item at the Top Level](/images/create-media-1.png)

The “Create” menu accessed through the “MEDIA” create menu offers only one option: Folder.

![Top-Level Create Options](/images/create-media-2.png)

Lower-level “Create” menus offer three options: Folder, Image, or File.

![Lower-Level Create Options](/images/create-media-3.png)

To delete an image, file, or folder from Media, right-click to access the ellipsis options menu for that item (or folder) and select “Delete”.

To re-order your Media (which you may wish to do after creating a new folder), select “Sort” and then drag-and-drop your items until they are in the desired order.

To move an item or folder (which comes in handy for putting items in a folder or pulling them out of a folder) select “Move.” This will bring up a list of available locations for the item. Select the final destination and click “Submit” to move the item.

[Return to Table of Contents](#table-of-contents)

#### Data Types ####

(Per [OurUmbraco.org][5]) "A data type defines the type of input for a property." Though it references a property editor, data types and property editors are *not* the same thing. A data type is a specific configuration of a property editor.

For example, a property editor like the built-in Umbraco color picker can be used for several data types, one of which offers forty-nine shades of grey for the content managers/creators to choose from called “IC Portal Forty-Nine Shades of Grey Color Picker,” one that offers the seven basic colors of the rainbow called “IC Portal ROYGBIV Picker,” and one with nothing but pastels called “IC Portal Precious Moments Color Selector.”

The distinction between data types and property editors isn’t that important for most purposes, but if you plan on delving deep into data types and property editors for some reason, you can think of a property editor as a generic bicycle—the [Platonic Form][6] of bicycle-ness, if you will—and a data type as a specific type of bicycle, like a tiny pink Huffy with purple tassels on the handlebars or an enormous, beast-like, caked-in-mud, blue mountain bike with purple tassels on the handlebars.

If you need to create or modify existing data types, it is highly recommended that you [read the OurUmbraco.org documentation][5]. Data types can be fussy and some of them (like the Grid Layout editor) can break completely, causing serious issues for any site already using them.

[Return to Table of Contents](#table-of-contents)

#### Document Types ####

![Document Type Anatomy](/images/doctype-anatomy.png)

**(A)	Tab section** — This section is displayed as a tab when viewing a node created from this document type in the Backoffice Content tab. All of the attributes/properties displayed in this tabbed section will be displayed on this tab (a “Content” tab, in this case).

**(B)	Tab title** — This is what the tab will be called when a content manager or creator goes into the Backoffice Content tab. The tab title can be changed by clicking on the text of the current title and typing in a new one.

**\(C\)	Attribute/Property/Data Field** — The attribute/property/data field defines a certain type of data for a created page of this document type. It gives this type of data a name, an alias, and a means of inputting data via a data type (or property editor). It also allows the developer (or savvy content manager/creator) to delete the property or change its settings.

**(D)	Property/Attribute Alias** — The name used to represent the input data in the code. (This is code usually lives in a template.)

**(E)	Property/Attribute Name** — The name that is displayed for the content manager or creator’s benefit.

**(F)	Data Type/Property Editor** — Defines the means by which data can be input.

**(G)	Settings** — The gear icon represents settings for this property editor/data type. Left-click on the gear to pull up configuration settings.

**(H)	Delete** — Click this little trash can (or recycling bin, if you’re fancy) to delete this property.

**(I)	Add Property** — Left-click this space to summon a property creation window.

**(J)	Compositions** — Allows you to add (or inherit, really) properties from another document type (some Umbraco projects create document types specifically to be used and reused as compositions).

**(K)	Reorder** — Selecting this will allow you to rearrange properties within tab sections and even rearrange the order of the tabbed sections themselves.

**(L)	Document Type icon** — This icon is displayed next to nodes in the Umbraco Backoffice’s “Content” tab. Left-clicking on this icon will pull up a window to select a different icon and/or different icon color. The icons are useful for giving content creators and managers a better idea about the function of pages created from this document type.

**(M)	Document Type description** — Offers a brief summary of what this document type is and what it is meant to accomplish. Can be changed by clicking on the existing text and editing or replacing that text.

**(N)	Document Type name** — The name of the document type. Initial name determines the document type alias (which will be in the lower [camelCase][7] format). Can be changed by clicking on the existing name and entering a new one. Ideally the name should be brief, but descriptive enough to tell what the document type is for (more or less).

**(O)	Whoops** — This is still the Document Type name. I…totally meant to do that. Super on purpose is what that is. (Look at it this way, at least now you really know where the Document Type name is, right? You’re a name-changing pro! A total expert. All thanks to me. Well done, me!)

**\(P\)	Document Type Alias** — The name used to represent the document type in the code. (Code referencing the document type alias can usually be found in a template.)

**(Q)	Design view** — The view with items A through P can be viewed and manipulated in this view. The structure (within the Backoffice “Content” view) and content of the document type is defined here.

**\(R\)	List view** —This view is primarily used to organize subordinate content. More in-depth information about this view is available [here][8].

**(S)	Permissions view** —Permissions view allows developers (and savvy non-developers) to choose whether or not a page/node of this document type can exist at the root (i.e. at the very top level of the page/node hierarchy) and which sorts of document types—if any—are allowed to be used to exist as child nodes of this document type.

**(T)	Templates view** — This view allows the user to select which templates—if any—are allowed to be associated with this document type. In cases like the IC Portal Settings document type, no templates are chosen because that node is not meant to be rendered. For document types used to create pages that are meant to be rendered, this area makes it possible for content creators and managers to have more choice when it comes to setting how the page will be rendered. If multiple templates are set in this view, savvy users can navigate to the “Properties” tab of a page created from this document type within the Backoffice “Content” tab and select a desired template from a list of options.

To create a new tab in a document type, left-click the “Add another tab” area underneath the last tab. (If there are no tabs yet, this will should up at the top of the page.)

![Create new tab](/images/add-tab.png)

Enter a name for your tab.

![Create new tab](/images/new-tab-1.png)

Next, you’ll want to add one or more properties. To create a new property, click the “Add new property” area of the tab. This will pull up a pane that will allow you to define some basic things about your property like its name and a brief description to help others figure out what it’s for and how to use it.

![Create new tab](/images/new-tab-2.png)

You can make the property mandatory, if you want to require that the content creator or manager add a value for this property. You can also add validation.

If you want to make sure the content creator/manager enters an email address as the value for this property, select that option from the Validation dropdown.

If you want to make sure that they are only allowed to enter a number in the field, select that. If you are familiar with regular expressions, you can opt to create your own type of validation, if you so desire.

Finally, select a property editor for this property. Left-clicking “Add editor” will bring you to a list of available property editors. Keep in mind that this is not an exhaustive list of available editors. This can make finding the editor you really want a little annoying. You can search for the property editor you want, but that’s not much help if you’re not familiar with all of the available types.

If you have access, you can expand the Data Types folder in the Developer tab in order to see an exhaustive list of all available types. You will still have to search for it when you go back to assign an editor to the property, but at least you’ll be able to find it.

![Add property editor](/images/new-tab-3.png)

Once you’ve selected your property editor, click “Submit.” Now you have a new property inside your new tab! You can add as many properties to existing tabs as you like and as many additional tabs as you want (though be reasonable, for the sake of those who will have to use them).

If you want to delete tabs or properties, click on the little trash can icon in the upper right of the property or tab in question and then select the green check to confirm.

Umbraco’s official documentation concerning document types can be found [here][9]
A tutorial can be found [here][10].

[Return to Table of Contents](#table-of-contents)

#### Templates ####
Templates in Umbraco are (more or less) ASP.NET [Razor][21] views that are used to define a page's structure. They are also where data put into the template's document type can be pulled into the page.

Document types without corresponding templates (whether full templates or the "partial view" templates that define the structure of a *part* of a page) are not intended to be displayed. Trying to preview a page (or "node", really) without a template will result in an error. This does not break the site, but as with many Umbraco errors, it can be alarming to encounter. (So much red!) Just remember that the error is a minor one that stems from trying to view something that is not intended to be viewed and that the error should not affect the site in any way (apart from the initial error page).

[Return to Table of Contents](#table-of-contents)

#### Macros ####
Macros are basically reusable pieces of functionality. The login box carousels, for example, are macros that can be plopped into any macro-supporting pages in the intoCareers portals. Of course, not all macros are appropriate for every place or page into which you can insert one. The main LoginBox macro would look strange plopped into a Contact Form page. The styling associated with each macro is tailored to fit certain macro-allowing spaces on a page, so a macro may look weird if it is put somewhere it was not designed to go.

[Return to Table of Contents](#table-of-contents)

### Creating A Site ###
#### Page Hierarchy and Navigation ####
Before diving into creating a new site, it's important to understand how Umbraco structures sites and how that structure informs the generation of the navigation menu.

Umbraco sites are structured a tree/hierarchy like so:

![Page Hierarchy](/images/page-hierarchy-1.png)

Because of the way that navigation menus are typically created in Umbraco, it is important to structure your hierarchy according to where you wish page items to appear on the navigation bar. For example, the hierarchy shown in the above image would result in a navbar that looks like this:

![Navigation Menu Generated By Page Hierarchy Structure](/images/nav-page-hierarchy.png)

You may have noticed that the intoCareers Global Settings item does not appear on the navbar. There is an option to exclude pages from showing up on the menu. All page types have a “Hide from navigation?” checkbox. Not only is that useful for keeping users from seeing the site settings node, but it can also be used for pages that are not finished or are otherwise not quite ready for primetime.

It is also important to note that the intoCareers sites' navigation menus do not currently support a hierarchy any deeper than shown in the first image in this section. The "About Us" folder, for example, cannot contain another folder with nested content. Doing so would result in a really wonky navigation menu.

[Return to Table of Contents](#table-of-contents)

#### Root Node ####

In order to create a new site, first create a new root node. Navigate to the **Content tab** in the Umbraco backoffice and hover over the "CONTENT" heading. Left-click the ellipsis that appears on hover and select the type of item you want your root node to be.

The "IC Portal Home 2" document type (or any other Home document type) is an example of a type of root node that can be created.

The "IC Portal Settings" document type option should not be chosen for a root node. This option (to create this type at the root level) only exists in case a placeholder settings node is needed for the initial root node configuration.

After selecting the document type you'd like to use for your root node, you will need to give it a name. The name should be something that represents the client for which the site is being created (e.g. "North Dakota").

Once the root node has been named, a page will open in the right window of the backoffice:

![New Site Page](/images/new-site-1.png)

The first tab you will (likely) see is the **SEO** tab. Adding meta tags for search engine optimization can be done here. This tab is purely optional, so it's fine to ignore it.

The second tab is labeled **Content** and where the main content of the page goes. This tab doesn't need to be filled with content right away. The page can be created without it.

The third tab is the **Additional Settings** tab. This tab has two mandatory fields and the page will not be able to be created without assigning values to the "Page Title" and "Settings Node" properties. To clarify, the "Page Title" here is the name of this current page (e.g. 'Home') and not the name of the site as a whole. The name of site will be set when you create your Settings node. There is a placeholder settings node that can be selected. A real settings tab will need to be created next and you can go back and change the node from the placeholder to the new settings node.

![Additional Settings Tab](/images/new-site-2.png)

The last tab is always the **Properties** tab. You can set publication dates and times and page templates here. This tab should only be used by developers who have familiarized themselves with its purpose.

[Return to Table of Contents](#table-of-contents)

#### Adding Settings ####
To create a settings node, hover over the root node and left-click on the ellipsis to access the ellipsis create menu. From there, select the "IC Portal Settings" document type.

After entering a name for your node (e.g. "Example Global Settings"), fill in as many properties as you can. Property fields that must have values for the site to function include "Main Stylesheet" (select a theme stylesheet from the dropdown menu), "Microsoft Browser Styles" (select an appropriate stylesheet from the dropdown menu), site title, background color (light grey is the preferred selection), and the "Portal Brand" image (this is the image that appears at the top of the page when using the Legacy theme). Colors for the navbar, navbar text (white usually works best), login box, login box text, footer, and footer text all need to be selected to avoid crashing the site. These can always be changed later, so assigning them temporary values is not a problem.

Once that's done and you've save the settings node, go back to the root node and change the assigned settings node.

> NOTE: Don't try to "Preview" a settings node. It is exclusively used to set site-wide and login-related properties and there is no template to render it.

[Return to Table of Contents](#table-of-contents)

#### Culture and Hostnames ####
In a multi-site Umbraco project like this, Umbraco needs a way to tell which page belongs to which site. This is especially important when the sites have page with identical names.

For example, if the "New Jersey" site has a page called "About Us" and the "Oklahoma" site also has a page called "About Us", Umbraco will only be able to display *one* of them. While navigating to "About Us" from within the "New Jersey" site will take the user to the correct "About Us" page, navigating to "About Us" from within the "Oklahoma" site will take the user to *New Jersey's* "About Us" page and not Oklahoma's.

Umbraco will see identical page names as belonging to different sites *only if* those pages are tied to different domains or hostnames. This setting--called "Cultures and Hostnames"--can be accessed by hovering over the root node, and right-clicking on the ellipsis to open the options menu panel.

![Culture and Hostnames Option](/images/culture-hostnames-1.png)

In the configuration window that opens upon selecting "Cultures and Hostnames," select “Add New Domain” to assign a site a unique domain or hostname. The pattern used to differentiate the intoCareers sites is "portal.intocareers.org/[2-letter client code]":

![Add New Hostname](/images/culture-hostnames-2.png)

[Return to Table of Contents](#table-of-contents)

### Managing Pages ###
#### Add a Page ####
In order to add a page to an intoCareers site, first choose a parent node for your page. To add a "Products" page that needs to be displayed on the main navigation bar of the "New Jersey" site, for example, hover over the "New Jersey" site until the ellipsis appears and either *left-click* the ellipsis to immediately access the create menu or *right-click* the ellipsis to open the options menu and select the "Create" option there (if you want to take the scenic route).

![Choose Parent Node for the New Page](/images/add-page-1.png)

This will bring up a list of possible document types allowed at this level in the hierarchy. To stick with the "Products" page example, it might be good to select a document type like the ["IC Portal Thumbnail List Page"](#thumbnail-list-page) type.

![Select New Page Document Type](/images/add-page-2.png)

Once a document type has been selected, the main pane of the Umbraco backoffice will display fields that can be filled in to add content to the new "Products" page.

![Select New Page Document Type](/images/add-page-3.png)

Add content by filling in the fields in the various tabs presented, then save and send for publishing or save and publish, if you have that ability. Any mandatory fields left blank will prevent the page from being saved, so be sure to assign34 values to all of the mandatory fields.

[Return to Table of Contents](#table-of-contents)

#### Remove a Page ####
In order to remove a page/node, find the page you wish to delete, hover over it and then right-click on the ellipsis that appears to its right in order to access the ellipsis option menu. Following that, select the "Delete" option and then confirm the deletion.

![Delete Page Option](/images/delete-page-1.png)

> CAREFUL: Be aware that if the node/page you're deleting has child nodes/pages (subordinate pages), those will be deleted as well.

Don't worry if you make a mistake or decide later on that you want that page/node after all. If the **Recycle Bin** hasn't been emptied since pages that need to be restored were deleted, any of those pages (including child nodes!) can be recovered from the Recycle Bin.

![Delete Page Option](/images/delete-page-2.png)

Simply open the ellipsis options menu by *right-clicking* on the ellipsis that appears upon hovering over the page to be restored, select the "Restore" option near the top of the menu, and confirm the restoration.

![Restore Deleted Page](/images/delete-page-3.png)

[Return to Table of Contents](#table-of-contents)

#### Move a Page ####
Pages can be moved both within a site and between sites. They can also be sorted in any order desired.

To move a page, *right-click* on the ellipsis that appears upon hovering over that page to access the ellipsis options menu. The options menu pane that appears has a "Move" option.

![Move Page Option](/images/move-page-1.png)

Selecting “Move” will pull up a collapsed hierarchical list of all sites and nodes to which you have access. After selecting the "Move" option, select the desired parent node for the page.

For example, in order to move Missouri's "About Us" page from the second-level to the third-level under the "Resources" folder, select the "Resources" item from the list and then click the green "Move" button.

![Move Location Selection](/images/move-page-2.png)

To move a page like "User Support" from within the Resources folder up to a level, the "Missouri" root node would be the parent node selected.

![Move Location Selection](/images/move-page-3.png)

But what if you only want to change the order of the items in the hierarchy. To sort items, *right-click* the ellipsis that appears upon hovering over the parent node of the items you wish to sort in order to access the options menu. From there, select the "Sort" option and drag the items into the desired order. Make sure to save the new order before closing the sorting pane.

![Sort Pages](/images/sort-page-1.png)

[Return to Table of Contents](#table-of-contents)

#### Copypaste a Page ####
One great feature of Umbraco is the ability to copy and paste pages. This is especially useful in cases where there are pages within different intoCareers projects that have similar or identical content.

Q and A pages, for example, often have a lot of content that is  time-consuming to create, but is almost exactly the same across all of the intoCareers sites. Copypasting content like this can save a lot of time.

The only potential issue with copypasting is that it's very easy to forget to swap out any references, links, or images that are specific to the client site from which a page has been copied. Forgetting to change those is...not a good look.

In order to copy and paste a page, access the ellipsis option menu of the page you wish to copy and select the “Copy” option:

![Copy a Page](/images/copypaste-1.png)

This will pull up a collapsed hierarchical list of all sites and pages that can be selected as parent nodes for the copied content.

To copy the intoCareers Products page--another page that is very similar across the sites--from "intoCareers" so that it can be pasted into "Ohio," for example, select the desired node/page that will serve as the parent node for the page.

One thing to watch out for are the "Relate to original" and "Include descendants" checkboxes. They are both checked automatically.

![Paste a Page](/images/copypaste-2.png)

"Relate to original" means that changes you make to the copy may affect the original and vice versa.

"Include descendants" means that any child nodes that the copied node may have will be copied as well (and structured in the same way). This is useful for copying entire folders of content like the "Technical Support" folder, which is very similar across sites. (Though, again, be sure to change anything in the copy that is specific to the site from which it originated.)

Click the green "Copy" button and the page will be copied.

The copy will now appear under the selected destination parent node, but it will be greyed-out. The page needs to be saved before it can really be a part of the destination site. It is possible to customize the copied page before saving it for the first time, so (one last time...) be sure make any changes to the page that are specific to the site from which is was copied.

[Return to Table of Contents](#table-of-contents)

### Grid Layouts and Classes ###
#### Grid Layout Overview ####
Before moving on to the individual intoCareers portal document types, it’s good to know a little bit about a property that you will run into on a few of them: grid layouts.

A grid layout is an Umbraco data type that can make content management a lot more flexible for content managers. Often, a grid layout property will offer a range of different layouts to choose from like an equal column two-column layout, a full-width single-column layout, a lopsided two-column layout, etc.

Within those layouts, there are grid rows that provide further options for customizing the type of content that appears on a page (i.e. a headline or an image) and in what order than content appears.

Though they can be a little difficult to style at times, grid layouts (hopefully) offer an easy plug-n-play experience for content managers.

The grid layout on a new page using the "IC Portal Standard Page" document type, for example, offers a clear, simple set of row options for content managers to start adding content to the page:

![IC Portal Standard Page Grid Layout](/images/grid-layout-1.png)

After adding the initial row, rows are added by clicking on a "+" button below a row. Clicking an "Add content" area within a row will add more content, but that content will still technically be within the same row.

![Grid Layout Add Row](/images/grid-layout-2.png)

Using the IC Portal Standard Page grid layout, a content manager could add a Heading row, followed by a Main Content row, another Heading after that, and a Main Content Row to cap off the page. Content managers can continue to add rows upon rows upon rows if desired. A content manager could also add one heading row with two, three, four, one thousand headlines. (It's unclear *why* someone would do that, but it is *possible*.)

![Grid Layout Add Row](/images/grid-layout-3.png)

To style the row (i.e. specify how it is displayed), there are two places where [classes][18] may be able to be set. If the row is set to allow it, there will be a gear icon in the upper-right corner of the row and a gear in the upper-right corner of the content *inside* of the row. Clicking on one of the gears will pull up a settings pane that allows a class to be set for that block of content. (It doesn't usually matter which settings gear you select, but if assigning a class to one results in funky styling, it's worth trying to unset it and set the other.)

At the moment, the grid layout section on the lower part of the "IC Portal Home 2" document type is the only place where a class may be set. Setting a class for each of the two columns on this page type can be done by selecting one of the radio button options.

![Grid Layout Add Row](/images/grid-layout-4.png)

More information about grid layouts can be found [here][19].

[Return to Table of Contents](#table-of-contents)

#### Grid Layout Classes ####
Ideally, content managers would not need to do any class-setting, but the automatic generation of the grid layout columns by Umbraco's grid layout editor can make it difficult to attach default classes to those columns.

Until a better solution comes along (and it likely will, given that grid layouts are a relative new feature of the Umbraco CMS), some grid layouts require that content managers set classes so that the columns display as desired.

[Return to Table of Contents](#table-of-contents)

##### IC Portal Home 2 Classes #####
The "IC Portal Home 2" document type has two classes, one for each of the lower section grid layout columns:

* home-left-col --> targets the left column!
* home-right-col --> targets the right column!

[Return to Table of Contents](#table-of-contents)

### intoCareers Page Types ###
#### Settings Page ####
The settings page is where site-wide settings like navigation menu color and footer text can be set.

The naming convention for Settings nodes is
```
[ClientName] Global Settings
```
Examples: "intoCareers Global Settings," "Arizona Global Settings"

See: [Adding Settings](#adding-settings)

##### Settings Page Properties #####
###### Portal-Wide Content Tab ######
**Site Title**: This is the title for the entire site.

**Main Stylesheet**: This is the main stylesheet for the page. It specifies how the content will be displayed. Select the desired theme from the dropdown menu.

**Microsoft Browser (IE/Edge) Stylesheet**: Microsoft has historically been resistant to adopting standards and though this is changing, many people still use older Internet Explorer browsers. It is sometimes necessary to create styles specific to IE to accomodate its special snowflake-ness. Select the file from the dropdown "ie-override-styles.css" or the stylesheet that matches the theme selected.

**Secondary Stylesheet**: (Optional) An additional stylesheet can be added to the site here, if necessary. The file loads *after* the other stylesheets, so it can potentially override styles defined in stylesheets that are loaded before it. Enter a filename (e.g. happy-styles.css) in the blank field, if using this feature. The stylesheet file referenced should live in the Umbraco "Stylesheets" folder that is accessible from the "Settings" tab. Using a secondary stylesheet is discouraged.

**Background Color**: This is the main background color for the site. Light grey is the preferred color for sites using the legacy theme.

**Background Image**: (Optional) A seamless tileable texture can be set as the page background.

**Portal Brand**: This is the intoCareers brand (logo) image that appears at the top of intoCareers sites.

**Portal Small Brand**: This brand will be swapped out for the main brand on phones that are in portrait orientation.

**Favicon**: Upload a 16 x 16 or 32 x 32 .ico (preferrably "favicon.ico") image that can be displayed on the user's browser location bar or in user's bookmarks when users favorite the site.

**Hide in navigation?**: This should always be checked on all settings nodes that make user of the "IC Portal Settings" document type. No template exists to render this content on any sort of "Settings" page, so attempting to preview or otherwise view a settings page will crash fail.

###### Navigation Tab ######
**Navbar Color Picker**: This sets the background color of the main navigation bar. Select a color from the available prevalues.

**Navbar Text Color**: This property defines the text color of the items on the main navigation bar. Select an appropriate color. It is highly recommended to use white as the text color.

###### Login Section Tab ######
**Login Tab Color Picker**: This sets the background color for the login box. Select a color from the available prevalues.

**Login Text Color**: This property defines the color of the text on the login box. White is recommended.

###### Footer Tab ######
**Simple Footer**: This is the text that will appear in the footer at the bottom of every page. It should be one line of text. The usual text is: ©1971-2016 University of Oregon. All rights reserved. Created by intoCAREERS, a unit of the University of Oregon.

**Footer Background Color**: This sets the background color for the footer. Select a color from the available prevalues.

**Footer Text Color**: This property defines the color of the text in the footer. White is recommended.

[Return to Table of Contents](#table-of-contents)

#### Home Page ####
"IC Portal Home 2" is a document type for the root node of the intoCareers site. It not only acts as the root of the entire site, but also specifies the content on the landing page that visitors will see when they first navigate to the site.

##### Home Page Properties #####
###### Content Tab ######
**Banner Image**: Select the banner image that will appear on the homepage. It should be 940 x 251px, if using the legacy theme.

**Equal Columns (Grid Layout)**: The "Equal Columns" property here is actually a grid layout property. It is more restrictive than most grid layouts and only allows for one row and two columns. The left column only accepts Image, Macro, and Embed (like YouTube videos or Twitter feeds) content types, while the right column only accepts Macros. Each column needs a class to be set in order to display properly. The left column uses the home-left-col class and the right column uses the home-right-col class.

![IC Portal Home 2 Document Type Content Tab](/images/home-page-1.png)

###### Additional Settings ######
**Page Title**: This is the title that will show up for the page (only this page!) on the browser's tool bar. It is recommended to set it to something like "Home" for this page.

**Settings Node**: This is where the proper Settings node is attached to the site as a whole.

![IC Portal Home 2 Document Type Additional Settings Tab](/images/home-page-2.png)

[Return to Table of Contents](#table-of-contents)

#### Standard Page ####
The "IC Portal Standard Page" is the document type for basic portal pages like "About Us."

##### Standard Page Properties #####
###### Content Tab ######
**Page Title**: This is the title that will show up for this page on the browser's toolbar.

**Hide in navigation?**: Check to keep this page from appearing as an item on the navigation menu.

**Grid Layout**: Add text headings, image headings, and main content.
See: [Grid Layouts](#grid-layouts-and-classes)

![Standard Page Content Tab](/images/standard-page-1.png)

[Return to Table of Contents](#table-of-contents)

#### No View Folder ####
The "IC Portal No View" document type is exclusively for grouping items that will be displayed on the navigation menu. The "No View" type is, as the name suggests, without a "view" attached to it. In other words, it cannot be displayed (and as such will result in an error for anyone who tries to preview it).

[Return to Table of Contents](#table-of-contents)

#### External Link Page ####
Given that Umbraco dynamically generates the navigation menu for intoCareers sites by using the site hierarchy, what do you do if you want to add a link to an outside site (or a [PDF](#pdf-page)) to the navbar?

The "IC Portal External" document type get around this by more or less tricks Umbraco into thinking that pages created from this document type are nodes and not links to outside sites or content. When the navigation menu generation code runs into an External Link node, instead of creating a navigation link to the node itself, it extracts the value of an External Link page's External Link *property* and uses *that* as the value of the navigation link.

The Razor markup that accomplishes this in the Navbar partial view:
```html
else if (childPage.documentTypeAlias == "iCPortalExternal")
{
	foreach (var item in childPage.externalLink )
	{
		var linkUrl = item.link;
		var linkTarget = (bool)item.newWindow ? "_blank" : null;
		<li class="open-item @(childPage.IsAncestorOrSelf(CurrentPage) ? "selected" : null)">
			<a href="@linkUrl" target="@linkTarget" style="@navTextStyle">@childPage.Name</a>
		</li>
	}
}
```

(There is another similar snippet for creating the link in submenu pages.)

##### External Link Properties #####
NOTE: The name of the item that will appear on the navigation menu is the value of the "IC Portal External" node's name and not the value of the link's caption.

###### External Content Tab ######
**External Link**: Enter a Url for an outside site and a caption for it. (You may set an internal site, if desired, but there is no good reason to do this.) The caption does not currently have a function, but in the future, it will be used as the value of the "alt" attribute for the `<img>` tag that is generated by this property. You may also opt to make sure that this link opens in a new window instead of navigating away from the portal site altogether. (It is recommended that this be checked.)

![External Link Page](/images/external-link-1.png)

[Return to Table of Contents](#table-of-contents)

#### PDF Page ####
The "IC Portal PDF" document type is very similar to the "IC Portal External" document type and exists for the same reason (to get around how Umbraco dynamically generates the navigation menu).

Though the document type is meant to allow PDFs to be linked to from the navigation menu, it can link to any media that Umbraco allows to be stored in its Media folder.

The main Navbar partial view code for adding the PDF link to the navigation bar is as follows:

```html
if (childPage.documentTypeAlias == "iCPortalPDF")
{
	IPublishedContent childNode = Umbraco.TypedContent(childPage.Id);
	var pdfIdString = childNode.GetProperty("pdfPicker").Value.ToString();
	var pdfItem = Umbraco.Media(pdfIdString);
	var pdfPath = @*"." + *@ pdfItem.umbracoFile;
	<li class="open-item @(childPage.IsAncestorOrSelf(CurrentPage) ? "selected" : null)">
		<a href="@pdfPath" target="_blank">@childPage.Name</a>
	</li>
}
```

(There is another similar snippet for creating the link in submenu pages.)

##### PDF Page Properties #####
###### Linked Content Tab ######
**Hide in navigation?**: Select whether or not this item should be displayed on the navigation bar.

**PDF Picker**: Choose the PDF (or other media item) that the navigation menu should use as this item's link Url. This property opens up a pane for finding the PDF in question. PDFs are stored in the Media "Resources" folder.

![PDF Page](/images/pdf-page-1.png)

[Return to Table of Contents](#table-of-contents)

#### Q and A Page ####
The "IC Portal Q and A Page" document type is a page meant to contain answer-and-response content like FAQs, but could be adapted for other purposes as well, like grouping links or resources like so:

![Grouping with the Q and A document type](/images/grouping-with-q-and-a.png)

##### Q and A Page Properties #####
###### Basic Content Tab ######
**Page Title**: This is the title that will show up for this page on the browser's toolbar.

**Hide in navigation?**: Select whether or not this item should be displayed on the navigation bar.

**Image Heading**: This is an optional property that allows an image to be set. The image is meant to work in place of or in addition to a text heading. However, it is in the process of being phased out (or altered), so making use of this property is discouraged at this time..

**Text Heading**: This is the heading for the main content of the page.

**Intro Text**: This optional text will appear just above the question-and-answer list. It is intended to allow content managers to add some context to the list that follows.

###### Q and A Tab ######
**Q and A Sets**: Unlike many of the other Umbraco properties, this property is very flexible and allows the content manager to add as many (or as few) questions and answers and as many *sections* of questions and answers as needed. It is a specific configuration of the [Archetype][20] property editor, which is a third-party property editor and *not* a part of the original, vanilla Umbraco CMS installation. This particular configuration--the Q and A Sets configuration--allows a user to set a(n optional) heading/title for a collection of topic-and-response items, add as many questions and answers as needed, *and* add as many *sets* of topic-and-response items as needed.

In the event that an issue with this Archetype property editor configuration arises, visit the [official Archetype site][20] and see if the problem is a known issue with the property editor and if someone has found a work-around or bugfix.

![Q and A Tab](/images/q-and-a-1.png)

[Return to Table of Contents](#table-of-contents)

#### Contact Page ####
The "IC Portal Contact Page" is a document type intended to contain a contact form, as well as any other contact-related information like addresses and phone numbers. (Non-contact form contact information can still be placed in other types of pages provided that those pages support entering content via a Rich Text Editor.)

##### Contact Page Properties #####
![Contact Page Document Type Properties](/images/contact-page-1.png)

###### Content Tab ######
**Page Title**: This is the title that will show up for this page on the browser's toolbar.

**Hide in navigation?**: Check this to prevent this page from showing up as a navigation item in the main navigation menu.

**Contact Grid Layout**: This grid layout property is fairly  minimalist. When a new contact page is created, the grid layout editor will offer a selection of four row types allowed in this grid layout. It is recommended that the first row added be a "Heading" row and that the "Image Heading" property be avoided unless absolutely necessary. After adding a Heading and maybe a Main Content row following that, create a "Contact Form Section" row. This row requires that a [macro](#macros) be set. The recommended macro for the Contact Form Section row is the "ContactFormFrame" macro.

![Contact Page Grid Layout Property](/images/contact-page-2.png)

[Return to Table of Contents](#table-of-contents)

#### Thumbnail List Page ####
The "IC Portal Thumbnail List Page" document type is intended to be used to present lists that have an image that should be displayed next to each list item. It works well for Products pages, though it can certainly accomodate many other situations. An example of an "off-label" use for this document type would be an "Who We Are"-esque employee bio page, with each employee list item containing a brief bio accompanied by a square 100x100 photo, avatar, or placeholder image.

##### Thumbnail List Page Properties #####
###### Content Tab ######
**Page Title**: This is the title that will show up for this page on the browser's toolbar.

**Hide in navigation?**: Check this to prevent this page from showing up as a navigation item in the main navigation menu.

**Heading**: This is the heading for the main content of the page.

**Additional Text**: This is optional text that can be used to provide context or some sort of introduction for the following list.

![Thumbnail List Page Content Tab](/images/thumbnail-list-1.png)

###### List Items Tab ######
**Thumbnail List**: This property is created from the generic [Archetype][20] property editor and allows a content manager to add as many (or as few) thumbnail list items as needed. Navigating to the List Items tab in a fresh "IC Portal Thumbnail List Page"-type page will look like so:

![List Items Tab Thumbnail List Archetype Property](/images/thumbnail-list-2.png)

The **Heading** field will be displayed as the heading for *this item*. The **Item Text** field is typically something like a product description. Below that Item Text rich text editor is an image picker. This may be left blank, but list items with an image look much better. (After all, this *is* a *Thumbnail* list page.) This must be a 100x100 pixel image. Traverse the media collection to find an appropriate image (or upload one in the proper place). Most images for property can be found in the "Brands" subfolder of the Media collection. These images are generally grouped by client, though a few general brands that can apply to multiple clients can be found in the "Brands" folder itself or in the "IC" subfolder (for the vanilla intoCareers portal site). To add additional list items, click the "+" icon to the right of the list item. Select the "x" to delete an item.

![Thumbnail List Items](/images/thumbnail-list-3.png)

[Return to Table of Contents](#table-of-contents)

#### Parchment Page ####
The "IC Portal Static Parchment Page" is a document type specifically for containing information and forms concerning the Parchment service. It is a totally rigid and inflexible page type that is intended to render in one very specific way, for one specific theme: the legacy theme. Other themes may make use of any Standard Page document type configuration that allows adding one or more headings, one or more sections of rich text content, and one or more form macros.

##### Parchment Page Properties #####
###### Content Tab ######
**Hide in navigation?**: Check this to prevent this page from showing up as a navigation item in the main navigation menu.

**Page Title**: This is the title that will show up for this page on the browser's toolbar.

**Main Heading**: This is the main heading for the page. Suggested text: PARCHMENT PARNERSHIP.

**Sub Heading**: This is the secondary heading for the page, which is displayed beneath the main heading. Suggested text: Parchment is available through **[Client]**

**Main Text Content**: This is the first major chunk of text that will be displayed on the page.    
Suggested text:
"**[Client]** and Parchment have partnered to make credential ordering easy for your school and your learners. Parchment is the most advanced academic credential management system available, allowing learners, academic institutions, and employers to request, verify, and share credentials in simple and secure ways. Parchment's platform has helped millions of people exchange more than 20 million transcripts and other credentials globally.

Implementing the Order Link, means your students can order transcripts anytime, anywhere, and just-in-time using the products they're already using every day. After submitting the form above, your Parchment representative will contact you to tell you more about implementing Parchment with **[Client Acronym]**."

![Parchment Page Content Tab Part 1](/images/parchment-page-1.png)

**Folder Ribbon Aside**: This is a property that will prompt the content manager to select a macro. Choose the SidebarFoldedImageTop macro and fill in the macro's empty fields. The first field is "Top Image", which needs an image that can be found in the "Brands" subfolder of the overall Media folder. The correct parchment image to choose here is the "banner_logo.png" image. After setting that, add the text that will appear on the folded ribbon aside to the "Folded Sidebar Text" field. Suggested text: Enable transcript ordering with **[Client Career Information System]** (**[Client System Acronym]**).

![Parchment Page Content Tab Part 2](/images/parchment-page-2.png)

![Parchment Page Content Tab Part 3](/images/parchment-page-3.png)

The Folded Ribbon Aside looks like this:

![Parchment Page Content Tab Part 5](/images/parchment-page-5.png)

**Tiny Heading**: This is the heading for the second major text section. It used to be tiny. Now it is the same size as the other headings. See what happens when you eat your vegetables?

**Supporting Text Content**: This is the second major chunk of text that will appear on the page.   
Suggested text: "As a member of Parchment's Affiliate Partner Program, **[Client Acronym]** can turn on transcript ordering as a feature in its student workflow. Ordering a transcript from the **[Client]** site is as easy as clicking the Order Link. The first step to adding this feature is setting up a license for Parchment Send, which includes a no-fee license option."

**Supporting Image**: This image displays to the right of the supporting text. Suggested image: Media --> Images --> Transcript.jpg

**Parchment Form**: Select the ParchmentForm from the dropdown menu.

![Parchment Page Content Tab Part 3](/images/parchment-page-4.png)

[Return to Table of Contents](#table-of-contents)

#### Fancy Page ####
The "IC Portal Fancy Page" document type is one of the most flexible available, which also makes it the most likely to go horribly horribly wrong. (No pressure!)

![Fancy Page "Fancy Content" Tab](/images/fancy-page-1.png)

##### Fancy Page Properties #####
**Page Title**: The title of this page.   
**Main Content**: This property makes use of a grid layout editor. This grid editor allows for a wide variety of different row types. Because there are many rows, it might be useful to describe what they are and how to use them:
* **Two Column Image-Left Text-Right**  
  This row type is (hopefully!) more or less self-explanatory. It is intended to accomodate an image in the left column and text content in the right column. The left-hand image content takes up a third of the row, while the text can do its text-y business with the other two thirds of the row.
* **Heading + 2-Col: Img-Left, Text-Right**  
  This row type is very similar to the above type, except that it allows a headline row directly above the image and text content. So...why have two different row types? Primarily for grouping and styling reasons. Applying a "basic-card" class (see: [fancy page classes](#fancy-page-classes)) to this entire row will make sure that the heading is on the card with the rest of the row's content. The heading-less version of this row does not offer this capability and so that content will be displayed separately from any heading.
* **Heading + 2-Col: Text-Left, Img-Right**  
  This row type is like a flipped version of the above type. It, too, has a heading-less variety (again, for grouping and styling reasons). A full-width heading sites atop an asymmetrical pair of columns. The left column, which takes up 2/3rds of the row, holds text content, while the right column (taking up the remaining third of the row) holds an image.
* **Heading + 3-Col Text or Image**  
  This row type allows a full-width heading over three equal-width columns, all three of which can accomodate text or an image. The flexibility of this type makes it pretty easy to make something ugly or weird-looking. So, like, don't...do...that? (You can use it, of course, just be careful.)
* **Full-Width Heading, Text, or Img**  
  This row allows for a full-width heading, full-width text content section, or a full-width image.
* **Triple Img Top, Triple Text Beneath**  
  This row type supports a top row of three images (each taking up a third of the row), with a row below that includes accompanying text underneath each of those three images.
* **3-Col Icon Macro Top, 3-Col Text Beneath**  
  This row type is very similar to the one above, except that instead of images, the top row (divided into thirds) supports a macro (called FontAwesomeLargeIcon) that displays a large [Font Awesome][35] icon.
* **Two-Column Text-Left, Image-Right**  
  This row type consists of a column for text content on the left (that takes up 2/3rds of the row) and a column for image content on the right (the remaining third of the row).
* **Heading + 2-Col Img or Text**  
  This row type includes a full-width heading row above an equal-width 2-column row that can accomodate images or text content.
* **Heading + Full-Width Txt or Img**  
  This row type has a full-width heading row on top of a full-width text or image row. This row type is meant for cases when the heading and full-width content beneath it need to be grouped together (usually for styling reasons).
* **Equal 2-Col Img or Text**  
  This row type has a single row of two equal-width columns that can contain Text, Image, or a combination of the two.

![Fancy Page Grid Layout Row Options](/images/fancy-page-2.png)

##### Fancy Page Classes #####
 There are a few CSS classes that can be added to rows, columns, or individual cells to style them in a specific way. When you click on a row or column settings icon to assign a class to that row/column/cell, the settings window opens, offering the following class options:

 ![Fancy Page CSS Class Options](/images/fancy-page-3.png)

 * **basic-box**  
    Select this class for separating the content to which it is applied using a thin grey border.

    ![Basic Box Example](/images/basic-box.png)
 * **big-heading**  
    Select this for heading rows (or cells) that you'd like to be larger than the default heading size. This is largely intended to be applied to the heading at the very top of a page. It can, of course, be used elsewhere there is a heading.
 * **centered-text**  
    Select this to center text. Useful especially for headings, but can be applied to any row/cell/column containing text content. The alignment of most text content can be overridden with this class.
 * **centered-img**  
    Select this to center image content. Will work in most cases, but there may be the occasional image that cannot be centered this way.
 * **display-on-small-screen**  
    Display this row/cell/column on small screens. Useful for cases when macros or images are hidden on smaller screens by default (usually to save data or avoid visual weirdness) and you want to display them anyway.
 * **hide-on-small-screen**  
    Hides this row/cell/column on smaller screens. Useful for cases when content that would otherwise be displayed on smaller screens should be hidden (if it looks terrible or doesn't scale down properly, for example).
 * **img-responsive**  
    Select this for image content that should automatically adjust its size to accomodate any device viewport. Most images should be doing this by default, but in the event that it's not scaling, using this class should help in most cases.
 * **invisibox**  
    Select this to pad content so that it aligns with *basic-box* content.
 * **light-grey-fancy-section**
    Select this class in order to set a light grey background with dark grey text.

    ![Light Grey Fancy Section Example](/images/light-grey-fancy-section.png)
 * **pretty-list**  
    Select this to format a content section that includes or consists entirely of a list. The main list items are displayed as large, bolded text and are *not* marked by bullet points. Nested list items are marked by empty circle bullet points.

    ![Pretty List Example](/images/pretty-list-1.png)
 * **pretty-little-list**  
    Select this class to format a content section that includes or consists of entirely of a list. The list does not really have to be small (it was meant to be applied to smaller lists at first, but now exists mostly to offer another option for formatting list content). The list items are bold text marked by square bullet points. (The grey background in the example screenshot is the result of applying the light-grey-fancy-section class to this content's container and is not part of the pretty-little-list styling.)

    ![Pretty Little List Example](/images/pretty-little-list-1.png)

 * **white-fancy-section**
    Apply this to content to make the section background white and the text color whichever text color is set to be used for the main text content on this page. It will pad content exactly as the *white-on-blue-fancy-section*, *white-on-red-fancy-section*, and the *white-on-slate-fancy-section* classes do.
 * **white-on-blue-fancy-section**
    Select this to pad content and set the section's background to navy blue and its text color to white.
 * **white-on-red-fancy-section**
    Select this to pad content and set the section's background to brick red and its text color to white.
 * **white-on-slate-fancy-section**
    Select this to pad content and set the section's background to dark slate grey and its text color to white.
 * **[blank]**  
    Select this to remove a class previously assigned to this row/column/cell.

> Note: Applying classes to entire rows or individual cells may slightly affect alignment. Experiment with different arrangements of rows if some rows seem to be having slightly different indentation or other such alignment weirdness.

[Return to Table of Contents](#table-of-contents)

#### Clever Page ####
This page is specifically designed to display information about the Clever service.

##### Clever Page Properties #####
###### Basic Tab ######
**Page Title**:  This is the title for this page (as it will appear on the browser bar).
**Hide in navigation?**: Check to keep this page from appearing as a  navigation menu item.

###### Content Tab ######
**Main Heading**: This is the overall heading for the page.  
**Folded Ribbon Aside**: This section accomodates several macros that differ slightly in term so the content they can contain.  
**Heading With Text Section**:  This section consists of a heading and some text content below that. As many of these sections can be added as needed (since this is a property that uses [Archetype][20]).  
**Q and A Section**:  This section consists of collapsible question and answer pairs (as many as needed). They do not need to be *questions* or *answers* at all (as can be seen on the screenshot that I've included). As many of these sections can be added as needed (as this property also makes use of the [Archetype][20] property editor).

The anatomy of a clever page (annotations in orange):

![Clever Page Anatomy](/images/clever-page-1.png)

[Return to Table of Contents](#table-of-contents)

### intoCareers Macros ###
#### ContactFormFrame ####
The ContactFormFrame macro is a small, straightforward partial-view macro with only one parameter: **stateCode**. The stateCode (or client code) must consist of exactly two letters.

The partial view itself consists almost entirely of an iframe pulling in the actual form from a remote source (the value of which is assigned to the `src` attribute).

```html
@inherits Umbraco.Web.Macros.PartialViewMacroPage
<section class="contact-form">
	<iframe
  class="contact-iframe" src="https://cistemp.intocareers.org/TechSupportForm/default.aspx?State=@Model.MacroParameters["stateCode"]"
  width="540"
  height="540"
  frameborder="0"
  align="middle">
  </iframe>
</section>
```
Apart from entering a state code/client code, nothing else needs to be done with this macro.

[Return to Table of Contents](#table-of-contents)

#### FontAwesomeLargeIcon ####
The FontAwesomeLargeIcon macro that displays a large icon has only one parameter: **icon**, which takes the name of a Font Awesome icon (e.g. fa-rocket). A full list of Font Awesome icon names (and the icons they summon) can be found on the official [Font Awesome Cheatsheet][36].

[Return to Table of Contents](#table-of-contents)

#### LoginBox2 ####
The "LoginBox2" macro is the most basic login macro available. The fields that need to be filled out for the macro are:

**Login Box Heading**: This heading will show up in large leterring at the top of the box. It could be something like "CIS Login", "NJCAN Login", or just plain "Login."

**Additional Login Box Text**: This text gives users a little bit of guidance for completing the form. Suggested text: "Log in below with ANY of your **[ClientAcronym]** account usernames or passwords."

**Login Form Submission Url**: This is the url to which this login form will be sent for processing. The current formula for intoCareers sites is: `https://[client].intocareers.org/loginmain.aspx`    
*Example*: https://ecis.intocareers.org/loginmain.aspx`

**Password/Username Recovery Url**: This is the url for the page containing the form for recovery lost passwords and/or usernames. The current formula for intoCareers sites is:`https://[client].intocareers.org/login_getpassword.aspx`   
*Example*: https://ecis.intocareers.org/login_getpassword.aspx

The partial view Razor code for this macro:

```html
@inherits Umbraco.Web.Macros.PartialViewMacroPage
@{
	IPublishedContent homeNode = Model.Content.AncestorOrSelf(1);
	var settingsNode = Umbraco.TypedContent(homeNode.GetProperty("settingsNode").Value);
	var loginBoxColor = settingsNode.GetProperty("loginTabColorPicker").Value.ToString();
	var loginTextColor = settingsNode.GetProperty("loginTextColor").Value.ToString();

	var bgStyle = "background-color:#" + loginBoxColor;
	var textStyle = "color:#" + loginTextColor;
}
<section class="login-tabs-section">
	<div id="login" class="login-box" style="@bgStyle">
		<header class="login-header">
			<h2 class="login-box-heading" style="@textStyle">@Html.Raw(@Model.MacroParameters["loginBoxHeading"])</h2>
			<p style="@textStyle">@Html.Raw(@Model.MacroParameters["loginTabText"])</p>
		</header>
		<div class="login-form">
			@Html.Partial("LoginForm", new intoCareers.Models.LoginVM(), new ViewDataDictionary {{"customAction", Model.MacroParameters["customAction"]}})
		</div>
		<div class="recovery-link-section">
			<p class="@textStyle">
				<a href="@Model.MacroParameters["forgotPasswordOrUsername"]" style="@textStyle">Forgot your username or password?</a>
			</p>
		</div>
	</div>
</section>
```

[Return to Table of Contents](#table-of-contents)

#### LoginBoxLinked1 ####
The "LoginBoxLinked1" macro is the basic login macro that allows an extra button link be set. This link could be to something like a "Just Browsing"  or "Guest" version of the post-login intoCareers sites. The fields that need to be filled out for the macro are:

**Login Box Heading**: This heading will show up in large leterring at the top of the box. It could be something like "CIS Login", "NJCAN Login", or just plain "Login."

**Additional Login Box Text**: This text gives users a little bit of guidance for completing the form. Suggested text: "Log in below with ANY of your **[ClientAcronym]** account usernames or passwords."

**Login Form Submission Url**: This is the url to which this login form will be sent for processing. The current formula for intoCareers sites is: `https://[client].intocareers.org/loginmain.aspx`    
*Example*: https://ecis.intocareers.org/loginmain.aspx`

**Password/Username Recovery Url**: This is the url for the page containing the form for recovery lost passwords and/or usernames. The current formula for intoCareers sites is:`https://[client].intocareers.org/login_getpassword.aspx`   
*Example*: https://ecis.intocareers.org/login_getpassword.aspx

**Button Link Label**: This is the text that will be on the linked button.

**Button Link Url**: This is the url to which the user will go if the user clicks the button.

The macro settings pane:

![Macro](/images/login-macro-1.png)

The resulting login widget:

![Macro](/images/login-macro-2.png)

The LoginBoxLinked1 partial view Razor markup:

```html
@inherits Umbraco.Web.Macros.PartialViewMacroPage
@{
	IPublishedContent homeNode = Model.Content.AncestorOrSelf(1);
	var settingsNode = Umbraco.TypedContent(homeNode.GetProperty("settingsNode").Value);
	var loginBoxColor = settingsNode.GetProperty("loginTabColorPicker").Value.ToString();
	var loginTextColor = settingsNode.GetProperty("loginTextColor").Value.ToString();

	var bgStyle = "background-color:#" + loginBoxColor;
	var textStyle = "color:#" + loginTextColor;
}
<section class="login-tabs-section">
	<div id="login" class="login-box" style="@bgStyle">
		<header class="login-header">
			<h2 class="login-box-heading" style="@textStyle">@Html.Raw(@Model.MacroParameters["loginBoxHeading"])</h2>
			<p style="@textStyle">@Html.Raw(@Model.MacroParameters["loginBoxText"])</p>
		</header>
		<div class="login-form">
			@Html.Partial("LoginForm", new intoCareers.Models.LoginVM(), new ViewDataDictionary {{"customAction", @Model.MacroParameters["customAction"]}})
		</div>
		<div class="recovery-link-section">
			<p class="@textStyle">
				<a href="@Model.MacroParameters["forgotPasswordOrUsername"]" style="@textStyle">Forgot your username or password?</a>
			</p>
		</div>
		<div class="login-link-section-1">
			<a href="@Html.Raw(@Model.MacroParameters["btnLinkUrl"])" target="_blank">
				<button type="button" class="login-box-link btn btn-block">
					@Html.Raw(@Model.MacroParameters["btnLinkLabel"])
				</button>
			</a>
		</div>
	</div>
</section>
```

[Return to Table of Contents](#table-of-contents)

#### LoginBoxLinked2 ####
Similar to the [LoginBoxLinked1](#loginboxlinked1) macro, this macro allows button links to be added to the login box area. The major different between the two, is that LoginBoxLinked1 accomodates **1** button link and LoginBoxLinked2 accomodates **2**.

A loginbox created using this macro will look something like:

![LoginBoxLinked2 Macro](/images/login-macro-3.png)

The code/markup for these two macros are mostly the same, except that the LoginBoxLinked2 macro replaces the login-link-section-1 `div` section with:

```html
<div class="login-link-section-2">
			<a href="@Html.Raw(@Model.MacroParameters["btnLinkUrl1"])" class="login-button-link" target="_blank">
				<button type="button" class="btn">
					@Html.Raw(@Model.MacroParameters["btnLinkLabel1"])
				</button>
			</a>
			<a href="@Html.Raw(@Model.MacroParameters["btnLinkUrl2"])" class="login-button-link" target="_blank">
				<button type="button" class="btn">
					@Html.Raw(@Model.MacroParameters["btnLinkLabel2"])
				</button>
			</a>
		</div>
```

[Return to Table of Contents](#table-of-contents)

#### LoginTabs2LinkedTab ####
Though it bears some similarities to the LoginBox macros above, the LoginTabs2LinkedTab is different in some key ones. One of the major differences is that login-related content can be split across two tabs (though the first tab must contain a standard login form). For the most part, the fields that need to be entered once the macro is created or when it is edited are nearly the same as the properties for the [LoginBox](#loginbox2) [types](#loginboxlinked1) [above](#loginboxlinked2).

The first tab (the main login tab) looks something like this:

![LoginTabs2LinkedTab Tab 1](/images/login-tab-macro-2.png)

The second tab looks something like this:

![LoginTabs2LinkedTab Tab 2](/images/login-tab-macro-1.png)

The second tab is designed to include three--exactly three--linkable buttons. It is suggested that the three button links be related to each other and be login-related more generally (like in the example login tabs displayed above).

[Return to Table of Contents](#table-of-contents)

#### LoginTabs2LinkedPlus ####
The LoginTabs2LinkedPlus macro is virtually identical to the [LoginTabs2LinkedTab](#logintabs2linkedtab) macro, except for one thing:
instead of supporting three button links in the second tab, it supports *four*. How exciting!

[Return to Table of Contents](#table-of-contents)

#### LoginTabs2TabLink ####
This is a stupid Login Tabs login macro that treats the second tab as a direct link. It is otherwise pretty much the same as the regular old login box. Why link to something by way of the tab (and I mean the *tab* itself, not the contents)? Because this is how some of the older portal sites do it and a few clients want to keep it that way, probably for continuity and/or habit reasons.

##### LoginTabs2TabLink Parameters #####
**Login Tab Title**: This is the title for the first tab.

**Second Tab Title**: This is the title for the second tab (i.e. the text that is used to link to another destination page or site).

**Second Tab Link**: This is the URL that the second tab title will go to when clicked. If it is an internal page, the entire URL is necessary (relative paths will not work). See the [Frequently Asked Questions](#frequently-asked-questions) for information about finding a page's full URL.

**Login Tab Intro Text**: This text will appear at the top of the login tab. This text is typically something like "Log in below with ANY of your CIS account usernames or passwords."

**Form Submission URL**: This is the URL of the page that will be processing the login form when a user tries to log in.

**Password/Username Recovery Link**: This is the URL of the page that allows the user to retrieve a lost username or password.

[Return to Table of Contents](#table-of-contents)

#### LoginTabs2TabLinkPlusClever ####
This is almost identical to the LoginTabs2TabLink macro, except that it adds a button that the user can click to be taken to a Clever login page.
##### LoginTabs2TabLinkPlusClever Parameters #####
This macro includes all of the parameters needed by the LoginTabs2TabLink macro (albeit in a slightly different order), but requires the following additional information:  
**Clever Login URL**: This is the URL for the Clever login page.

**Clever Login Image**: This is the button image that the user can click on to be taken to the Clever page. Various sizes of Clever button images can be found by navigating here: Media --> Brands --> Clever.

[Return to Table of Contents](#table-of-contents)

#### ParchmentForm ####
The ParchmentForm is a plug-n-play macro that contains the HTML (and [Razor][21]) necessary for retrieving and displaying the form for contacting [Parchment][22]. It can simply be plunked into a page using the "IC Portal Static Parchment Page" document type and does not require any additional data.

[Return to Table of Contents](#table-of-contents)

#### SidebarFoldedImageTop ####
The SidebarFoldedImageTop macro is tailored to fit "IC Portal Static Parchment Page" pages. After its properties have been set, it will look something like this:

![SidebarFoldedImageTop Screenshot](/images/parchment-page-5.png)

This macro requires a few different pieces of information: **Top Image** and **Folded Sidebar Text**.

The parchment image banner_logo.png (which can be found inside the Brands subfolder of the Media folder) is the recommended image for a Parchment page. An image selected for this property must be 300 x 56 pixels in order for it to be displayed correctly.

The Folded Sidebar Text is the text that appears on the folded aside, directly beneath the "top image." Recommended text: "Enable transcript order with [Client] Career Information System ([ClientCISAcronym]) and Parchment"

![SidebarFoldedImageTop Screenshot 2](/images/sidebarfoldedimagetop-1.png)

[Return to Table of Contents](#table-of-contents)

#### SmallCarousel ####
The SmallCarousel macro uses the [Owl Carousel][23] jQuery plugin. It cycles through a collection of (more or less) similar-sized images. When adding the SmallCarousel to a page (such as the left column area of the lower section of an "IC Portal Home 2"-type page), the macro will prompt you to select (or upload and then select) any number of images to display in the carousel.

![SmallCarousel Add Images](/images/smallcarousel-1.png)


[Return to Table of Contents](#table-of-contents)

#### SmallCarouselLinkable ####
The SmallCarouselLinkable macro is similar in appearance to the [SmallCarousel][#smallcarousel] macro, but is different in a few very important ways. The first major difference is that this macro requires that three--and only three--images be set when it is first added to a page.

![SmallCarouselLinkable Macro Prompt](/images/smallcarousel-linkable-1.png)

It also offers a textbox for inputting the url for wherever the user should end up after clicking on the corresponding image in the carousel.

![SmallCarouselLinkable Add Content](/images/smallcarousel-linkable-2.png)

It is important to note that it is okay to leave any or all of the link fields blank. The carousel works fine without links. (Though why a person not interested in attaching links to any of the carousel images might decide to use the SmallCarouselLinkable macro instead of the SmallCarousel macro is a mystery.)

![SmallCarouselLinkable OK To Leave Unlinked](/images/smallcarousel-linkable-3.png)

[Return to Table of Contents](#table-of-contents)

#### SmallCarouselLinkable4Items ####
Same as [SmallCarouselLinkable](#smallcarousellinkable) except that it can accomodate 4 items (linked, unlinked, or a mixture between the two).

[Return to Table of Contents](#table-of-contents)

### Advanced Customization Options ###
#### Change Color Picker Colors ####
So you wanna add a new color to the color pickers, huh? Thankfully, adding and removing colors from the color pickers (such as the navigation bar color picker) is fairly straightforward. If you wish to do this but cannot see the "Settings" tab in the Umbraco backoffice, ask your site administrator for more generous permissions.

The first thing to do is to navigate to the "Document Types" folder in the the Settings tab of the backoffice. If the folder is collapsed collapsed, uncollapse it so that you can see all of the document types.

All of the color pickers for the intoCareers site are currently located in the ["IC Portal Settings"](#settings-page) document type.

![Add Colors to Color Picker 1](/images/add-colors-1.png)

Though it looks like there are more, there are only 5 different color pickers at this time. Some of the color pickers are used more than once, but there are only 5 *distinct* color picker property editors.

The color pickers available are:
The **background color picker** ("IC Portal Settings - Background Color - Color Picker"), which exclusively sets the main background for pages across the site. Any colors added to this picker should be light enough that black text contrasts with them enough that the text is still comfortably readable.

![Add Colors to Color Picker 2](/images/add-colors-3.png)

The **navbar color picker** ("IC Portal Settings - Navbar Color Picker - Color Picker") sets the background color of the main navigation bar and the **navbar text color picker** ("IC Portal Settings - Navbar Text Color - Color Picker") sets the color of any text on the navbar (navigation link items included). These color pickers are also used to set the background and text color of the page footer. Changing the color selection of either of the navigation color pickers will also change the color options for the footer. It is important to note that the available color options for the footer are the only things apart from the nav colors affected by altering these color pickers. Once a settings page has been created (or when it is in the process of being created), the colors chosen for the navbar and footer can, of course, be different. It is only the selection that is the same.

![Add Colors to Color Picker 3](/images/add-colors-4.png)

Notice the names of the data types for the footer color pickers:

![Add Colors to Color Picker 4](/images/add-colors-2.png)

The last two color pickers are the **login tab color picker** ("IC Portal Settings - Login Tab Color Picker - Color Picker") and the **login text color picker**("IC Portal Settings - Login Text Color - Color Picker"). The *second* login tab color picker property actually uses the same color picker as the login tab color picker:

![Add Colors to Color Picker 5](/images/add-colors-5.png)

Once you know which color picker you want to alter, click on the gear icon in the top right corner of a property that uses it:

![Add Colors to Color Picker 6](/images/add-colors-6.png)

This will open a property settings pane to the right. Click on the gear next to the property editor:

![Add Colors to Color Picker 7](/images/add-colors-7.png)

(The data type settings can also be accessed more directly by sifting through the list of "Data Types" in the "Developer" tab.)

This will open a pane of top of the property settings pane that allow for the addition and removal of colors. To add a color, click the dropdown next to the "Add" button:

![Add Colors to Color Picker 8](/images/add-colors-8.png)

This will open a color wheel. Select a color by clicking on the appropriate color on the color wheel or by entering a color hex code. Click "Add" and submit your changes.

![Add Colors to Color Picker 9](/images/add-colors-9.png)

To remove colors, simply click the red "Remove" button next to any offending colors and submit your changes.

>TIP: Be mindful of the site's color scheme! It's easy to choose colors that aaaalmost look right, but are just a teensy bit off. Try using a color scheme tool like [Coolors][24] or [Adobe Color CC][25] to make sure that your colors work well together.  

[Return to Table of Contents](#table-of-contents)

#### Add New Stylesheets ####
The easiest way to add a new stylesheet to use on an Umbraco intoCareers site is to navigate to the "Settings" tab of the Umbraco backoffice, click on the ellipsis menu that appears upon hovering over the Stylesheets folder, and select the "Create" option.

![Add New Stylesheets 1](/images/add-new-styles-1.png)

Give the stylesheet a name. The name should be a css filename and *must* include the ".css" file extension.

![Add New Stylesheets 2](/images/add-new-styles-2.png)

Click "Create" and then select the generated stylesheet, which appears in the list of stylesheets in the "Stylesheet" folder. Copy and paste the desired styles (*all of them*) in the appropriate area. Click "Save" and...that's it!

![Add New Stylesheets 3](/images/add-new-styles-3.png)

[Return to Table of Contents](#table-of-contents)

#### Change Stylesheet Picker Dropdown ####
In order to add new stylesheets to the stylesheet selection dropdowns in the "IC Portal Settings" document type, navigate to the "Document Types" folder (which lives inside the Umbraco Backoffice "Settings" tab), and click on the "IC Portal Settings" document type. See [Change Color Picker Colors](#change-color-picker-colors) section for more detailed instructions about finding this type.

Find the property with the dropdown you want to offer and click the property settings gear icon in the upper right corner of that property:

![Change Stylesheet Picker Dropdown 1](/images/add-stylesheet-1.png)

This will open up the property settings pane. From here, click on the settings gear icon for the property editor itself:

![Change Stylesheet Picker Dropdown 2](/images/add-stylesheet-2.png)

(The data type settings can also be accessed more directly by sifting through the list of "Data Types" in the "Developer" tab.)

This will open an editor settings pane. In this pane, type the filename of the CSS file (already existing in the Stylesheets folder in Umbraco), including the ".css" file extension you want to add. Click "Add" and submit your changes.

Removing a stylesheet is as simple as clicking the red "Remove" button next to the stylesheet you want to remove from the dropdown and submit your changes.

![Change Stylesheet Picker Dropdown 3](/images/add-stylesheet-3.png)

[Return to Table of Contents](#table-of-contents)

### Examples ###
TODO: Ask content managers what examples they would like to see. Then write this section.

[Return to Table of Contents](#table-of-contents)

### URL Rewriting ###
> IMPORTANT: This section should be used as a reference instead of as an instructional manual or tutorial. It is meant to help with understanding the rules that are already configured in the event that rule-related issues crop up or in case rewrite rules need to be added to a new client site. Configuring rewrite rules for a new site will mostly be a matter of copypasting XML snippets into sites' Web.config files. See the linked resources for tutorials and other information that will aid in writing new rules. [Jump to the bottom](#new-site-procedure) of this section for the step-by-step procedure for adding rules to a new site.

In order for the portal sites to be deployed, their urls need to be rewritten to appear as expected. For example, "https://portal.intocareers.org/ex" will need to appear to the user as "https://ecis.intocareers.org"
and its subpages like "https://portal.intocareers.org/ex/whats-new/" need to be displayed as "https://ecis.intocareers.org/whats-new/".

The way that URL  is accomplished is through a process called URL rewriting, which (in this case) makes use of the [URL Rewrite][28] and [Application Request Routing][29] modules for [IIS][27].

The type of URL Rewriting used to display the desired URLs for the portal sites is known as a "reverse proxy." A "reverse proxy" makes it possible to use another server to act as a "proxy" for a site residing on a different server and allows URLs to be rewritten. The portal sites need to look as if they live side-by-side with the post-login intoCareers sites.

Altering url rewrite rules is generally not a good idea unless you know really what you're doing, but it may come in handy to know the whats, the wheres, the hows, and the whys of them, especially for troubleshooting or for adapting the rewrite rules for a new portal site.

Most--but not all!--of the rewriting can be done in a portal site's Web.config file (located in the root directory of the production site directory).

> IMPORTANT: Whenever altering the Web.config, copypaste it first into the same folder so that you can revert the site to its previous state  if you bork it up

The portal rewrite rules use [regular expressions][31] to match and capture patterns. [RegExr][32] is a good tool for testing regular expressions. There are two types of rewrite rules that are needed for a reverse proxy for a portal site:

#### Inbound Rules ####    
These rules rewrite urls from the server where the sites actually live to technical urls of the sites on the proxy server. Inbound rule example:

```xml
<rule name="Rewrite Subpage Rule 1" enabled="true" stopProcessing="true">
  <match url="^portal/(.*)"/>
  <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
    <add input="{CACHE_URL}" pattern="^(.*)://"/>
  </conditions>
  <action type="Rewrite" url="{C:1}://portal.intocareers.org/ex/{R:1}" logRewrittenUrl="false"/>
</rule>
```
Oy. For such a small, simple rule, it sure looks like there's a lot going on! Let's break it down piece by piece to make it a bit easier to parse:

The rule must have a **name**. It can really be anything, but it is advised to use descriptive names that convey its purpose.

> HOT TIP: Rules should never have the same name (this will confuse IIS).

There is also an option to disable the rule. To do this simply set the enabled attribute to false: `enabled="false"`. This is useful for when a rule is causing problems, but you don't want to throw it out. (It may just require a minor tweak here or there.)

Don't worry too much about `stopProcessing="true"`. Most of the tutorials recommend setting this attribute to "true".

The `<match url="^portal/(.*)" />` part of the rule contains the regular expression that captures urls (or parts of urls, in this case) that match the pattern. The bit in parentheses is what is called a "capture group". For a url like `/portal/whats-new/`, the `/whats-new/` is what is captured. Each capture group is assigned a number--starting at 1--that can be used in a **back reference** to plug captured text into a rewritten url.

The back reference in this rule is the `{R:1}` tacked onto the end of the rewritten url. Using a back reference, the `/whats-new/` in the example can be preserved without having to hard-code it.

You may on occassion run into rewrite rules with `{R:0}` back references. This refers to the entire url captured. In the example, a `{R:0}` back reference would be `/portal/whats-new/`.

The `{C:1}` is a stand-in for a **condition**. This particular condition makes it so that the rewritten url is protocol-agnostic (i.e. it doesn't matter whether it's `http` or `https`). The regular expression pattern is used to capture everything between those parentheses (the `(.*)` part) and then plugs whatever protocol it captures into the rewritten url. This condition preserves the original protocol, though that is not always desirable. Forcing `https` in some way or another is a good idea for security reasons.

The `<action type="Rewrite" url="{C:1}://portal.intocareers.org/ex/{R:1}" logRewrittenUrl="false">` section is where the type of rule (rewrite or redirect) and the desired format for the URL are specified.

#### Outbound Rules ####

If URL rewriting is your flavor, you can learn more about writing them [here][33]. The results from googling "URL Rewrite IIS tutorial" may also be useful.

Aaaaanyway.

The rewrite rules should be inserted somewhere in between the `<system.webServer>` and `</system.webServer>` tags. In the portal sites' Web.config files, the rewrite rules should be sandwiched between the `<security></security>` and `<httpProtocol></httpProtocol>` sections (but not *inside* those sections).

Directly beneath the `<httpProtocol>` section, there is a single setting that must be smooshed in there (still within the `<system.webServer>` tags):

```xml
<urlCompression doStaticCompression="false" doDynamicCompression="true" dynamicCompressionBeforeCache="false"/>
```

Outbound rewrite rules (i.e. rewrite rules that spit out the rewritten URL) will not work with static compression, so it's important to enable to dynamic compression.

Enabling dynamic compression alone will not completely fix outbound rewrite rule compression issues. If the server (the proxy server) does not have it already, a registry key will need to be added as well. More about the workaround for getting outbound rules to work in a reverse proxy situation can be found [here][30].

The portal rewrite rules look like this:

```xml
<rewrite>
  <rules>
    <clear/>
    <rule name="Redirect to HTTPS" enabled="true" stopProcessing="true">
      <match url="(.*)"/>
      <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
        <add input="{HTTPS}" pattern="^OFF$"/>
      </conditions>
      <action type="Redirect" url="https://{HTTP_HOST}/{R:1}" redirectType="Permanent"/>
    </rule>
    <rule name="Rewrite Media Path Rule" enabled="true" stopProcessing="true">
      <match url="^media/([0-9]{4})/(.*)$" ignoreCase="false" negate="false"/>
      <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
        <add input="{CACHE_URL}" pattern="^(.*)://"/>
      </conditions>
      <action type="Rewrite" url="{C:1}://portal.intocareers.org/media/{R:1}/{R:2}" logRewrittenUrl="false"/>
    </rule>
    <rule name="Rewrite Stylesheet Path Rule" enabled="true" stopProcessing="true">
      <match url="^css/(.+)$"/>
      <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
        <add input="{CACHE_URL}" pattern="^(.*)://"/>
      </conditions>
      <action type="Rewrite" url="{C:1}://portal.intocareers.org/{R:0}" logRewrittenUrl="false"/>
    </rule>
    <rule name="Rewrite Script Path Rule" enabled="true" stopProcessing="true">
      <match url="^scripts/(.+)$"/>
      <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
        <add input="{CACHE_URL}" pattern="^(.*)://"/>
      </conditions>
      <action type="Rewrite" url="{C:1}://portal.intocareers.org/{R:0}" logRewrittenUrl="false"/>
    </rule>
    <rule name="Rewrite Font Path Rule" enabled="true" stopProcessing="true">
      <match url="^fonts/(.+)$"/>
      <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
        <add input="{CACHE_URL}" pattern="^(.*)://"/>
      </conditions>
      <action type="Rewrite" url="{C:1}://portal.intocareers.org/fonts/{R:1}" logRewrittenUrl="false"/>
    </rule>
    <rule name="Reverse Proxy Inbound Rule 1" enabled="true" stopProcessing="true">
      <match url="(.*)"/>
      <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
        <add input="{CACHE_URL}" pattern="^(.*)://"/>
      </conditions>
      <action type="Rewrite" url="{C:1}://portal.intocareers.org/ex/{R:1}" logRewrittenUrl="false"/>
    </rule>
  </rules>
  <outboundRules rewriteBeforeCache="true">
    <clear/>
    <rule name="Reverse Proxy Outbound Rule" preCondition="ResponseIsHtml1" enabled="true" stopProcessing="true">
      <match filterByTags="A, Form, Input, Link" pattern="^http(s)?://portal.intocareers.org/ex/(.*)"/>
      <conditions logicalGrouping="MatchAll" trackAllCaptures="true"/>
      <action type="Rewrite" value="/{R:2}"/>
    </rule>
    <rule name="Rewrite Relative Paths" preCondition="ResponseIsHtml1" enabled="true" stopProcessing="true">
      <match filterByTags="A, Form, Input, Link" pattern="^/ex/(.*)"/>
      <conditions logicalGrouping="MatchAll" trackAllCaptures="true"/>
      <action type="Rewrite" value="/{R:1}"/>
    </rule>
    <preConditions>
      <preCondition name="ResponseIsHtml1">
        <add input="{RESPONSE_CONTENT_TYPE}" pattern="^text/html"/>
      </preCondition>
    </preConditions>
  </outboundRules>
</rewrite>
```

Yikes! That's a lot of rules! The fewer the rules the better, but Umbraco's weird site structure necessitates the use of many of them.

You may be thinking, *what did I just look at nope nope nope*.

To which I might respond (telepathically?), *It's not as complicated as it looks, but I can see why it might seem a little overwhelming.*

#### Adding Rules When There Is No Web.config File (Yet )####
It is possible that there might not yet *be* a web.config file to which you can add rewrite rules. In that case, you may have to use the IIS Manager GUI on the server (presently) called The Thing to add the rules. A web.config file will be automatically generated when you add rules this way.

TODO: Add more here.

#### New Site Procedure ####
1. Find a set a rules . Copypaste rewrite rules into the Web.config located in the site's root directory. Make sure that bits that specifically reference a client site are correct. For example, if you're making a site for Puerto Rico, you will need to change any instances of the copypasted rules.
2. Make sure that dynamic compression is enabled and that static compression is disabled. Add after the `<httpProtocol>` subsection of the `<system.webServer>` section:
```xml
<urlCompression doStaticCompression="false" doDynamicCompression="true" dynamicCompressionBeforeCache="false"/>
```
3. Modify `portal.html` (located in [site root directory]-->materials-->portal) by commenting out the original meta tag so that it looks like this:
```html
<!--<meta http-equiv="Refresh" content="0; url=materials/portal/home.html" />-->
```
and then plunk the following html into portal.html above or below the commented-out `meta` tag:
```html
<meta http-equiv="Refresh" content="0; url=portal/" />
```
4. Add a new location to the location section of the Web.config:
```xml
	<location path="portal">
		<system.web>
			<authorization>
				<allow users="*"/>
			</authorization>
		</system.web>
	</location>
```
5. The "Redirect to HTTPS" rule will probably need to be disabled (set enabled="false" or disable it via the IIS GUI), as it can conflict with other forms of forcing the user to use a more secure protocol like Require SSL.
6. Make sure that "Enable proxy" is checked (this option can be found in the ARR module, which resides at the root level for ALL sites on the server, not just the current site).


[Return to Table of Contents](#table-of-contents)

### Accessibility ###
Making a site accessible in Umbraco can occasionally be tricky, especially when dealing with grid layouts and certain macros.

TODO: Add much much more here.

The [Ally Project][26] has a useful checklist for figuring out what needs to be done in order to make a website more accessible and inclusive.

[Return to Table of Contents](#table-of-contents)

### Frequently Asked Questions ###
TODO: Ask content managers which questions they would like to see answered here. Screenshot and note all Umbraco errors that crop up. (Especially the ones that are basically meaningless and can be banished by a simple page reload.) Then write this section.

**How do I find out the full URL of an Umbraco page?**    
In case you need to link to an internal page by using its full URL, you can find out the URL by first selecting the page for which you need to know the URL in the site's node tree.

Next, navigate to the page's "Properties" tab:    
![Properties Tab](/images/properties-tab-find-url-1.png)    

Once you've done that, find the "Link to document" section near or at the bottom of the Properties tab window. There are two different URLs listed. The first one is the relative link. The one beneath it is the full "friendly" URL:
![Friendly URL](/images/properties-tab-find-url-2.png)    

[Return to Table of Contents](#table-of-contents)

### What Next ###
This project is not perfect. Far from it, in fact. It is a little messy and there are some bad practices that leeched into it. ([Mistakes were made][38]...) The goal of this section is to list out a few ideas for how the project can be cleaned up and improved when there is the time to do so:  

* Refactor the Sass to better conform to best practices and eliminate some of the redundancy that crept in over time (the Sass was beautiful for a hot second there)
* Standardize margins, padding, and other layout/positioning styles by incorporating more flexbox styles wherever possible
* Investigate updating Owl Carousel widget to the 2.x. Replace Owl Carousel with the newer version if it looks like it'll play nice with Umbraco (and if it is an improvement over the 1.x versions).  
* Investigate using the [Formulate][37] plugin to create and handle forms within Umbraco. It can be accessed through "Formulate" tab in the Umbraco backoffice (if you cannot see it on the main backoffice navigation menu, ask your admin for the permissions to view and work with it). Formulate is a free alternative to Umbraco's paid Forms module. If there's the money for it and if the latest iteration is considered reliable by devs, use Forms instead (as you can be fairly certain that it will be better supported over a longer period of time). That said, Formulate is (as of the writing of this) considered to be reliable, well-supported, user-friendly, and it is widely used.
* Create new document types for document types that are either too rigid or too flexible.
* Add a Single Page Application document type.
* Get rid of the "checkbox hack" that is currently used on the navigation menu to make items clickable in favor of a simple jQuery plugin that is tab-able (for acessibility), readable by screen readers (also for accessibility), and clickable (for mobile and other touchscreen devices). The checkbox hack was supposed to be a very lightweight, css-only solution, but its problems far outweigh its benefits at this point.
* Upgrade to Umbraco 7.6 or newer. Be very careful. Read Umbraco's official instructions on how to do this without borking the entire project. There may also be some radical changes, so gird your loins for dealing with that.

There is a "Shadow" folder inside the list of available Document Types under the "Settings" tab of the backoffice and a corresponding folder in the list of available Templates (also under the "Settings" tab of the backoffice) that is meant to be a start in the direction of creating a cleaner set of document types and templates for the future. You are welcome to use them as a jumping-off point, as a base for building better document types (to eventually replace the current ones), or to ridicule my creative process.

Please note and date any issues that have been addressed in this documentation.

[Return to Table of Contents](#table-of-contents)

### Additional Resources ###
#### Official Umbraco Documentation ###
[Umbraco TV][11] – Some free videos with text versions of those videos, but most of the good stuff is paywalled.

#### Semi-Official Umbraco Documentation ####
[OurUmbraco][3] – Has some documentation as well as forums that may answer questions you have. Be sure to check the date that something was last updated. Some of the documentation is dated or concerns earlier version of Umbraco. Umbraco 7 is apparently quite different from earlier versions, so that is something to keep in mind on this site.

#### Accessibility Resources ####
[A11y Project Accessibility Checklist][26] - A checklist that can be used to go through a site and determine areas in which the accessibility/inclusivity can be improved.

#### Other Resources ####
[24 Days In Umbraco][12] – While largely geared toward more advanced Umbraco developers, there are a lot of enormously helpful and surprisingly accessible tidbits scattered throughout. Since each year contains different topics, it’s worth looking at the most recent few years. 2013 and 2014 are a little dated, but there is quite a bit that still applies.
* [2016 Version][12]
* [2015 Version][13]
* [2014 Version][14]
* [2013 Version][15]

[Jon D. Jones Umbraco Tutorials][16] – A treasure trove of current, easy-to-follow and -understand Umbraco tutorials and tips.

[YouTube][17] – Don’t forget about poor little YouTube! Searching YouTube will likely turn up some great (and some not-so-great) tips and tutorials.

[Return to Table of Contents](#table-of-contents)

[1]: https://www.umbraco.com "Umbraco"
[2]: https://www.asp.net/mvc "ASP.NET MVC"
[3]: http://www.ourumbraco.org "OurUmbraco.org"
[4]: https://our.umbraco.org/documentation/Getting-Started/Backoffice/ "Umbraco Backoffice Documentation"
[5]: https://our.umbraco.org/documentation/getting-started/data/data-types/ "Umbraco Data Types Documentation"
[6]: http://www.iep.utm.edu/plato/#SH6b "Plato's Theory of Forms"
[7]: https://en.wikipedia.org/wiki/Camel_case "camelCase"
[8]: http://umbraco.tv/videos/umbraco-v7/implementor/fundamentals/document-types/list-view-and-templates-menu/documentation "Umbraco.tv List View Video"
[9]: http://umbraco.tv/videos/umbraco-v7/implementor/fundamentals/document-types/what-is-a-document-type/documentation "Umbraco.tv Document Type Video"
[10]: https://our.umbraco.org/documentation/tutorials/creating-basic-site/document-types "OurUmbraco.org Document Types Documentation"
[11]: http://www.umbraco.tv/ "Umbraco.tv Videos"
[12]: http://24days.in/umbraco-cms/2016/ "24 Days in Umbraco 2016 Articles"
[13]: http://24days.in/umbraco-cms/2015/ "24 Days in Umbraco 2015 Articles"
[14]: http://24days.in/umbraco-cms/2014/ "24 Days in Umbraco 2014 Articles"
[15]: http://24days.in/umbraco-cms/2013/ "24 Days in Umbraco 2013 Articles"
[16]: http://jondjones.com/category/umbraco/ "Jon D. Jones Umbraco Tutorials"
[17]: http://www.youtube.com "YouTube"
[18]: http://www.htmldog.com/guides/css/intermediate/classid/ "HTMLDog CSS Classes"
[19]: https://our.umbraco.org/documentation/getting-started/backoffice/property-editors/built-in-property-editors/Grid-Layout/What-Are-Grid-Layouts "OurUmbraco.org Grid Layout Property Editor Documentation"
[20]: http://imulus.github.io/Archetype/ "The Archetype Umbraco Property Editor"
[21]: http://www.w3schools.com/asp/razor_intro.asp "Razor Markup"
[22]: http://www.parchment.com/ "Parchment"
[23]: http://www.landmarkmlp.com/js-plugin/owl.carousel/ "Owl Carousel"
[24]: https://coolors.co/ "Coolors Color Scheme Tool"
[25]: https://color.adobe.com/ "Adobe Color CC"
[26]: http://a11yproject.com/checklist.html "A11y Project Accessibility Checklist"
[27]: https://www.iis.net/learn "Internet Information Services (IIS)"
[28]: https://www.iis.net/downloads/microsoft/url-rewrite "URL Rewrite IIS Module"
[29]: https://www.iis.net/downloads/microsoft/application-request-routing "ARR IIS Module"
[30]: https://blogs.msdn.microsoft.com/manjug/2014/07/12/workaround-for-outbound-rewriting-can-be-used-together-with-iis-dynamic-compression/ "URL Rewrite Compression Workaround"
[31]: https://msdn.microsoft.com/en-us/library/az24scfc(v=vs.110).aspx "Regular Expressions Overview"
[32]: http://regexr.com/ "RegExr Tool for Learning, Building, and Testing Regular Expressions"
[33]: https://www.iis.net/learn/extensions/url-rewrite-module/creating-rewrite-rules-for-the-url-rewrite-module "IIS Url Rewrite Module How-To"
[34]: https://material.io/guidelines/components/cards.html "Material Design Component Guidelines - Cards"
[35]: http://fontawesome.io/ "Font Awesome"
[36]: http://fontawesome.io/cheatsheet/ "Font Awesome Cheat Sheet"
[37]: https://our.umbraco.org/projects/backoffice-extensions/formulate/ "Formulate"
[38]: https://en.wikipedia.org/wiki/Mistakes_were_made "Mistakes were made"
