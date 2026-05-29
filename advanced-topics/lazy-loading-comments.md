---
description: Lazy loading comments can improve performance
---

# Lazy Loading Comments

Lazy-loading comments can improve the page load of your blog posts and pages. If there are a lot of comments on a post, this can slow down the page's loading speed.

<figure><img src="../.gitbook/assets/dlxplugins-1698260663513-1x.webp" alt=""><figcaption><p>Lazy Loading Admin Options</p></figcaption></figure>

### Prerequisite: Please set your selectors first

{% hint style="danger" %}
**Make sure you set your selectors first.** You can use Menu Helper to help set your selectors.
{% endhint %}

{% content-ref url="selectors.md" %}
[selectors.md](selectors.md)
{% endcontent-ref %}

{% content-ref url="../first-time-users/menu-helper.md" %}
[menu-helper.md](../first-time-users/menu-helper.md)
{% endcontent-ref %}

### Enabling Lazy Loading

<figure><img src="../.gitbook/assets/dlxplugins-1698261017234-1x.webp" alt=""><figcaption><p>Enable Lazy Loading Option</p></figcaption></figure>

Find the Lazy Load options in the admin settings. The first option on the page allows you to enable or disable lazy loading for comments.

{% content-ref url="../first-time-users/finding-the-settings.md" %}
[finding-the-settings.md](../first-time-users/finding-the-settings.md)
{% endcontent-ref %}

### Testing Lazy Loading

You can use Menu Helper to simulate lazy loading before it's activated.

<figure><img src="../.gitbook/assets/dlxplugins-1698261200693-1x.webp" alt=""><figcaption><p>Simulate Lazy Loading Enabled or Disabled</p></figcaption></figure>

{% content-ref url="../first-time-users/menu-helper.md" %}
[menu-helper.md](../first-time-users/menu-helper.md)
{% endcontent-ref %}

### Setting the Triggers

<figure><img src="../.gitbook/assets/dlxplugins-1698261368161-1x.webp" alt=""><figcaption><p>The Types of Lazy Load Triggers</p></figcaption></figure>

Here are the types of Triggers and what you can do for each one.

#### External Trigger

Comments do not load unless specifically invoked by an external source.

The external source will want to call this JavaScript function to load in the comments:

```javascript
WPAC.RefreshComments();
```

#### Comments Scrolled Into Viewport

<figure><img src="../.gitbook/assets/dlxplugins-1698261793566-1x.webp" alt=""><figcaption><p>Comments Scrolled Into Viewport Option</p></figcaption></figure>

This option allows Ajaxify Comments to load when the comments section has been reached. This will be useful for never loading the comments for the user until that user reaches further down the page in the comments section.

You can adjust a vertical scroll offset (in pixels) to "trigger" loading a certain distance above the comments section.

#### Dom Ready (Default)

<figure><img src="../.gitbook/assets/dlxplugins-1698261893790-1x.webp" alt=""><figcaption><p>Dom Ready Option</p></figcaption></figure>

This will load comments once the page has finished loading. This is the default behavior.

#### Dom Element Reached

<figure><img src="../.gitbook/assets/dlxplugins-1698261959635-1x.webp" alt=""><figcaption><p>Dom Element Reached</p></figcaption></figure>

This option allows you to set which HTML element or CSS selector must be scrolled into view in order to load comments.

{% hint style="danger" %}
**Use a valid CSS selector using jQuery notation** (`.css-class,#css-id,form`)
{% endhint %}

For example, if you set a selector to some Related Posts at the bottom of your content, the comments will load in when the posts are scrolled into view.

You can set the scroll offset so that the loading occurs a certain number of pixels above the offset.

{% hint style="info" %}
**Units are in pixels**: Scroll offset is in pixels.
{% endhint %}

#### Scroll Distance Trigger

<figure><img src="../.gitbook/assets/dlxplugins-1698262222499-1x.webp" alt=""><figcaption><p>Load Comments a Number of Pixels from the Top</p></figcaption></figure>

You can set the loading trigger to be scroll distance. This will load the comments when a user reaches a certain number of pixels from the top of the screen.

### Setting the Loading Settings and Messages

<figure><img src="../.gitbook/assets/dlxplugins-1698262626669-1x.webp" alt=""><figcaption><p>Overlay Options</p></figcaption></figure>

You can choose between an overlay or no overlay for lazy loading. An animation of the loading popover is below.

<figure><img src="../.gitbook/assets/lazy-load-comments-trigger.gif" alt=""><figcaption><p>Lazy Loading Overlay</p></figcaption></figure>

The Overlay can be configured in the Appearance settings.

{% content-ref url="../customization/appearance-settings.md" %}
[appearance-settings.md](../customization/appearance-settings.md)
{% endcontent-ref %}
