# `<myuw-app-bar>`

A material top app bar designed for use with other MyUW web components

## Development and contribution

To run the demo app locally and test the component, run the following commands:

```bash
$ npm install
$ npm start
```

## Getting Started

Add the following import to your page's `<head>`:

```html
<link rel="import" href="https://unpkg.com/@myuw-web-components/myuw-app-bar@1.0.0/myuw-app-bar.html">
```


Use the component's HTML tag wherever you want:

```HTML
<myuw-app-bar
    theme-name="MyUW"
    theme-url=""
    app-name=""
    app-url=""
>
</myuw-app-bar>
```

### Configurable properties via attributes

- **themeName (theme-name):** Sets the theme/portal name (defaults to "MyUW")
- **themeUrl (theme-url):** Sets then URL to go to when user clicks the theme name
- **appName (app-name):** Sets the app name (e.g. "Bucky Backup")
- **appUrl (app-url):** Sets then URL to go to when user clicks the app name

### Styling the app bar

MyUW app bar exposes custom CSS properties so users can change some of its styles.

- **--myuw-app-bar-bg:** Cahnges the background color of the app bar (default is UW-Madison red)
- **--myuw-app-bar-color:** Changes the text color of the app bar (default is white)

#### How to use custom CSS properties

Add the following selector to your CSS:

```css
myuw-app-bar {
    --myuw-app-bar-bg: #fff;
    --myuw-app-bar-color: #c5050c;
    --myuw-app-bar-font: 'Roboto', sans-serif;
}
```

### Configuration / child components

Use the named `<slot>` tags to include child components of the top-app-bar:

```html
<myuw-app-bar>
    <your-navigation-drawer-component slot="myuw-navigation"></your-navigation-drawer-component>
    <your-notifications-component slot="myuw-notifications"></your-notifications-component>
</myuw-app-bar>
```

**Available slots:**
- **myuw-navigation**: Insert the `<myuw-navigation-drawer>` component
- **myuw-help**: Insert the `<myuw-help-and-feedback>` component
- **myuw-notifications**:  Insert the `<myuw-notifications>` component
- **myuw-profile**: Insert the `<myuw-profile>` component

*Note: Child components are a WIP*