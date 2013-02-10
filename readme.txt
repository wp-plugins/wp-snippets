=== WP Snippets ===

Contributors: WebSharks
Donate link: http://www.s2member.com/donate/
Tags: snippet, snippets, include, includes, shortcode, shortcodes, php, post type, post types, utilities, posts, pages

License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Stable tag: 130206
Requires at least: 3.2
Tested up to: 3.6-alpha

Create Snippets! This plugin adds a new Post Type. Snippets can be included in other Posts/Pages/Widgets via Shortcodes. A very lightweight plugin!

== Description ==

This plugin is VERY simple. There are NO configuration options necessary.

This plugin adds a new Post Type. This plugin makes it SUPER easy to reuse fragments of content (i.e. Snippets). Snippets can be included in other Posts/Pages/Widgets via Shortcodes. This is a very lightweight plugin!

After installing this plugin, create a new Snippet (find menu item on the left in your Dashboard). Give your Snippet a Slug (i.e. under the title of your Snippet). Once you have a Snippet and a Slug, you can include your Snippet anywhere you like — in other Posts/Pages/Widgets (and even inside PHP template files).

Using a Snippet that you've created in the WP Editor. Follow this simple Shortcode syntax.

	[snippet slug="my-cool-snippet" /]

Using a Snippet that you've created inside a PHP template file.

	<?php echo do_shortcode('[snippet slug="my-cool-snippet" /]'); ?>

== Frequently Asked Questions ==

#### How do I use a Snippet that I create?

Using a Snippet that you've created in the WP Editor. Follow this simple Shortcode syntax.

	[snippet slug="my-cool-snippet" /]

Using a Snippet that you've created inside a PHP template file.

	<?php echo do_shortcode('[snippet slug="my-cool-snippet" /]'); ?>

#### Who can manage Snippets in the Dashboard?

By default, only WordPress® Administrators can manage (i.e. create/edit) Snippets (anyone who can edit Posts/Pages can use them though). If you would like to give others the Capabilities required, please use a plugin like [Enhanced Capability Manager](http://wordpress.org/extend/plugins/capability-manager-enhanced/).

Add the following Capabilities to the additional Roles that should be allowed to manage Snippets.

	$caps = array
			(
				'edit_snippets',
				'edit_others_snippets',
				'edit_published_snippets',
				'edit_private_snippets',
				'publish_snippets',
				'delete_snippets',
				'delete_private_snippets',
				'delete_published_snippets',
				'delete_others_snippets',
				'read_private_snippets'
			);

#### Is it possible to use other Shortcodes inside a Snippet?

Yes. Absolutely. You can even nest one Snippet inside another one via Shortcodes.

#### I also installed the [Raw HTML plugin](http://wordpress.org/extend/plugins/raw-html/). Can I use Raw HTML inside a Snippet?

Yes. When creating a new Snippet, please wrap your Snippet content with `[raw][/raw]` tags; or with `<!--raw--><!--/raw-->` tags. Consult the [Raw HTML documentation](http://wordpress.org/extend/plugins/raw-html/) on this please. An important point to make is that Snippets are self-contained. Applying Raw HTML to a Post/Page that includes a Snippet via `[snippet slug="my-snippet" /]`, will NOT apply Raw HTML to the Snippet content itself. You must wrap the Snippet content with raw tags to achieve this. This actually provides a great deal of flexibility, because it allows you to have a Raw HTML Post or Page, but have Snippets that were designed in the WP Visual Editor (or vice versa — and even mixtures, if you include multiple Snippets).

#### I also installed the [ezPHP plugin](http://wordpress.org/extend/plugins/ezphp/). Can I use PHP tags inside a Snippet?

Yes. Absolutely. I recommend [ezPHP](http://wordpress.org/extend/plugins/ezphp/), but WP Snippets are also compatible with [Exec-PHP](http://wordpress.org/extend/plugins/exec-php/).

#### I also installed the [s2Member® plugin](http://wordpress.org/extend/plugins/s2member/). Can I protect content in Snippets conditionally?

Yes. Absolutely. I recommend this KB article: [s2Member® Simple Conditionals](http://www.s2member.com/kb/simple-shortcode-conditionals/). s2Member's Simple Shortcode Conditionals can be used inside a Snippet itself, or by wrapping your Snippet Shortcode when you put it into a Post or Page. Either way is fine.

== Installation ==

= WP Snippets is very easy to install (instructions) =
1. Upload the `/wp-snippets` folder to your `/wp-content/plugins/` directory.
2. Activate the plugin through the `Plugins` menu in WordPress®.
3. Use Snippets in your Posts/Pages/Widgets via Shortcodes.

	[snippet slug="my-cool-snippet" /]

== Changelog ==

= v130206 =
 * Initial release.