# Installation
This module change the callback of link twig extenstion.

From your drupal root run the following commands:
  drush en -y menu_twig

This module provide the textarea to rewrite the menu or render the twig extestions and twig filters.


Some of the sample code find below:

1 . Add some text / image after the Link

Step 1. Navigate through : Structure > Menu > Main navigation > Add Link

Step 2. Expend the link "MENU TWIG" by click on it.

Step 3. See the textarea inside the link "MENU TWIG". Now choose the text editor then write some text/ insert image inside the textarea and save the form.


2 . Rewrite the link / Add attributes to link

Step 1. Navigate through : Structure > Menu > Main navigation > Add Link

Step 2. Expend the link "MENU TWIG" by click on it.

Step 3. Check the checkbox says "Exclude the menu item or override the menu item with text editor".

Step 4. Please find the some examples help to rewrite the link twig link function.

         Example 1:   {{ link(title, url)}}
         Example 2:   {{ link(title, url, { 'class':['overwrite_link']}) }}
         Example 3:   <a href="{{url}}" >{{title}}</a>


3 . Render the custom block / view block

Step 1. To render the custom block / view block I am using the additional module "Twig tweak". See some examples

Step 2. Navigate through : Structure > Menu > Main navigation > Add Link

Step 3. Expend the link "MENU TWIG" by click on it.

Step 4. Write the twig extension code inside the textarea to render the block with link itself.

         Example 1:   {{ drupal_view('who_s_new', 'block_1') }}

4 . How to use twig extension filters / functions with Menu Twig

Step 1. Navigate through : Structure > Menu > Main navigation > Add Link

Step 2. Expend the link "MENU TWIG" by click on it.

Step 3. You will find the link says "filters" and "functions" under description of textarea. Click on the links and you will find the all availble twig functions and filters available in system.

Step 4. Twig provides a number of handy functions that can be used directly within Templates. For more infomation please go through the article.

Step 5. Filters in Twig can be used to modify variables. Filters are separated from the variable by a pipe symbol. They may have optional arguments in parentheses. Multiple filters can be chained. The output of one filter is applied to the next. For more infomation please go through the article.

         Example 1:   <a href="{{ url('view.frontpage.page_1') }}">{{ 'View all content'|t }}</a>

5 . Optimize the html output render by twig extension

Step 1. Navigate through : Structure > Menu > Main navigation > Add Link

Step 2. Expend the link "MENU TWIG" by click on it.

Step 3. Now we have two ways to optimize the output of twig extension. Let say twig extension example

{{ drupal_view('who_s_new', 'block_1') }}
.
Step 4. First 1: You can restrict the output of the twig extension by choose the textarea filter. For example choose Text format 'Restricted HTML' to get clean content.

Step 5. First 2: You can use twig extension filters for the same to strip the html using filter "striptags". See exmaple below:

        {% set whonew = drupal_view('who_s_new', 'block_1')  %}
        {{ whonew|render|striptags('<a>') |raw }}
