# Changing Labels Programmatically

You can use filter `dlxplugins/ajaxify/comments/options/pre_output` to filter the options returned by the plugin.

The filter accepts 3 arguments:

* `$options`: (array) Optioons array containing the labels.
* `$post_id`: (int) Post ID of the comment being posted to.
* `$post_type`: (string) Post type of the comment being posted to.

Here is an example of changing the labels for WooCommerce reviews:

```php
<?php
/**
 * This snippet demonstrates changing the labels for the WooCommerce product reviews.
 */
add_action( 'plugins_loaded', 'dlx_my_ajaxify_plugins_loaded' );

/**
 * Run when the plugin is loaded.
 */
function dlx_my_ajaxify_plugins_loaded() {
	add_filter( 'dlxplugins/ajaxify/comments/options/pre_output', 'dlx_ajaxify_comments_options', 10, 3 );
}

/**
 * Modify options before they are output.
 *
 * @param array  $options    The options to output.
 * @param int    $post_id    The post ID the options are being output to.
 * @param string $post_type The post type the options are being output to.
 */
function dlx_ajaxify_comments_options( $options, $post_id, $post_type ) {
	// Check if WooCommerce product, and change a few strings.
	if ( 'product' === $post_type ) {

		// Change the text for the reviews and messages.
		$options['textPosted']                   = __( 'Your review has been posted. Thank you!', 'plugin-domain' );
		$options['textPostedUnapproved']         = __( 'Your review has been posted and is awaiting moderation. Thank you!', 'plugin-domain' );
		$options['textReloadPage']               = __( 'Reloading page. Please wait.', 'plugin-domain' );
		$options['textPostComment']              = __( 'Posting your review. Please wait.', 'plugin-domain' );
		$options['textRefreshComments']          = __( 'Loading reviews. Please wait.', 'plugin-domain' );
		$options['textUnknownError']             = __( 'Something went wrong, your review has not been posted.', 'plugin-domain' );
		$options['textErrorTypeComment']         = __( 'Please type your review text.', 'plugin-domain' );
		$options['textErrorCommentsClosed']      = __( 'Sorry, reviews are closed for this item.', 'plugin-domain' );
		$options['textErrorMustBeLoggedIn']      = __( 'Sorry, you must be logged in to post a review.', 'plugin-domain' );
		$options['textErrorFillRequiredFields']  = __( 'Please fill the required fields (name, email).', 'plugin-domain' );
		$options['textErrorInvalidEmailAddress'] = __( 'Please enter a valid email address.', 'plugin-domain' );
		$options['textErrorPostTooQuickly']      = __( 'You are posting reviews too quickly. Please wait a minute and resubmit your review.', 'plugin-domain' );
		$options['textErrorDuplicateComment']    = __( 'Duplicate review detected. It looks like you have already submitted this review.', 'plugin-domain' );

	}
	return $options;
}
```
