# Equinox
Theme For glFusion

# Installation
Warning, although this theme will work without them, this theme employs some advanced "Static Page Hackery" to work properly.
Thanks Mark for your help!!!

Create Static Pages (Go to the Pages Admin)

   A. Create a page with an id of equinox_topic_header with execute PHP (Return) selected in the attributes tab then add the following code and save.
```
if ( isset( $_GET['topic'] )) {
    $topic = COM_applyFilter( $_GET['topic'] );
} else if ( isset( $_POST['topic'] )) {
    $topic = COM_applyFilter( $_POST['topic'] );
} else {
    $topic = '';
}
if ( $topic != '' ) {
    echo PLG_replaceTags("[staticpage_content:equinox_header_".$topic."]");
}
```
With this you can create a header for any topic you would like. Just create a static page with equinox_topic_topicid.

   B. Create a page with an id of "equinox_landing_logo" (The following will enable the demo content. You may put what ever you would like here.)
   ```
   <div class="uk-cover uk-position-relative" style="height: 600px;" data-uk-scrollspy="{cls:'uk-animation-fade', delay:900}">
    <img class="uk-invisible" src="" width="" height="" alt="">
    <video class="uk-cover-object uk-position-absolute" width="640" height="360" autoplay loop muted>
    <source src="/layout/equinox/demo/video/rain.mp4" type="video/mp4" /></video>
   <div class="uk-position-cover uk-overlay-panel uk-flex uk-flex-center uk-flex-middle" data-uk-scrollspy="{cls:'uk-animation-scale-down', delay:1100}">
   <img  class="uk-width-1-2" src="/layout/equinox/demo/images/equinox.png">
   </div>
   </div>
   ```

   C. To control the footer logo create a static page with the id of "equinox_footer_logo". (Just replace with whatever image path or other content to what you you like, the folowing will enable the demo content.)
   ```
   <img class="uk-width-medium-1-4" src="/layout/equinox/demo/images/equinox.png">
   ```

   D. To Control the Mobile nav bar logo create a a static page with the id of "equinox_mobile_nav". (Just replace with whatever image path or other content to what you you like, the folowing will enable the demo content.)
   ```
   <style>
.eq-nav-brand {
max-width:200px!important;
}
</style>
<img class="uk-responsive-width uk-animation-scale" src="/layout/equinox/demo/images/equinox.png" >
   ```

   E. To change headers for each topic you will need to create staticpages with the id of equinox_header_topic_id. The "topic_id" should be the id of the topic you would like to change. Topics without a staticpage will have no header image.

# Dependencies
glFusion 1.6.2 or Higher (https://www.glfusion.org)
CMS theme that comes with glFusion
