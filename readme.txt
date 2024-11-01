=== Tracking Code for Twitter Pixel ===
Contributors: claytoncollie
Donate link: https://www.claytoncollie.com/
Tags: google, analytics, tracking code, tag, universal analytics, tracking snippet
Requires at least: 4.8
Tested up to: 6.6.0
Requires PHP: 5.6
Stable tag: 1.0.0
License: GPLv3 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Simple, lightweight solution for inserting your Twitter Pixel Universal tracking code.

== Description ==

Tracking Code For Twitter Pixel is a simple, lightweight WordPress plugin for inserting your Twitter Pixel tracking code. The plugin does one thing and one thing only; prints the standard Twitter Pixel tacking script to the `<head>` of your website. To insert your tag ID, navigate to Settings > General and then scroll to the bottom of the page.

### Composer

`composer require claytoncollie/tracking-code-for-twitter-pixel`

### Filters

If you want to set the tag ID without using the wp-admin user interface, use the filter below.

`
add_filter(
	'tracking_code_for_twitter_pixel_id',
	/**
	 * Set Twitter Pixel tag ID.
	 *
	 * @param string $tag_id Tag ID.
	 *
	 * @return string
	 */
	function ( $tag_id ) {
		return '123456789';
	}
);
`

### Contributing

While the purpose of this plugin is to be very tightly scoped, issues and pull requests are welcome, but I do not guarantee that everything will be merged or support will be given.

https://github.com/claytoncollie/tracking-code-for-twitter-pixel

== Installation ==

1. Upload `tracking-code-for-twitter-pixel` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Navigate to Settings > General > scroll to the bottom of the page
4. Insert your tag ID
5. Save your changes

== Frequently Asked Questions ==

= Why did you build this plugin? =

The plugins I have used in the past to solve this problem have too many features for my liking. This plugin is comprised two functions. One for registering a settings field on the Options General page. And another for printing the tracking code to the frontend. I want a lightweight solution for the websites that I build without all of the extra bells and whistles. If you are expecting this plugin to do more or grow in the future, please do not use it.

= Where is the tracking code inserted? =

The tracking code is inserted into the `<head>` section.

= Will this plugin slow down my website? =

No. This plugin is intentionally lightweight. All it does is register a settings field, saves to the database, and then inserts the tracking code. Nothing more.

= I found a bug. How do I report it? =

https://github.com/claytoncollie/tracking-code-for-twitter-pixel/issues

= Can I use this plugin with Composer? =

https://packagist.org/packages/claytoncollie/tracking-code-for-twitter-pixel

== Changelog ==

= 1.0.0 =
* Initial release