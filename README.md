### Kajabi Tinymce `focuswriter_icons` icon pack

This is a template project for creating an Icon Pack for TinyMCE. For instructions on how to use this project, [visit the documentation for Create an Icon Pack](https://www.tiny.cloud/docs/tinymce/latest/creating-an-icon-pack/).

#### How to use

1. Install dependencies using `npm install`
   - Enter the name of the icon pack (found in `package.json`): `focuswriter_icons`
1. Place icons in `src/svg`
1. Run `gulp` to build the icon pack (See "Known Issues" below)
1. Open the file `dist/icons/focuswriter_icons/icons.js`
1. Copy _only your new icon_ to the Kajabi-products repo in the file
   - `app/javascript/common/components/FocusWriter/assets/focuswriter_icons/register.js`

### Known Issues

1. The generator is known to override some required elements from the original `<svg />`, causing the output icon to appear broken. 🥲
   - `highlight-bg-color`: The generator will remove a path tag that breaks the icon. We need to add that special `<path>` back in.
   ```
   <path d="M0 12H16V16H0V12Z" fill="#D9D9D9" class="tox-icon-highlight-bg-color__color"/>
   ```
   - `adobe-express`: The generator removed a few required elements from the `<svg />` like `<pattern />` and `<rect />`, so the output from this generator is not used in `kajabi-produts`

> UI example of the additional tag usage for `highlight-bg-color`. 👇 It allows TinyMCE to style the icon based on the color selected.
> ![Andrew McIntee Screenshot 2024-03-26 at 05-11-15PM@2x](https://github.com/Kajabi/tinymce-focuswriter-icons-pack/assets/565743/ef89b898-3e29-414a-be14-a815f1298744)

