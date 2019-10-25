## [3.0.0](https://github.com/TravelTripperWeb-Sites/blank-template/releases/3.0.0)

Overall changes:

* Refactored crs and conversion plus/ttweb plugins settings into conversion-plus submodule
* Fixed package.json to compile JS during npm run start
* new structure for default layout
* added include for docready fix (fire post-css)
* rename rt3api.min.js to cp.min.js
* rename conversion_plus settings to conversion_plus_banner settings
* rename ttweb_plugins settings to conversion_plus settings
* created default _data/_cms_config/content_nav.yml file for configuring CMS menu
* create layouts for CMS and dynamic rooms and offers
* remove required setting for most fields in most models
* changed CSS import to handle bedrock themes
* change config.yml to handle bedrock themes

### New Deafult Layout

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

This will be an option in the CMS in the future.


