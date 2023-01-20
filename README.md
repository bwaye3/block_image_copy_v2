# *Add to the subtheme.libraries.yml*

#Image Copy V2 <br />
gt-image-copy-v2: <br />
version: "2.0.x" <br />
css: <br />
theme: <br />
//cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css: { type: external } <br />
templates/block/custom/image_copy_v2/css/gt-image-copy.css: {} <br />
js: <br />
//cdnjs.cloudflare.com/ajax/libs/waypoints/4.0.1/jquery.waypoints.min.js: { type: external } <br />
templates/block/custom/image_copy_v2/js/waypoint.js: {} <br />
dependencies: <br />
- core/jquery <br />

# *Add to the repositories section in subtheme composer.json*

"repositories": [ <br />
{ <br />
"type": "vcs", <br />
"url": "https://github.gatech.edu/ICWebTeam/block_image_copy_v2.git" <br />
}
# *Add to the require in subtheme composer.json*

"require": { <br />
"gt/image_copy_v2": "dev-master" <br />
"mnsami/composer-custom-directory-installer": "^2.0"<br />
},

# *Add to the installer paths in subtheme composer.json*
"installer-paths": { <br />
"web/themes/custom/SUBTHEME/templates/block/custom/image_copy_v2": [ <br />
"gt/image_copy_v2" <br />
] <br />
},

# *Implements hook_page_attachments_alter(). in subtheme.theme*
function SUBTHEME_page_attachments_alter(&$page) {<br />
$page['#attached']['library'][] = 'SUBTHEME/image_copy_v2';<br />
}

# **CUSTOM BLOCK  SET-UP**
![](images/set-up.png)

# **TAXONOMY SET-UP**
![](images/animations.png)
