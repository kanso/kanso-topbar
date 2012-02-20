## Kanso Top-Bar

This package provides resources for the standard navigation and session
management bar used in manage core Kanso apps. Using a standard topbar
means your users will be instantly familiar with how to login and
navigate back to their dashboard.


### Resources

#### Attachments

* kanso-topbar/topbar.css
* kanso-topbar/dashboard\_icon.png

#### Modules

* kanso-topbar


### Usage

Add 'kanso-topbar' to your `kanso.json` file.

```javascript
{
    ...
    "dependencies": {
        "kanso-topbar": null
    }
}
```

Install the new package with `kanso install`. Then, if you are using rewrites, make sure you have a rewrite set up for the attachments provided by this module:

```javascript
// rewrites.js
modules.exports = {
    ...
    {from: '/kanso-topbar/*', to: 'kanso-topbar/*'}
};
```

Add the kanso-topbar stylesheet to your HTML:

```html
<link rel="stylesheet" type="text/css" href="kanso-topbar/topbar.css" />
```

Finally, make sure you call the kanso-topbar init function using jQuery document ready, or by adding a script tag at the bottom of the page. This should go after you've included `modules.js`:

```javascript
require('kanso-topbar').init();
```

If you're using the Duality framework, you may wish to add this to an
`init` event handler instead.
