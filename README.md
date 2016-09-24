# Equinox 
Theme For glFusion

#Installation
Warning, although this theme will work without them, this theme employs some advanced "Static Page Hackery" to work properly.
Thanks Mark for your help!!!

1. Upload Equinox to your layout directory, usuaully in /public_html/layout.

2. Create Static Pages (Go to the Pages Admin)

   A. Create a page with an id of equinox_landing_logo with execute PHP (Return) selected in the attributes tab then add the follow code and save. 
```php   
   if ( isset( $_GET['topic'] )) {
    $topic = COM_applyFilter( $_GET['topic'] );
} else if ( isset( $_POST['topic'] )) {
    $topic = COM_applyFilter( $_POST['topic'] );
} else {
    $topic = '';
}
if ( $topic != '' ) {
    echo PLG_replaceTags("[staticpage_content:header_".$topic."]");
}
```  

   B. Create a page with an id of equinox_topic_header
   C. 
#Dependencies
glFusion 1.6.2 or Higher (https://www.glfusion.org)
CMS theme that comes with glFusion
