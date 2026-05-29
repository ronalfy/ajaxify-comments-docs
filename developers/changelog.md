# Changelog

### Changelog

#### 2.0.11

> Released 2023-10-06 Added support for the Ollie theme. Updated Menu Helper to better support block-enabled themes. Added WPML support to the plugin ([docs on how to set this up](https://docs.dlxplugins.com/v/ajaxify-comments/advanced-topics/wpml-and-translations)).

#### 2.0.9

> Released 2023-10-03 Added CSS class to overlay for easier styling. Added WPML config for translatable string options.

#### 2.0.7

> Released 2023-09-30 Placed `gettext` call only on comment posting, improving performance. Resolved improper `functions.php` inclusion. New filter for changing options before they are output as JSON.

#### 2.0.5

> Released 2023-09-28 Refactoring lazy loading. It should be much more reliable now. It has been tested with Astra, Twenty Twenty-Three, and Genesis themes. Updating Menu Helper to simulate lazy loading on or off.

#### 2.0.1

> Released 2023-09-27 Lazy loading was referencing the wrong variable. This has been fixed.

#### 2.0.0

> Released 2023-09-24 Renamed WP Ajaxify Comments to Ajaxify Comments in the admin. Updated branding. Completely refreshed admin interface. The admin is now organized into tabs with quick saving and reset options. Appearance tab allows for a real-time preview of the plugin's appearance. Appearance tab is a lot more user friendly, allowing for easy customization of the plugin's appearance. Added Support tab with helpful links to documentation and support. Removed admin notice on plugins screen. Replaced admin notice with contextual plugin row notice. This will display whenever debug mode is on, or if the plugin is disabled. Added first-time-installation notice for new users who are new to setting up the plugin. Added synthetic callback events for the available callbacks. This allows developers to hook into the plugin's events without having to modify the plugin's code. Callbacks have a slightly more secure implementation and execution. Added a tool called Selector Helper, which will help users find the right selectors for their theme. Please [read the announcement post](https://dlxplugins.com/announcements/ajaxify-comments-2-0-is-released/) for more information.

#### 1.7.5

> Released 2023-08-30 Ensuring compatibility with WordPress 6.3.

#### 1.7.4

> Fixed HTML5 validation warning for script tag

#### 1.7.3

> Updated default value for "Comments container selector" to work with default theme "Twenty Twenty" without breaking compatibility to older (default) themes

#### 1.7.2

> Added compatibility to older WordPress versions (< 5.2.0) and to WordPress 5.6

#### 1.7.1

> Added compatibility to latest WordPress versions >### 5.5.0 Updated Waypoints library to 4.0.1 Updated jQuery blockUI plugin to 2.70.0 Updated Idle Timer to 1.1.1 Updated jsUri to 1.3.1

#### 1.7.0

> Preserve focus element when reloading comments Fixed deprecated error in PHP 7.4

#### 1.6.2

> Added compatibility to latest WordPress versions

#### 1.6.1

> Optimized JavaScript injection

#### 1.6.0

> Removed dependency to PHP session

#### 1.5.1

> Fixed "Undefined variable: wpac\_options"

#### 1.5.0

> Added JavaScript callback "OnAfterPostComment"

#### 1.4.1

> Prevent the comment form from being submitted multiple times in parallel Fixed PHP notice "Undefined index: pagenow" (thanks to ravipatel)

#### 1.4.0

> Added (expert) option "Enable by query"

#### 1.3.0

> Added request parameters "WPACAll", "WPACSkip" and" WPACTake" to query comments

#### 1.2.0

> Added (expert) option "Disable cache" Use GET request when updating comments

#### 1.1.1

> Fixed link to settings page in admin frontend

#### 1.1.0

> Fixed compatibility to WordPress 4.1 Changed plugin name from "WP-Ajaxify-Comments" to "WP Ajaxify Comments"

#### 1.0.0

> Changed plugin owner to weweave an added professional support Added (expert) option "Base URL" to support reverse proxy configuration Fixed page title update for titles containing UTF-8 characters Typo fix in default localization

#### 0.25.0

> Loading comments now updates page title (thanks to Jincheng Shan) OnBeforeSubmitComment callback is now called before submitUrl is extracted

#### 0.24.1

> Updated localization for zh-CN (thanks to Jincheng Shan) Added CDATA tag for inline JavaScript (thanks to Jincheng Shan)

#### 0.24.0

> Added parameter commentUrl to callbacks OnBeforeUpdateComments and OnAfterUpdateComments

#### 0.23.1

> Changed order of links in plugin overview Make sure WPAC.\_Options is always initialized Bugfix for comment paging links

#### 0.23.0

> Added (expert) option "Place scripts in footer" Added option "Comment links selector" to prevent (complete) page loads for comment links on pages if "Break comments into pages \[...]" is enabled Bugfix for "Users must be registered and logged in to comment" Fixed PHP Notice for PHP < 5.4.0

#### 0.22.0

> Minor optimizations Added (expert) option "Optimize AJAX response" to save bandwidth Fixed JavaScript includes for HTTPS

#### 0.21.0

> Added option "Disable scroll to anchor" Fixed paging support and async comment loading for pages where comments are closed Fixed compressed JavaScript file Fixed support for URLs with comments anchor if async comment loading is enabled

#### 0.20.0

> Added option "Post container" to support for multiple comment forms per page Added option "Comment pages URL regex" to support none default WordPress comment pages

#### 0.19.0

> Added parameter newDom to callbacks OnBeforeUpdateComments and OnAfterUpdateComments Fixed JavaScript error "TypeError: WPAC.\_Options is undefined" (thanks to Suzanne Ahjira) Fixed JavaScript error in Internet Explorer (thanks to timhengeveld)

#### 0.18.1

> Fixed double slashes in JavaScript include (thanks to Mr Press)

#### 0.18.0

> Added option to define when to load comments asynchronously with secondary AJAX request Optimized JavaScript includes (use compressed/merged JavaScript file and only include files if they are needed)

#### 0.17.3

> Fixed "Undefined index" PHP notice (thanks to fergomez)

#### 0.17.2

> Fixed compatibility to wpMandrill (thanks to paddywagon)

#### 0.17.1

> "OnAfterUpdateComments" callback is now called after form data has been reset

#### 0.17.0

> Added options to customize (default) WordPress messages Disabled (auto) scrolling when comments are updated by "Auto update idle time" Fixed compatibility to jQuery "no conflict mode"

#### 0.16.1

> Bugfix for cross-domain scripting detection

#### 0.16.0

> Added option "Auto update idle time" to automatically update comments if user is "idle" Updated jQuery blockUI to 2.64

#### 0.15.0

> Added option to disable URL updating

#### 0.14.3

> Fixed some PHP strict warnings

#### 0.14.2

> Fixed compatibility to PHP < 5.4.0

#### 0.14.1

> Fixed compatibility to jQuery "no conflict mode"

#### 0.14.0

> Added options to customize texts WPAC.RefreshComments() and WPAC.LoadComments() now accept option object (and added option "showLoadingInfo" to suppress loading overlay) Updated jQuery blockUI to 2.61 Added jsuri 1.1.1 to avoid query strings with duplicated WPAC fallback parameters

#### 0.13.1

> Comment paging now updates browser URL Added localization for da-DK (thanks to Bjarne Maschoreck) Bugfix for themes where comment form is not nested in comment container Bugfix for clearing all settings (thanks to HarroH)

#### 0.13.0

> Ajaxified comment paging Improved debug support for cross-domain scripting problems

#### 0.12.1

> Hotfix for environments where PHP is not installed as an Apache module

#### 0.12.0

> Bug-fix: Options are no longer saved if validation fails Refactored and extended client-side JavaScript API Updated localization for de-DE Added option to load comments asynchronously with secondary AJAX request

#### 0.11.0

> Added localization for hu-HU (thanks to Patrik Bagi) Added option to customize the overlay's width Added option to customize the overlay's padding

#### 0.10.0

> Added localization for he-LI (thanks to Siman-Tov Yechiel ([www.wpstore.co.il](http://www.wpstore.co.il))) Added JavaScript callback ("Before submit comment") Updated jQuery blockUI to 2.57

#### 0.9.0

> Added JavaScript method wpac\_init() to enable manual client side initialization Optimized SQL queries (thanks to Geleosan) Added validation for "scrollSpeed" option Fixed debug alert message in IE 9 Added localization for sk-SK (thanks to Branco, Slovak translation ([WebHostingGeeks.com](http://webhostinggeeks.com/user-reviews/)))

#### 0.8.0

> Added option to customize the font size Added i18n support for admin frontend

#### 0.7.0

> Added JavaScript callback ("Before select elements")

#### 0.6.3

> Added localization for ar (thanks to sha3ira)

#### 0.6.2

> Fixed some PHP warnings (thanks to petersb) Fixed HTTPS check for ISAPI under IIS Added support for non-standard HTTP port Fixed handling of unexpected/unsupported server responses

#### 0.6.1

> Added localization for ru-RU and uk (thanks to Валерий Сиволап)

#### 0.6.0

> Added JavaScript callbacks ("Before update comments" and "After update comments")

#### 0.5.4

> jQuery 1.7+ compatibility: Use on() or delegate() if available instead of deprecated live() (thanks to tzdk)

#### 0.5.3

> Added localization for tr-TR (thanks to Erdinç Aladağ) Added localization for pt-BR (thanks to Leandro Martins Guimarães)

#### 0.5.2

> Added localization for fa-IR (thanks to rezach4)

#### 0.5.1

> Updated localization for zh-CN (thanks to Liberty Pi) Updated jQuery blockUI to 2.42 (thanks to Mexalim)

#### 0.5.0

> Success overlay now supports comments that are awaiting moderation Add "?" when commentUrl has no query string to reload page in case of partial page update fails More detailed debug messages and debug support for Internet Explorer 9 Added localization for ca (thanks to guzmanfg)

#### 0.4.1

> Added localization for nl-NL (thanks to Daniël Tulp)

#### 0.4.0

> Success and error overlays now show default cursor instead of loading cursor Fixed problems for translations containing double quotes Cancel AJAX request if cross-domain scripting is detected Added options to customize the look and feel Added localization for vi-VN (thanks to Nguyễn Hà Duy Phương) Added localization for es-ES (thanks to guzmanfg) Updated localization for de-DE

#### 0.3.4

> Added localization for pl-PL (thanks to Jacek Tomaszewski)

#### 0.3.3

> Bugfix for Internet Explorer

#### 0.3.2

> Added localization for fr-FR (thanks to saymonz)

#### 0.3.1

> Added localization for zh-CN (thanks to Liberty Pi)

#### 0.3.0

> Added i18n support Added localization for de-DE

#### 0.2.1

> Fallback mode reloads page with comment anchor Bug-fix for themes where comment form is nested in comments container (thanks to saymonz)

#### 0.2.0

> Added Option "Error Container Selector" to customize the error message extraction Added compatibility with comment spam protection plugins like "NoSpamNX" (thanks to Liberty Pi) Removed timeout for loading overlay (thanks to saymonz)

#### 0.1.2

> Fixed compatibility with setting pages of other plugins (thanks to saymonz) Reactivated warning and info notices on admin page "Plugins"

#### 0.1.1

> Fixed updating of browser address bar

#### 0.1.0

> Support for themes with threaded comments where form tag is not nested in comment container (Smooth) scrolling to new comment after new comment has been posted Update browser address bar to show comment URL after new comment has been posted Abort plugin initialization on pages and posts where comments are not enabled Info overlay when complete page reload is performed in fallback mode

#### 0.0.2

> Fixed error with warning and info notices on admin page "Plugins"

#### 0.0.1

> Initial release

### Upgrade Notice

#### 1.7.4

> Fixed HTML5 validation warning for script tag

#### 1.7.3

> Updated default value for "Comments container selector"

#### 1.7.2

> Added compatibility to older WordPress versions (< 5.2.0) and to WordPress 5.6

#### 1.7.1

> Added compatibility to latest WordPress versions >### 5.5.0 and updated external libraries

#### 1.7.0

> Preserve focus element when reloading comments and fixed deprecated error in PHP 7.4

#### 1.6.2

> Added compatibility to latest WordPress versions

#### 1.6.1

> Optimized JavaScript injection

#### 1.6.0

> Removed dependency to PHP session

#### 1.5.1

> "Undefined variable: wpac\_options"

#### 1.5.0

> Added JavaScript callback "OnAfterPostComment"

#### 1.4.1

> Prevent the comment form from being submitted multiple times in parallel, fixed PHP notice "Undefined index: pagenow"

#### 1.4.0

> Added (expert) option "Enable by query"

#### 1.3.0

> Added request parameters "WPACAll", "WPACSkip" and "WPACTake"

#### 1.2.0

> Added (expert) option "Disable cache", use GET request when updating comments

#### 1.1.1

> Fixed link to settings page in admin frontend

#### 1.1.0

> Fixed compatibility to WordPress 4.1

#### 1.0.0

> Added (expert) option "Base URL" to support reverse proxy configuration, fixed page title update for titles containing UTF-8 characters, typo fix

#### 0.25.0

> Loading comments now updates page title, OnBeforeSubmitComment callback is now called before submitUrl is extracted

#### 0.24.1

> Updated localization for zh-CN

#### 0.24.0

> Added parameter commentUrl to callbacks OnBeforeUpdateComments and OnAfterUpdateComments

#### 0.23.1

> Changed order of links in plugin overview, Make sure WPAC.\_Options is always initialized, Bugfix for comment paging links

#### 0.23.0

> Added (expert) option "Place scripts in footer", Bugfix for "Users must be registered and logged in to comment", Added option "Comment links selector", Fixed PHP Notice for PHP < 5.4.0

#### 0.22.0

> Minor optimizations, Added (expert) option "Optimize AJAX response", Bugfix for HTTPS

#### 0.21.0

> Added option "Disable scroll to anchor", Bugfixes for pages where comments are closed and/or async comment loading is enabled, Fixed compressed JavaScript file

#### 0.20.0

> Added support for multiple comment forms per page and support for none default WordPress comment pages

#### 0.19.0

> Added parameter newDom to callbacks OnBeforeUpdateComments and OnAfterUpdateComments, Fixed JavaScript errors

#### 0.18.1

> Fixed double slashes in JavaScript include

#### 0.18.0

> Optimized JavaScript includes, Added option to customize trigger for asynchronous comment loading

#### 0.17.3

> Fixed "Undefined index" PHP notice

#### 0.17.2

> Fixed compatibility to wpMandrill

#### 0.17.1

"OnAfterUpdateComments" callback is now called after form data has been reset

#### 0.17.0

Options to customize (default) WordPress messages, Disabled (auto) scrolling when comments are updated by "Auto update idle time", Fixed compatibility to jQuery "no conflict mode"

#### 0.16.1

Bugfix for cross-domain scripting detection

#### 0.16.0

Added option to automatically update comments if user is "idle", Updated jQuery blockUI to 2.64

#### 0.15.0

Added option to disable URL updating

#### 0.14.3

Fixed some PHP strict warnings

#### 0.14.2

Fixed compatibility to PHP < 5.4.0

#### 0.14.1

Fixed compatibility to jQuery "no conflict mode"

#### 0.14.0

Added options to customize texts, Updated jQuery blockUI to 2.61, Improved client-side API, Added jsuri 1.1.1 to optimize query string sin fallback URLs

#### 0.13.1

Bug-fixes, improved URL updating, added localization for da-DK

#### 0.13.0

Ajaxified comment paging, added localization for da-DK

#### 0.12.1

Hotfix for environments where PHP is not installed as an Apache module

#### 0.12.0

Bug-fixes, refactored and extended client-side JavaScript API

#### 0.11.0

Added localization for hu-HU, added more options to customize the overlays

#### 0.10.0

Added localization for he-LI, added JavaScript callback ("Before submit comment"), updated jQuery blockUI to 2.57

#### 0.9.0

Added JavaScript method wpac\_init(), optimzed SQL queries, fixed debug alert in IE 9, added localization for sk-SK

#### 0.8.0

Added option to customize the font size, i18n support for admin frontend

#### 0.7.0

Added JavaScript callback ("Before select elements")

#### 0.6.3

Added localization for ar

#### 0.6.2

Some bug-fixes

#### 0.6.1

Added localization for ru-RU and uk

#### 0.6.0

Added JavaScript callbacks

#### 0.5.4

jQuery 1.7+ compatibility

#### 0.5.3

Added localization for tr-TR and pt-BR

#### 0.5.2

Added localization for fa-IR

#### 0.5.1

Updated localization for zh-CN, Updated jQuery blockUI to 2.42

#### 0.5.0

Bug-fix, support for comments that are awaiting moderation, more detailed debug messages & debug support for IE 9, added localization for ca

#### 0.4.1

Added localization for nl-NL

#### 0.4.0

Bug-fix, added options to customize the look and feel, added localizations (vi-VN and en-ES), updated localization for de-DE

#### 0.3.4

Added localization for pl-PL

#### 0.3.3

Bug-fix

#### 0.3.2

Added localization for fr-FR

#### 0.3.1

Added localization for zh-CN

#### 0.3.0

Added i18n support

#### 0.2.1

Bug-fix & minor improvements

#### 0.2.0

Added compatibility with comment spam protection plugins

#### 0.1.2

Bug-fix

#### 0.1.1

Bug-fix

#### 0.1.0

Better theme support (for threaded comments) and new features

#### 0.0.2

Bug-fix
