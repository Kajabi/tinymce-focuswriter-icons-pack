### Kajabi fork dev notes
Figma svg source file: https://www.figma.com/file/OflCx3yN3sw5ycMGysO7nZ/tinymce-focuswriter-icons-pack?type=design&t=TJJ4to0XktvYQIxA-6

---

### Kajabi Tinymce `focuswriter_icons` icon pack 

This is a template project for creating an Icon Pack for TinyMCE. For instructions on how to use this project, [visit the documentation for Create an Icon Pack](https://www.tiny.cloud/docs/tinymce/latest/creating-an-icon-pack/).

### Quick guide
Open a terminal and navigate to the project folder, then

1. Install dependencies using `npm install`
3. Place your icons in `src/svg`
4. Run `gulp` to build the icon pack
5. Copy the contents of the generated icons file `dist/icons/focuswriter_icons/icons.js` to monolith `app/javascript/common/components/FocusWriter/assets/focuswriter_icons/register.js`
