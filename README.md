### Kajabi Tinymce `focuswriter_icons` icon pack 

This is a template project for creating an Icon Pack for TinyMCE. For instructions on how to use this project, [visit the documentation for Create an Icon Pack](https://www.tiny.cloud/docs/tinymce/latest/creating-an-icon-pack/).

#### How to use

1. Install dependencies using `npm install`
2. Place icons in `src/svg`
3. Run `gulp` to build the icon pack
4. Use `focuswriter_icons` when prompted for the icon pack name
5. Copy the contents of the generated icons file `dist/icons/focuswriter_icons/icons.js` to monolith `app/javascript/common/components/FocusWriter/assets/focuswriter_icons/register.js`
6. Add the path tag to the generated `highlight-bg-color` svg
    ```
    <path d="M0 12H16V16H0V12Z" fill="#D9D9D9" class="tox-icon-highlight-bg-color__color"/>
    ```
    - The `highlight-bg-color` color will override the stock icon. Inside of the stock icon there is a special `<path>` to display the active color. We need to add that special `<path>` back in.
    - This generator doesn't handle this specific case. 🥲
    - UI example of the additional tag usage 👇 It allows TinyMCE to style the icon based on the color selected.
![Andrew McIntee Screenshot 2024-03-26 at 05-11-15PM@2x](https://github.com/Kajabi/tinymce-focuswriter-icons-pack/assets/565743/ef89b898-3e29-414a-be14-a815f1298744)




#### Figma source file
There's a Figma source file that can be used export icons from Figma (not required). It's useful for multiple icons out of a design comp quickly.

🔗 https://www.figma.com/file/OflCx3yN3sw5ycMGysO7nZ/tinymce-focuswriter-icons-pack?type=design&t=TJJ4to0XktvYQIxA-6
