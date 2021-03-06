=== Church Community Builder Core API ===
Contributors: jaredcobb
Tags: ccb, church, api, chms
Requires at least: 3.0.1
Tested up to: 4.3.1
Stable tag: 0.9.6
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Provides a core integration to the Church Community Builder API.

== Description ==

Church Community Builder Core API *synchronizes* your church data to WordPress [custom post types](https://codex.wordpress.org/Custom_Post_Types).
This plugin is geared toward developers (or advanced WordPress users who aren't afraid to get into a little bit of code).

Find out more at [http://www.wpccb.com/](http://www.wpccb.com).

= Why Use This Plugin? =

One of the biggest challenges with getting your Church Community Builder data onto your site is the actual API integration.
This plugin does all of the heavy lifting for you. Once your church data is securely synchronized you can use it freely in
your theme, widgets, or even your own plugins!

= Features =

* Get your Public Groups
* Get your Public Events
* Auto-synchronize (set it and forget it)
* Manually synchronize anytime
* Cached data (extremely fast)
* Works in the background (never interrupts you or your visitors)
* Secure (API communication is encypted, and so are your credentials)

= Documentation =

The [http://www.wpccb.com/documentation/](official documentation) has more information, including code samples, hooks, filters, and links to tutorials.

== Installation ==

1. Upload the entire plugin folder to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress
1. You'll find a settings page in a sidebar menu titled "CCB Core API"
1. Enter your Church Community Builder software subdomain
1. Enter your Church Community Builder API credentials
1. Enable the synchronizations you'd like

== Frequently Asked Questions ==

= I installed this plugin and my site doesn't look any different =

This plugin has a very specific task: It gets some of your Church Community Builder data and imports it into your
WordPress database (as custom post types). A developer (or advanced WordPress administrator) will need to
alter your theme to *take advantage* of this data.

= Some of my groups in Church Community Builder aren't being synchronized =

You'll need to ensure your [group settings](https://support.churchcommunitybuilder.com/customer/portal/articles/361764-editing-groups)
allow the group to be publicly listed. A great way to cross reference if your group is publicly visible is to visit
*yoursubdomain*.ccbchurch.com/w_group_list.php and see if the missing group shows up there.

== Screenshots ==

1. screenshot-1.png
2. screenshot-2.png

== Changelog ==

= 0.9.6 =
* Added automatic flushing of rewrite rules when custom post type settings are changed
* Added link to official documentation in README and About page

= 0.9.5 =
* Added an option to import Group Images as the Featured Image (no longer referencing the CCB CDN location which expires quickly)
* Added filters which allow you to customize the API to Custom Post Type mappings:
 * `add_filter( 'ccb_include_group_participants' )`, whether or not to ask the API to include group participants in the response
 * `add_filter( 'ccb_get_groups_taxonomy_map' )`, ability to customize the taxonomy mapping for groups
 * `add_filter( 'ccb_get_groups_custom_fields_map' )`, ability to customize the custom fields mapping for groups
 * `add_filter( 'ccb_get_calendar_taxonomy_map' )`, ability to customize the taxonomy mapping for events
 * `add_filter( 'ccb_get_calendar_custom_fields_map' )`, ability to customize the custom fields mapping for events
* Added ability to automatically import collections of meta data (for example, multiple group leaders)

= 0.9.4 =
* Added Group "Meet At" address and longitude / latitude coordinates as custom fields

= 0.9.3 =
* Fixed a bug for backwards compatibility with PHP 5.2 servers

= 0.9.2 =
* Added tooltips to some settings to help explain the functionality
* Added better defaults for date ranges
* Updated the plugin web site to http://www.wpccb.com

= 0.9.1 =
* Fixed an issue where some web hosts were not saving encypted passwords

= 0.9.0 =
* Initial release
