# Actions and Filters

### Action: Execute code before Ajaxify starts loading in

#### Action definition:

{% code overflow="wrap" %}
```php
/**
 * Fires before the main WPAC actions/filters. Useful for hooking in early.
 */
do_action( 'dlxplugins/ajaxify/comments/wp' );
```
{% endcode %}

### Action: Execute code after Ajaxify enqueues its scripts

#### Action definition:

```php
/**
 * Do action after scripts are enqueued.
 */
do_action( 'dlxplugins/ajaxify/comments/enqueue_scripts', $version, $in_footer );
```

This action is executed after all of Ajaxify Comments' scripts have been enqueued. This is useful to run custom scripts after Ajaxify Comments.

### Filter: Force Ajaxify Comments to load

Regardless if Ajaxify Comments is disabled, you can pass `true` to force load the scripts and functionality needed to take over the comment section. This can still be overruled by the `dlxplugins/ajaxify/comments/can_load` filter.

#### Filter definition:

{% code overflow="wrap" %}
```php
/**
 * Filter whether to load the plugin's scripts.
 *
 * @param bool $can_force_script_override Whether to load the plugin's scripts. Pass `true` to force scripts to load.
 */
$can_force_script_override = apply_filters( 'dlxplugins/ajaxify/comments/force_load', false );
```
{% endcode %}

### Filter: Block Ajaxify Comments from loading

Prevent any loading of Ajaxify Comments scripts or functionality regarding the comment section.

#### Filter definition:

{% code overflow="wrap" %}
```php
/**
 * Filter whether to load the plugin's scripts.
 *
 * @since 2.0.0
 *
 * @param bool $can_load Whether to load the plugin's scripts. Pass `false` to prevent scripts from loading.
 */
$can_load = apply_filters( 'dlxplugins/ajaxify/comments/can_load', true );
if ( ! $can_load ) {
	return;
}
```
{% endcode %}

### Filter: Prevent Activation Redirect

This next filter, if `false` is returned, will not redirect the plugin to the plugin's settings screen after activation.

#### Filter definition:

{% code overflow="wrap" %}
```php
/**
 * Filter whether to redirect on plugin activation.
 *
 * @param bool $can_redirect Whether to redirect on plugin activation. Pass `false` to prevent redirect.
 */
$can_redirect = apply_filters( 'dlxplugins/ajaxify/comments/activation/can_redirect', true );
```
{% endcode %}

### Filter: Return a Custom Color Palette in the Admin

Ajaxify Comments allows changing the alert and text colors in the Appearance settings of the admin.

{% content-ref url="../../customization/appearance-settings.md" %}
[appearance-settings.md](../../customization/appearance-settings.md)
{% endcontent-ref %}

When selecting colors, Ajaxify attempts to get the theme's colors. You can return custom colors by hooking into this next filter.

#### Filter definition:

{% code overflow="wrap" %}
```php
/**
 * Filter the color palette.
 *
 * @param array $color_palette Color palette {
 *   @type string $name Primary color name.
 *   @type string $slug Primary color slug.
 *   @type string $color Primary color hex or var.
 * }
 */
return apply_filters( 'ajaxify/comments/theme_color_palette', $color_palette );
```
{% endcode %}

### Filter: Filter the options before they are output as JSON

Filter the options before they are output via JSON as settings. This can be used to manipulate labels or settings per post and post type.

**Filter definition:**

```php
/**
 * Filter the options before they are output.
 * This is useful for adding custom options or modifying labels.
 *
 * @param array  $options The options to be output.
 * @param int    $post_id The post ID.
 * @param string $post_type The post type.
 */
$options = apply_filters(
	'dlxplugins/ajaxify/comments/options/pre_output',
	$options,
	get_the_ID(),
	get_post_type( get_the_ID() )
);
```

{% content-ref url="changing-labels-programmatically.md" %}
[changing-labels-programmatically.md](changing-labels-programmatically.md)
{% endcontent-ref %}

### Need an action or filter?

Please [contact support](https://dlxplugins.com/support/).
