# BS - custom

a template sass file based on my typical bootstrap customization.
will be updated very sporadicaly. This is my personal reference but will be public for others to use as a starting point.

## Callout Component

Additionally I am including an example of a custom mixin suggested by the bootstrap documentation, a callout. The callout component and can be found in the `_callout.scss` below. If you look at the bottom line of `custom.scss`, this mixin is included in a comment on the very last line. 
Include both of these files in the same directory and uncomment the last line in custom.scss to also genertate the callout components when you compile your `custom.scss`.

Feel free to ask me questions here if you are curious how to make or customize anything. 

## Usage

- 1. include bootstraps scss files in your project either in a `~/lib/bootstrap/scss` directory or change the url's in this file to point at their location in your project. Only those listed in the custom.scss You may alternatively include a single `bootstrap.scss` right below the import statement for `_functions.scss` and remove all other import statements for bootstrap within the file.
    - change the colors found towards the top of the file to your theme colors. EI: primary, secondary, tertiary etc.
    - set any other variables you may want to override within bootstrap. You can use any scss variables you might find while reading through the [bootstrap docs](https://getbootstrap.com/docs/5.3/customize/sass/).

- 2. use a web compiler to compile your `custom.scss` into `custom.css`
    - which scss compiler you use will depend on the type of your project.
    - for dotnet projects I suggest [WebCompiler](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.WebCompiler) 

- 3. include a reference to the compiled css file in your projects html head like the example below.
    - the reference to `custom.min.css` or `custom.css` should be after the reference to bootstrap and before the rest of the stylesheets for your project.
    - if you are also generating the callout component, there is no need to include a separate link reference for the callout file nor is there any need to attempt to compile `_callout.scss`. Uncommenting the very last line in `custom.scss` will generate the callout styles along with the rest of your `custom.css`.
 
```html
    <link href="css/app.css" rel="stylesheet" />
    <link href="lib/bootstrap/css/bootstrap.min.css" rel="stylesheet" />
    <link href="scss/custom.css" rel="stylesheet" />

```
