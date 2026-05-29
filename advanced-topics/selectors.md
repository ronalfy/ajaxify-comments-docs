# Selectors

Selectors help tell Ajaxify Comments about your comment section.

<figure><img src="../.gitbook/assets/dlxplugins-1695535471074-1x.webp" alt=""><figcaption><p>Selectors in the Admin Settings</p></figcaption></figure>

Selectors can be an advanced topic, so it's best to allow **Menu Helper** to help with finding the right selectors.

{% content-ref url="../first-time-users/menu-helper.md" %}
[menu-helper.md](../first-time-users/menu-helper.md)
{% endcontent-ref %}

To find the right selectors, it's recommended to open the developer tools in your browser and go to elements.

<figure><img src="../.gitbook/assets/dlxplugins-1695536444733-1x.webp" alt=""><figcaption><p>Default Selectors Shown</p></figcaption></figure>

{% hint style="danger" %}
Selectors must be compatible with jQuery notation. IDs must have a `#` sign and classes must have a `.` in front of them.
{% endhint %}

### Comments Container Selector

This container wraps the comments list. You can usually find it by opening the dev tools and finding an individual comment.

Trace this comment back to its parent container, and you'll find the container ID or class.

<figure><img src="../.gitbook/assets/dlxplugins-1695535801603-1x.webp" alt=""><figcaption><p>Find the wrapper around the individual comments</p></figcaption></figure>

### Comment Form Selector

This is the wrapper ID or class for the `form` element in the comments section.

<figure><img src="../.gitbook/assets/dlxplugins-1695535924098-1x.webp" alt=""><figcaption><p>Find the ID or Class of the comment form element</p></figcaption></figure>

This can usually be found by inspecting the comment form's textarea element and tracing it back to the `form` parent element.

### Respond Selector

This wraps the respond area for the comment section.

You can usually find this by selecting the comment form's textarea and tracing it back to the form's parent container.

<figure><img src="../.gitbook/assets/dlxplugins-1695536125001-1x.webp" alt=""><figcaption><p>The Respond Selector wraps the comment form</p></figcaption></figure>

### Comment Textarea Selector

This is the comment form's textarea field and can be found by selecting the comment's textarea.

<figure><img src="../.gitbook/assets/dlxplugins-1695536324121-1x.webp" alt=""><figcaption><p>Textarea field that shows the ID of the textarea</p></figcaption></figure>

### Comment Submit Button Selector

This is the submit button for the comment section. It can be found by selecting the submit button and finding the ID or class of the button or input.

<figure><img src="../.gitbook/assets/dlxplugins-1695536569688-1x.webp" alt=""><figcaption><p>Submit Button Selector Example</p></figcaption></figure>

### Advanced Selectors

Advanced Selectors must be in jQuery notation.
