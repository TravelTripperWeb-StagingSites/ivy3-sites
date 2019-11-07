## [3.0.0](https://github.com/TravelTripperWeb-Sites/blank-template/releases/3.0.0)

Overall changes:

* Refactored crs and conversion plus/ttweb plugins settings into conversion-plus submodule
* Fixed package.json to compile JS during npm run start
* new structure for default layout
* added include for docready fix (fire post-css)
* rename rt3api.min.js to cp.min.js
* rename conversion_plus settings to conversion_plus_banner settings
* rename ttweb_plugins settings to conversion_plus settings
* add RVNG settings options
* created default _data/_cms_config/content_nav.yml file for configuring CMS menu
* create layouts for CMS and dynamic rooms and offers (including featured sub-lists)
* remove required setting for most fields in most models
* changed CSS import to handle bedrock themes
* change config.yml to handle bedrock themes
* removed gallery layout (just use generic page and add a gallery picker region)
* added default settings_nav file - use this to manage whether BRG or CP settings are shown
* updated JS compilation to use webpack
* node package updates for security
* add accessibility to attractions map
* siteindex.json files (for searches) with LoadSiteIndex function and basic search page implementation
* LoastPostsIndex function and basic posts.json usage implementation (load-more action)
* update SEO to allow for explicit vs title-partials
* update page-gen to allow for SEO fields (meta.meta_tile, .meta_title_prefix, .meta_description)

### Note:

The _includes/components files may be used as-is and styled to fit the needs of the site. However they're intended as "maximal" examples and it's generally recommended you override these files to display the fields and HTML structure you need.

When using a them, the files in _includes/components are more intended to be used directly without need for modification as they are already designed to work for the given theme.

### New Default Layout

Includes many more entry points so default layout can be customized globally without having to override the entire layout.


### Content Nav config

Now that ther's a default config file, you'll need to update it if you want to add/remove model types to the list.


### Options for rooms and offers

The default page list now includes an offers list, offer detail, rooms list and room detail page that all refer to the dynamic layout versions that do not use CMS content models at all. You can switch these layouts and enable rooms/offers models in the CMS Content Nav for any of the following cases

* Rooms/Offers pages have custom designs that require data not provided by the CRS
* Rooms/Offers content needs to be translated into multiple languages
* Rooms/Offers content needs to be reused in various places on the site in complex ways.
* SEO performance for dynamic rooms/offers content becomes an issue


### Using themes

For now to switch themes you'll need to make 5 updates

* in _config.yml change all the references to theme folder, replacing 'none' with 'hg01' in the 4 relevant paths
* in _sass/_theme-selection.scss change 'none' to 'hg01' in 1 line

There will be a way to automate this via the CMS in the future


