# Fork From Image Block for the [Editor.js](https://editorjs.io).

## Modified some code to separate the API Request value from the preview value for the image preview feature.

- Install
```shell
  npm i @seg00/editorjs-image-preview
```

- Use
```javascript
import ImageTool from "@seg00/editorjs-image-preview";
```

- The image upload API requires the 'file' object to have a 'preview' variable.
```javascript
{
    ...
    data: {
        time: 1700475383740
        blocks: [
            {
                id: String,
                type: "image",
                data: {
                    caption: String,
                    withBorder: Boolean,
                    withBackground: Boolean,
                    stretched: Boolean,
                    file: {
                        // It should be in the form of a “path” for the image upload API and DB storage.
                        // eg) editor/8561a264-6536-4894-bd29-d25b32fca273
                        url: String,
                        // This should be in the form of an image URL as a preview in the editor.
                        // eg) S3 Pre-signed URL : Need Another Action
                        preview: String,
                    },
                },
            },
        ]
    }
    ...
}
```
