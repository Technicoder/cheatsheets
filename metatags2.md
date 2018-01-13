# Metatags

## Table of Contents

- [Example](#template)
- [Recommended Minimum](#recommended-minimum)
- [Elements](#elements)
- [Meta](#meta)
- [Link](#link)
- [Favicons](#favicons)
- [Social](#social)
  - [Facebook Open Graph](#facebook-open-graph)
  - [Twitter Card](#twitter-card)
  - [Twitter Privacy](#twitter-privacy)
  - [Google+ / Schema.org](#google--schemaorg)
  - [Facebook Instant Articles](#facebook-instant-articles)
  - [OEmbed](#oembed)
- [Browsers / Platforms](#browsers--platforms)
  - [Apple iOS](#apple-ios)
  - [Apple Safari](#apple-safari)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Google Chrome Mobile (Android Only)](#google-chrome-mobile-android-only)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
- [Browsers (Chinese)](#browsers-chinese)
  - [360 Browser](#360-browser)
  - [QQ Mobile Browser](#qq-mobile-browser)
  - [UC Mobile Browser](#uc-mobile-browser)
- [App Links](#app-links)
- [Other Resources](#resources)

## Template

```html
<!-- Recommend minimum -->
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<meta name="description" content="A description of the page">
<title>Page Title</title>
<base href="http://example.com/page.html">

<!-- Open graph -->
<meta property="og:title" content="Content Title">
<meta property="og:description" content="Description Here">
<meta property="og:url" content="http://example.com/page.html">
<meta property="og:site_name" content="Site Name">
<meta property="og:image" content="http://example.com/image.jpg">

<!-- Favicons (realfavicongenerator.net) in /images/
<meta name="msapplication-config" content="/images/browserconfig.xml">
<meta name="theme-color" content="#ffffff">
<link rel="apple-touch-icon" sizes="180x180" href="/images/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/images/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/images/favicon-16x16.png">
<link rel="manifest" href="/images/manifest.json">
<link rel="mask-icon" href="/images/safari-pinned-tab.svg" color="#5bbad5">
<link rel="shortcut icon" href="/images/favicon.ico">

<!-- Stylesheets -->
<link rel="stylesheet" href="http://example.com/styles.css">
<style>...</style>

<!-- Scripts -->
<script src="script.js"></script>
<script>...</noscript>
```

## Recommended Minimum

```html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!--
  The above 3 meta tags *must* come first in the <head>
  to consistently ensure proper document rendering.
  Any other head element should come *after* these tags.
 -->
<title>Page Title</title>
```

**[⬆ back to top](#table-of-contents)**

## Elements

Valid `<head>` elements include `meta`, `title`, `base`, `link`, `style`, `script` and `noscript`.


``` html
<!-- In the head: -->

<!-- Meta -->
<meta charset="utf-8">

<!-- Title -->
<title>Page Title</title>

<!-- Base -->
<base href="http://example.com/page.html">

<!-- Link -->
<link rel="stylesheet" href="styles.css">

<!-- At the bottom of the body: -->

<!-- Script and Noscript -->
<script src="script.js"></script>
<script>
  // function(s) go here
</script>
<noscript>
  <!-- No JS alternative -->
</noscript>
```

**[⬆ back to top](#table-of-contents)**

## Meta

``` html
<!-- Recommended minimum -->
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

<!-- Control over where resources are loaded from, applied to resources that are declared after it. -->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- Name of web application (only if used as an app) -->
<meta name="application-name" content="Application Name">

<!-- Short description of the document (150 characters) -->
<meta name="description" content="A description of the page">

<!-- Search engine crawling and indexing -->
<meta name="robots" content="index,follow"><!-- All Search Engines -->
<meta name="googlebot" content="index,follow"><!-- Google Specific -->

<!-- Google sitelinks search box -->
<meta name="google" content="nositelinkssearchbox">

<!-- Google translation -->
<meta name="google" content="notranslate">

<!-- Ownership -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
<meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
<meta name="alexaVerifyID" content="verification_token"><!-- Alexa Console -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Pinterest Console-->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- Software used to build the document -->
<meta name="generator" content="program">

<!-- Subject -->
<meta name="subject" content="Your document's subject">

<!-- Age rating -->
<meta name="rating" content="General">

<!-- Referrer informations -->
<meta name="referrer" content="no-referrer">

<!-- Phone numbers -->
<meta name="format-detection" content="telephone=no">

<!-- DNS prefetching -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Cookies -->
<meta http-equiv="set-cookie" content="name=value; expires=date; path=url">

<!-- Frame -->
<meta http-equiv="Window-Target" content="_value">

<!-- Geo tags -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- Country code (ISO 3166-1): mandatory, state code (ISO 3166-2): optional; eg. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- eg. content="New York City" -->
```

- 📖 [Meta tags that Google understands](https://support.google.com/webmasters/answer/79812?hl=en)
- 📖 [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)

**[⬆ back to top](#table-of-contents)**

## Link

``` html
<!-- External stylesheet -->
<link rel="stylesheet" href="http://example.com/styles.css">

<!-- Duplicate issues -->
<link rel="canonical" href="http://example.com/2010/06/9-things-to-do-before-entering-social-media.html">

<!-- Shortlink (deprecated) -->
<link rel="shortlink" href="http://example.com/?p=42">

<!-- AMP HTML version -->
<link rel="amphtml" href="http://example.com/path/to/amp-version.html">

<!-- JSON for "installation" credentials for the web applications -->
<link rel="manifest" href="manifest.json">

<!-- Author -->
<link rel="author" href="humans.txt">

<!-- Author/people -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Copyright -->
<link rel="license" href="copyright.html">

<!-- Other languages -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Archive -->
<link rel="archives" href="http://example.com/archives/">

<!-- Top level resources -->
<link rel="index" href="http://example.com/">

<!-- Self reference -->
<link rel="self" type="application/atom+xml" href="http://example.com/atomFeed.php?page=3">

<!-- Series of documents -->
<link rel="first" href="http://example.com/atomFeed.php">
<link rel="next" href="http://example.com/atomFeed.php?page=4">
<link rel="prev" href="http://example.com/atomFeed.php?page=2">
<link rel="last" href="http://example.com/atomFeed.php?page=147">

<!-- Third party service -->
<link rel="EditURI" href="http://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- WordPress auto-comment -->
<link rel="pingback" href="http://example.com/xmlrpc.php">

<!-- URL notification -->
<link rel="webmention" href="http://example.com/webmention">

<!-- Micropub client -->
<link rel="micropub" href="http://example.com/micropub">

<!-- External HTML file loading -->
<link rel="import" href="/path/to/component.html">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="http://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing (more info at https://css-tricks.com/prefetching-preloading-prebrowsing/) -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="http://example.com/">
<link rel="preload" href="image.png" as="image">
```

**[⬆ back to top](#table-of-contents)**

## Favicons

``` html
<link rel="icon" type="image/png" sizes="16x16" href="/path/to/favicon-16x16.png">
<link rel="icon" type="image/png" sizes="32x32" href="/path/to/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="96x96" href="/path/to/favicon-96x96.png">
```

- 📖 [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)

**[⬆ back to top](#table-of-contents)**

## Social

### Facebook Open Graph

``` html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="http://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="http://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

- 📖 [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- 📖 [Open Graph protocol](http://ogp.me/)
- 🛠 Test your page with the [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

### Twitter Card

``` html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="http://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="http://example.com/image.jpg">
```

- 📖 [Getting started with cards — Twitter Developers](https://dev.twitter.com/cards/getting-started)
- 🛠 Test your page with the [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### Twitter Privacy
If you embed tweets in your website, Twitter can use information from your site to tailor content and suggestions to Twitter users. [More about Twitter privacy options](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
``` html
<!-- disallow Twitter from using your site's info for personalization purposes -->
<meta name="twitter:dnt" content="on">
```

### Google+ / Schema.org

``` html
<link href="https://plus.google.com/+YourPage" rel="publisher">
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="http://example.com/image.jpg">
```

### Pinterest

Pinterest lets you prevent people from saving things from your website, according [to their help center](https://help.pinterest.com/en/articles/prevent-people-saving-things-pinterest-your-site). The `description` is optional.

``` html
<meta name="pinterest" content="nopin" description="Sorry, you can't save from my website!">
```

### Facebook Instant Articles

``` html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- The URL of the web version of your article -->
<link rel="canonical" href="http://example.com/article.html">

<!-- The style to be used for this article -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Creating Articles - Instant Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Code Samples - Instant Articles](https://developers.facebook.com/docs/instant-articles/reference)

### OEmbed

``` html
<link rel="alternate" type="application/json+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- 📖 [oEmbed format](http://oembed.com/)

**[⬆ back to top](#table-of-contents)**

## Browsers / Platforms

### Apple iOS

``` html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Disable automatic detection and formatting of possible phone numbers -->
<meta name="format-detection" content="telephone=no">

<!-- Add to Home Screen -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- Touch Icons -->
<!-- In most cases, one 180×180px touch icon in the head is enough -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Startup Image ( Deprecated ) -->
<link rel="apple-touch-startup-image" href="/path/to/startup.png">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Apple Meta Tags](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

### Apple Safari

```html
<!-- Pinned Site -->
<link rel="mask-icon" href="/path/to/icon.svg" color="red">
```

### Google Android

``` html
<meta name="theme-color" content="#E64545">

<!-- Add to home screen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

``` html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Disable translation prompt -->
<meta name="google" content="notranslate">
```

### Google Chrome Mobile (Android Only)

Since Chrome 31, you can set up your web app to "app mode" like Safari.

``` html
<!-- Link to a manifest and define the manifest metadata -->
<!-- The example of manifest.json could be found in the link below -->
<link rel="manifest" href="manifest.json">

<!-- Define your web page as a web app -->
<meta name="mobile-web-app-capable" content="yes">

<!-- Homescreen Icon -->
<link rel="icon" sizes="192x192" href="/path/to/highres-icon.png">
```

- 📖 [Add to Homescreen - Google Chrome](https://developer.chrome.com/multidevice/android/installtohomescreen)

### Microsoft Internet Explorer

``` html
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- IE10: Disable link highlighting upon tap (https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/) -->
<meta name="msapplication-tap-highlight" content="no">

<!-- Pinned sites (https://msdn.microsoft.com/en-us/library/dn255024(v=vs.85).aspx) -->
<meta name="application-name" content="Sample Title">
<meta name="msapplication-tooltip" content="A description of what this site does.">
<meta name="msapplication-starturl" content="http://example.com/index.html?pinned=true">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-window" content="width=800;height=600">
<meta name="msapplication-task" content="name=Task 1;action-uri=http://host/Page1.html;icon-uri=http://host/icon1.ico">
<meta name="msapplication-task" content="name=Task 2;action-uri=http://microsoft.com/Page2.html;icon-uri=http://host/icon2.ico">
<meta name="msapplication-badge" value="frequency=NUMBER_IN_MINUTES;polling-uri=http://example.com/path/to/file.xml">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="/path/to/tileimage.jpg">

<meta name="msapplication-config" content="http://example.com/browserconfig.xml">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://example.com/livetile;polling-uri2=http://example.com/livetile2">
<meta name="msapplication-task-separator" content="1">
```

**[⬆ back to top](#table-of-contents)**

## App Links

``` html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">

<!-- Web fall back -->
<meta property="al:web:url" content="http://applinks.org/documentation">
```

- 📖 [App Links](http://applinks.org/documentation/)

**[⬆ back to top](#table-of-contents)**

## Browsers (Chinese)

### 360 Browser

``` html
<!-- Select rendering engine order -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

``` html
<!-- Locks the screen into the specified orientation -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- Display this document in fullscreen -->
<meta name="x5-fullscreen" content="true">

<!-- Document will be displayed in "application mode" (fullscreen, etc.) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

``` html
<!-- Locks the screen into the specified orientation -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Display this document in fullscreen -->
<meta name="full-screen" content="yes">

<!-- UC browser will display images even if in "text mode" -->
<meta name="imagemode" content="force">

<!-- Document will be displayed in "application mode"(fullscreen, forbidding gesture, etc.) -->
<meta name="browsermode" content="application">

<!-- Disabled the UC browser's "night mode" for this document -->
<meta name="nightmode" content="disable">

<!-- Simplify the document to reduce data transfer -->
<meta name="layoutmode" content="fitscreen">

<!-- Disable the UC browser's feature of "scaling font up when there are many words in this document" -->
<meta name="wap-font-scale" content="no">
```

- 📖 [UC Browser Docs](http://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ back to top](#table-of-contents)**

## Notes

### Related Resources

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js

### Author

**[Josh Buchea](https://joshbuchea.com/)**, full version on [Github](https://github.com/joshbuchea/HEAD/blob/master/README.md#meta).

**[⬆ back to top](#table-of-contents)**
