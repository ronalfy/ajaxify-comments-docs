---
description: Edit comments with Ajaxify Comments
---

# Comment Edit Core

Comment Edit Core allows you to edit comments for up to 5 minutes.

{% embed url="https://wordpress.org/plugins/simple-comment-editing/" %}

To ensure compatibility between Comment Edit Core and Ajaxify Comments, you can update the `OnAfterUpdateComments` callback with the following snippet:

```javascript
window.SCE_comments_updated(commentUrl)
```

<figure><img src="../.gitbook/assets/dlxplugins-1695325979496-1x.webp" alt=""><figcaption><p>OnAfterUpdateComments Callback for Comment Edit Core</p></figcaption></figure>

You should now be able to edit comments when new comments are posted.
