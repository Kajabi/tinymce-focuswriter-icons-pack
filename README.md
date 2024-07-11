### Kajabi Tinymce `focuswriter_icons` icon pack

This is a template project for creating an Icon Pack for TinyMCE. For instructions on how to use this project, [visit the documentation for Create an Icon Pack](https://www.tiny.cloud/docs/tinymce/latest/creating-an-icon-pack/).

#### How to use

1. Install dependencies using `npm install`
   - Enter the name of the icon pack (found in `package.json`): `focuswriter_icons`
1. Place icons in `src/svg`
1. Run `gulp` to build the icon pack
1. Open the file `dist/icons/focuswriter_icons/icons.js`
1. Copy _only your new icon_ to the Kajabi-products repo in the file
   - `app/javascript/common/components/FocusWriter/assets/focuswriter_icons/register.js`

### Known Issues

1. The `gulp` task is known to override some required elements from the original `<svg />`, causing the output icon to appear broken. The following icons were not copied from this repo directly into the `kajabi-products` repo:
   - `highlight-bg-color`: The `gulp` task removed the path tag `<path d="M0 12H16V16H0V12Z" fill="#D9D9D9" class="tox-icon-highlight-bg-color__color"/>` which is necessary to display the active color
   - `adobe-express`: This is a multi-color icon with a base64 image that contained a few `svg` related elements like `<pattern />` and `<rect />` that were removed by the `gulp` task.

![Andrew McIntee Screenshot 2024-03-26 at 05-11-15PM@2x](https://github.com/Kajabi/tinymce-focuswriter-icons-pack/assets/565743/ef89b898-3e29-414a-be14-a815f1298744)
