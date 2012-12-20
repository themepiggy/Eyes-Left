# Welcome to Eyes Left

Eyes Left is a content over chrome website designed for those who don't need the complexity of multiple pages. Eyes Left is, by design, a one page site with all content available on the page. Based on the popular Twitter Bootstrap, Eyes Left is also a responsive theme that takes advantage of media queries to layout elements for different resolutions.

Even though it is designed for smaller sites, Eyes Left understands that your content will logically fall into categories. To support this, a left hand side menu exists and will hot-link you to various portions of your content. If you prefer to read through it all though, Eyes Left will simply keep the menu in place and highlight the appropriate menu item as you scroll.

# Customization

Eyes Left uses a simple system of defining hash tags and divs to allow people using the site to quickly jump to the topic of their choice.

The source code is divided into two sections - the menu and the content. These sections are marked with HTML comments - <!-- MENU --> and <!-- CONTENT -->

To edit the menu, simply open the index.html file and find the portion that looks like this:

    <div class="menu-items">
      <ul class="nav nav-list">
        <li class="active"><a href="#home">Home</a></li>
        <li><a href="#customisation">Customization</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>

Note that each menu item has an href tag with a hash tag in it. Each hash tag binds to div which has an id with the same name as the hash tag.

So for example, we are currently in the "customization" section - in the menu, the code looks like this:

    <li><a href="#customisation">Customization</a></li>

Looking to the content section, we can find a div with the relevant id:

    <div id="customisation">

This wires up the "Customization" menu item to the content on the page and allows browsers to "jump" to the right content.

This menu system is simple to extend - adding a new item is a matter of creating a new "li" item with a hash tag - for example adding a new menu item like this

    <li><a href="#lolcats">Pictures of moggy</a></li

Will create a new menu item with the title "Pictures of moggy". All that you need to do to add the content is surround it with a div that has an id tag of "lolcats". For example

    <div id="lolcats">My funny kitty kat pictures</div>

And hey-presto, your new menu item will automatically be wired up.