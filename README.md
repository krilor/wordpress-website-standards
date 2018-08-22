
WordPress Website Standards
===========================

This document tries to outline an objective standard for what is required to be a great WordPress website. Anyone can create a WordPress website, but it’s not always clear what is needed for it to be a technically sound site. This list is part standard, part checklist and most of all a valuable reference for vendors and clients alike in their search for building or buying a great WordPress site.

<!-- MarkdownTOC autolink="true" bullets="*" indent="    " -->

* [About](#about)
    * [Version](#version)
    * [Purpose](#purpose)
    * [Audience](#audience)
    * [Considerations](#considerations)
    * [Required vs recommended vs optional](#required-vs-recommended-vs-optional)
    * [Open standard - let us discuss!](#open-standard---let-us-discuss)
    * [WordPress.org and WordPress.com](#wordpressorg-and-wordpresscom)
    * [Tags](#tags)
* [A Great WordPress Website](#a-great-wordpress-website)
    * [Code](#code)
        * [Child theme](#child-theme)
        * [Theme and Plugin Territory](#theme-and-plugin-territory)
        * [Valid HTML5 and CSS](#valid-html5-and-css)
        * [Print Stylesheet](#print-stylesheet)
        * [Responsiveness](#responsiveness)
        * [Accessibility](#accessibility)
        * [WordPress Coding Standards](#wordpress-coding-standards)
        * [Unused Themes and Plugins](#unused-themes-and-plugins)
        * [Google Search Console](#google-search-console)
        * [JavaScript Libraries](#javascript-libraries)
    * [Hosting](#hosting)
        * [PHP version](#php-version)
        * [Database version](#database-version)
        * [Manual backup](#manual-backup)
        * [Scheduled backups](#scheduled-backups)
        * [Redirecting www](#redirecting-www)
        * [Staging site](#staging-site)
        * [Email delivery](#email-delivery)
        * [Favicon](#favicon)
        * [Analytics](#analytics)
        * [Uptime monitoring](#uptime-monitoring)
    * [Search Engine Optimization](#search-engine-optimization)
        * [Sitemap](#sitemap)
        * [Breadcrumbs](#breadcrumbs)
    * [Security](#security)
        * [SSL Encryption](#ssl-encryption)
        * [Secure passwords](#secure-passwords)
        * [Automatic Security Updates](#automatic-security-updates)
        * [Admin username](#admin-username)
        * [Login attempt limit](#login-attempt-limit)
    * [WordPress functionality](#wordpress-functionality)
        * [Media image sizes](#media-image-sizes)
        * [Editor styles](#editor-styles)
        * [Page templates](#page-templates)
        * [Disable Comments](#disable-comments)
        * [Anti Spam for comments](#anti-spam-for-comments)
        * [404 page](#404-page)
        * [Sticky Posts](#sticky-posts)
        * [Privacy Policy](#privacy-policy)
    * [Page speed and optimization](#page-speed-and-optimization)
        * [Load time](#load-time)
        * [Response Time](#response-time)
        * [Time to first byte](#time-to-first-byte)
        * [Request count](#request-count)
        * [Page weight](#page-weight)
        * [Image compression](#image-compression)
        * [Cache](#cache)
        * [Content Delivery Network](#content-delivery-network)
        * [Compression](#compression)
        * [Render-blocking JavaScript and CSS](#render-blocking-javascript-and-css)
        * [Minified resources](#minified-resources)
        * [Browser Caching](#browser-caching)
        * [Landing page redirects](#landing-page-redirects)
        * [Prioritize Visible Content](#prioritize-visible-content)
* [Removed Items](#removed-items)
    * [Outdated](#outdated)
        * [Database Table Prefix](#database-table-prefix)
        * [Hide WordPress Version](#hide-wordpress-version)

<!-- /MarkdownTOC -->

About
=====

Version
-------

The master branch of this repo will contain the most up-to-date version of the standard. It might be between versions.
If you need to reference a specific version of this document, then check out the [releases](https://github.com/krilor/wordpress-website-standards/releases).
Feel free to browse trough the changes in the [commit log](https://github.com/krilor/wordpress-website-standards/commits/master).

Purpose
-------

The purpose of the document is to help get rid of ambiguous phrases like “best practice”, and rather set a benchmark for what practices **must** be used to qualify to be a great WordPress website.
I hope that it will help make agreements and communication between vendors and clients simpler. By having an objective standard, it will be easier for vendors to show clients that they are doing quality work, while clients can be confident in what they receive.

Audience
--------

This document is intended for persons involved in setting up or auditing WordPress websites.

Considerations
--------------

Building web pages is a craft: It requires hard work that involves many decisions and considerations. This standard aimes to be objective and presents itself as a list of rules stated as facts. While I believe that all the items of this list are warranted and based on reliable sources and commonly agreed upon practices, there is still room for interpretation and/or variations on the topics presented. Be aware that there might be sites or projects where some or many of the requirements are not justified or needed.

Some of the items on this list are very specific about the practices and tools that must be used to solve certain problems. For example, modifications to premade themes must always be done in a child theme. This is a commonly acknowledged practice, and therefore belongs in this list. This document intentionally does not cover subjects or areas where there are no commonly accepted practices or yardsticks to measure by. For example regarding third party code/functionality like:

* use of premade themes
* limitation of number of plugins on a site
* use of page builders

It is very hard to state commonly accepted guidelines for these kinds of topics, but there are some ground rules that should be applied. Be mindful about pros and cons of different solutions while building a site. Use plugins wisely and only when actually needed. Be aware that they can hurt the performance or user experience on the site. Always try, to the best of your abilities, to vet any third party code before adding it. Evaluate aspects such as update frequency and code quality.

Use this list as a reference, but be critical to it's contents. If you disagree or have suggestions to changes, don't hesitate to open an issue.

Required vs recommended vs optional
-------------------------------

This document distinguishes between what is required, recommended and optional for WordPress site deliveries. This is done through wording in each item.

> The key words "must", "must not", "required", "shall", "shall not", "should", "should not", "recommended",  "may", and "optional" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).

In broad strokes, requirements and recommendations divides a basic standard from a gold standard. The requirements are what needs to be met to deliver a good site, and the recommendations will push that even further.

Open standard - let us discuss!
-------------------------------

Please help me hone this standard so that it can serve as a reference for everyone that is using WordPress to power their websites. Open a new issue or submit a pull request to get the discussion going. If you want to help out, check the [contributing information](CONTRIBUTING.md).

WordPress.org and WordPress.com
-------------------------------

This document, and its author, is not affiliated with WordPress, other than being an enthusiastic user.

[WordPress.org Plugin Repository Guidelines](https://developer.wordpress.org/plugins/wordpress-org/detailed-plugin-guidelines/) and [WordPress.org Theme Repository Guidelines](https://make.wordpress.org/themes/handbook/review/required/) are not covered by this document, but as a keen reader you will find overlaps on certain points. Consider using the [Theme Checker](https://make.wordpress.org/themes/handbook/review/required/theme-check-plugin/) plugin to identify possible errors in your theme.

Tags
----

Below each requirement there can be one or multiple tags. These tags are used to give an indication of where the requirement originates or which group it belongs too. The following tags are used:

<dl>
  <dt>Insdustry Benchmark</dt>
  <dd>The industry page speed benchmark as presented by <a href="https://www.thinkwithgoogle.com/marketing-resources/data-measurement/mobile-page-speed-new-industry-benchmarks/">Think With Google</a>.</dd>
  <dt>PageSpeed</dt>
  <dd>The requirements originates from or is validated by Googles <a href="https://developers.google.com/speed/pagespeed/insights/">PageSpeed InSights tool</a> for checking website performance.</dd>
</dl>

A Great WordPress Website
=========================

The rest of this document outlines what it takes to be a Great WordPress Website

Code
----

### Child theme

> All modifications to premade themes **must** be placed in a child theme.

Any direct modifications to a theme that can be updated from the WordPress theme repository or any other source will probably be overwritten when updating the theme.

### Theme and Plugin Territory

> Custom functionality that is not related to design **should** be placed in a plugin, not in the a theme.

The purpose of this is mainly to keep the ability to switch themes without breaking the site. See WordPress Theme handbook for [Plugin Territory examples](https://make.wordpress.org/themes/handbook/review/required/explanations-and-examples/%23plugin-territory).

### Valid HTML5 and CSS

> Pages **must** be valid HTML5 with valid CSS.

Refer to the [Theme Handbook](https://developer.wordpress.org/themes/advanced-topics/validating-your-theme/) page on the topic.

### Print Stylesheet

> The site **should** have proper print styles.

There are no established best practices when it comes to print stylesheets, but the general guideline is to make make content useful and save ink. Consider what content is the most likely content to be printed, for example purchase receipts and other reference data.
Modern browsers will let you emulate print, for example [Chrome](https://developers.google.com/web/tools/chrome-devtools/css/reference#print-mode) or [Firefox](https://stackoverflow.com/a/28873496).
Consider the following practices

* Hide unwanted content such as headers and footers
* Don't print background images or colors
* Controlling page breaks
* [Show URLs after links](https://davidwalsh.name/optimize-your-links-for-print-using-css-show-url)
* Show title of _abbr_ and _acronym_ tags
* Swap to a serif font
* [Adding QR code for easy reference](https://www.smashingmagazine.com/2013/03/tips-and-tricks-for-print-style-sheets/#print-qr-codes-for-easy-url-references)

### Responsiveness

> All pages on the site **must** be responsive to work on devices off all sizes.

Page responsiveness has to be tested on actual devices by actual people, but **should** also be tested with automatic tools such as [Googles Mobile Friendly](https://search.google.com/test/mobile-friendly) and [Ready.mobi](https://ready.mobi)

### Accessibility

> The site **must** be according to [WCAG 2.0 AA](https://www.w3.org/TR/WCAG20/) guidelines.

This is the same guidelines that [WordPress core uses](https://make.wordpress.org/accessibility/handbook/test-for-web-accessibility/#what-are-the-guidelines). Check out the [WordPress Accessibility Handbook](https://make.wordpress.org/accessibility/handbook/) for tips on how to make the site accessible.

### WordPress Coding Standards

> All custom code **should** adhere to [WordPress Coding Standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/).

While following the WordPress Coding Standards is something that is recommended, it is not something that defines what a good WordPress site/delivery is. However, if the coding standards are followed for all custom code, it will make for an easier transition if a new vendor is doing work on the site in the future.

### Unused Themes and Plugins

> Unused plugins and themes **must** not be on the site.

### Google Search Console

> If registered with Google Search Console, the site **must** have no issues.

It is recommended to register the site with Google Search Console.

### JavaScript Libraries

> If using JavaScript libraries that are included in WordPress Core, use the one that is provided by WordPress.

[Many libraries](https://developer.wordpress.org/reference/functions/wp_enqueue_script/) are registered by WordPress, including Underscore and jQuery.

Hosting
-------

### PHP version

> PHP version **must** be according to [WordPress recommendations](https://wordpress.org/about/requirements/), currently PHP 7.2 or greater.

### Database version

> Database version **must** be according to [WordPress recommendations](https://wordpress.org/about/requirements/), currently MySQL version 5.6 or greater OR MariaDB version 10.0 or greater.

### Manual backup

> Site admin **must** be able to do manual backups at any time and store that backup locally or off-site.

### Scheduled backups

> Scheduled backup to off-site location with defined interval and retention period **should** be enabled.

### Redirecting www

> The site **must** redirect from www address to non-www address, or vice versa.

If a user tries to access the site on the non-canonical of the two addresses, then the site **must** still be delivered.

### Staging site

> The vendor **should** provide the client with a staging site where changes can be made, tested and then moved to the production site.

### Email delivery

> Appropriate measures **must** be taken to ensure that emails from password reset, forms etc are not flagged as spam.

There are multiple ways of doing this, ranging from setting up SPF records, SMTP solutions, using ESPs and so on. Check this guide from [Ninja forms](https://ninjaforms.com/definitive-guide-wordpress-email/).

### Favicon

> The site **must** have a defined favicon for all platforms and devices.

Favicons are not what they used to be - now we need many different types of sizes. Consider using a plugin like [Favicon](https://wordpress.org/plugins/favicon-by-realfavicongenerator/) to make your life easier.

### Analytics

> Site analytics and tracking **should** be configured.

### Uptime monitoring

> The site **should** have uptime monitoring with automatic notifications.

Search Engine Optimization
--------------------------

### Sitemap

> The site **must** have an XML sitemap.

### Breadcrumbs

> The site **should** have breadcrumbs.

Refer to [this article by Yoast](https://yoast.com/breadcrumbs-seo/) for a detailed view on why it is important.

Security
--------

Consider using the [WordPress Security Checklist](https://wpsecuritychecklist.org).

### SSL Encryption

> The site **must** have forced SSL encryption (HTTPS).

### Secure passwords

> The site **should** enforce strong passwords for all users with edit or publish capabilities.

While this can be handled on a policy level, it still makes sense to enforce it. This can be done via the plugin [Force Strong Passwords](https://wordpress.org/plugins/force-strong-passwords/). Users **should** also periodically set a new password.

### Automatic Security Updates

> Automatic Security Updates **must** be enabled.

### Admin username

> There **must** be no user with the user name admin.

### Login attempt limit

> The site **must** have a limit for failed login attempts.

Multiple plugins provide this functionality, including [Wordfence](https://wordpress.org/plugins/wordfence/).

WordPress functionality
-----------------------

### Media image sizes

> Media Image Sizes **must** not be configured unless the sizes are actually used by the theme.

Having WordPress produce images of the right size is nice, but if there is no use for it or, it shouldn’t be configured. It just causes bloat on the server. Be careful to define new image sizes, and consider [disabling](https://premium.wpmudev.org/blog/delete-unused-image-files-wordpress/) some of the default ones.

### Editor styles

> Editor styles **should** be added so that editing experience equals front-end.

### Page templates

> The site **should** include page templates that are ready for layout designers like Gutenberg or page builders.

This includes page templates that are wide (full content area/sidebars) and full-width (whole page).

### Disable Comments

> Commenting functionality **must** be disabled if not in use.

It’s rather easy to “hide” comments functionality on the front end by simply not including the [comment templates and code](https://developer.wordpress.org/themes/template-files-section/partial-and-miscellaneous-template-files/comments/) in a custom theme. However, if comments are not in use, they **must** also be disabled on the back end. Consider using either [Disable Comment](https://wordpress.org/plugins/disable-comments/) or [No Page Comment](https://wordpress.org/plugins/no-page-comment/) plugins.

### Anti Spam for comments

> If comments are used, then there **must** be anti-spam functionality enabled.

### 404 page

> A proper 404 page template **must** be in place and http status code 404 returned.

Also, consider tracking which urls are most frequently returning 404, using a plugin like [Redirection](https://wordpress.org/plugins/redirection/).

### Sticky Posts

> The theme **must** honor sticky posts and handle them consistently.

### Privacy Policy

> A privacy policy page **must** be created, added to the privacy policy setting and displayed on all pages on the website.

Page speed and optimization
---------------------------

The most viable way to test for an optimized web page is to use automatic testers like
[Google PageSpeed InSights](https://developers.google.com/speed/pagespeed/insights/),
[Google TestMySite](https://testmysite.withgoogle.com/),
[GTmetrix](https://gtmetrix.com)
or [Pingdom Website speed test](https://tools.pingdom.com/).
Some of the requirements below are based on the [industry benchmarks](https://www.thinkwithgoogle.com/marketing-resources/data-measurement/mobile-page-speed-new-industry-benchmarks/) from Think With Google.

### Load time

> All pages on the website **must** load in less than 3 seconds on all devices on average.

`Industry Benchmark`

### Response Time

> [Server response time](https://developers.google.com/speed/docs/insights/Server) **must** be under 200 ms.

`PageSpeed`

### Time to first byte

> Time to first byte **must** be less than 1.3 seconds.

`Industry Benchmark`

### Request count

> Number of requests **must** be less than 50.

`Industry Benchmark`

### Page weight

> The total size of a webpage, **should** be less than 500 KB.

`Industry Benchmark`

### Image compression

> Proper [image compression](https://developers.google.com/speed/docs/insights/OptimizeImages) functionality **must** be configured on the site.

`PageSpeed`

Consider removing the default JPEG image compression via a [custom](https://premium.wpmudev.org/blog/fix-jpeg-compression/) or [installable](https://wordpress.org/plugins/disable-jpeg-compression/) plugin, and then add a third-party lossless compression plugin like:

* [reSmush.it](https://wordpress.org/plugins/resmushit-image-optimizer/)
* [WP Smushit](https://wordpress.org/plugins/wp-smushit/)
* [EWW Image Optimizer](https://wordpress.org/plugins/ewww-image-optimizer/)
* [ShortPixel Image Optimizer](https://wordpress.org/plugins/shortpixel-image-optimiser/)

### Cache

> Web site cache **should** be enabled.

The ideal solution is to do this on the server level, but using a cache plugin can give a lot of gain for very little effort.

### Content Delivery Network

> The static content of the site **should** be delivered by a CDN.

### Compression

> [Gzip compression](https://developers.google.com/speed/docs/insights/EnableCompression) **must** be enabled.

`PageSpeed`

### Render-blocking JavaScript and CSS

> JavaScripts that are not critical to initial render **should** be made [asynchronous or deferred](https://developers.google.com/speed/docs/insights/BlockingJS) until after the first render. CSS delivery **should** be [optimized](https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery).

`PageSpeed`

### Minified resources

> All HTML, JavaScript and CSS **must** be [minified](https://developers.google.com/speed/docs/insights/MinifyResources).

`PageSpeed`

### Browser Caching

> Each resource served **must** specify an [explicit caching policy](https://developers.google.com/speed/docs/insights/LeverageBrowserCaching).

`PageSpeed`

### Landing page redirects

> There **must** be no [landing page redirects](https://developers.google.com/speed/docs/insights/AvoidRedirects).

`PageSpeed`

### Prioritize Visible Content

> The size of the data that is needed to render the above-the-fold content of the page **should** be [limited](https://developers.google.com/speed/docs/insights/PrioritizeVisibleContent).

`PageSpeed`

Removed Items
=============

The following items has been removed from the standard, but is kept as a reference.

Outdated
--------

### Database Table Prefix

> Database tables **must** use a different prefix than _wp__.

`Outdated`

There is no reason to hide change the database prefix. [Hackers are more clever than that](https://www.wordfence.com/blog/2016/12/wordpress-table-prefix/).

### Hide WordPress Version

> The meta generator tag which includes WordPress version **must** be hidden.

`Outdated`

This is not needed because you should always have an updated version of WordPress. Also, [hiding the version doesn't really help](https://www.wpwhitesecurity.com/wordpress-security/hide-wordpress-version-does-it-matter/).