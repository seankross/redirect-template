# Redirection Template

This repository serves as a public template to set up a simple HTML redirection. A template is a pre-defined repository that can be used as a starting point for creating new projects.

To use this template, simply click on the "Use this template" button on the top of this repository page. This will allow you to create a new repository with the same files and structure.

The particularity of this template is that it makes a redirection to another page that you can specify. This redirection is usually done by other means (for instance as an entry in the `.htaccess` file, in the case of an Apache server), but it can be useful to use this simple way in some situations.

## Customizing the Template

To customize this template for your own use, replace the occurrances of the expression `https://seankross.com/[REPO NAME]/[FILE NAME]` with the url you want to redirect to.

```html
<html>
<head>
  <meta http-equiv="refresh" content="0; url=https://seankross.com/[REPO NAME]/[FILE NAME]" />
</head>
<body>
  <p><a href="https://seankross.com/[REPO NAME]/[FILE NAME]">Click here</a> if you're not redirected.</p>
</body>
</html>
```

## About the Redirection

The redirection in this template is accomplished using an HTML `meta` tag in the `head` section of the `index.html` file. This tag causes the browser to refresh the page, but instead of reloading the same page, it redirects to a new URL specified in the `content` attribute.

The redirection is instantaneous due to the `0` before the semicolon in the `content` attribute. The URL to which it redirects is specified after the semicolon.

There's also a fallback link in the `body` of the HTML. This serves as a manual redirection option if for some reason the automatic redirect doesn't work.

## When to Use This Redirection

This type of redirection is client-side, meaning it relies on the user's browser to carry out the redirect. While this method works, it has some downsides. These include potential negative SEO implications and the reliance on the user's browser supporting this functionality.

However, this method can be particularly useful in several situations such as website or page migrations, temporary redirects, or when server-side scripting isn't available. It can be an easy way to redirect users to an external site or to handle redirects for short-lived websites or events.
