# jQuery Image Upload
A jQuery plugin that adds controls to the selected jQuery elements with a simple call.

## Example

```js
// initialize image upload
$(".image").imageUpload({
    formAction: "/upload"
}).on("imageChanged", function () {
    console.log("Changed the src");
});
```

## Available on CDN
This library is available on [CDNJS](https://cdnjs.com/libraries/jquery-image-upload).

## Documentation

### Options

<table>
    <thead>
        <tr>
            <th>Option Name</th>
            <th>Description</th>
            <th>Type</th>
            <th>Values</th>
            <th>Default</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>formAction</code></td>
            <td>The url that will compute the form data and upload the image on the server. This must respond with a string that represents the new image source.</td>
            <td>String</td>
            <td>Any string</td>
            <td>No default value, but required field</td>
        </tr>
        <tr>
            <td><code>wrapContent</code></td>
            <td>The element that must wrap the selected elements. Used only when <code>hover</code> is <code>false</code></td>
            <td>String</td>
            <td>HTML String or jQuery object</td>
            <td><code>"&lt;div class='jQuery-imageUpload'&gt;"</code></td>
        </tr>
        <tr>
            <td><code>inputFileName</code></td>
            <td>The name of the file input element.</td>
            <td>String</td>
            <td>Any string</td>
            <td>inputFile</td>
        </tr>
        <tr>
            <td><code>inputFileClass</code></td>
            <td>The class of the file input element</td>
            <td>String</td>
            <td>Any string</td>
            <td>inputFile</td>
        </tr>
        <tr>
            <td><code>uploadButtonValue</code></td>
            <td>The value (text) of the upload button.</td>
            <td>String</td>
            <td>Any string</td>
            <td>Upload</td>
        </tr>
        <tr>
            <td><code>uploadButtonClass</code></td>
            <td>The class of the upload button element</td>
            <td>String</td>
            <td>Any string</td>
            <td>uploadButton</td>
        </tr>
        <tr>
            <td><code>browseButtonValue</code></td>
            <td>The value (text) of the browse button element.</td>
            <td>String</td>
            <td>Any string</td>
            <td>Browse</td>
        </tr>
        <tr>
            <td><code>browseButtonClass</code></td>
            <td>The class of the browse button element</td>
            <td>String</td>
            <td>Any string</td>
            <td>browseButton</td>
        </tr>
        <tr>
            <td><code>deleteButtonValue</code></td>
            <td>The value (text) of the delete button element.</td>
            <td>String</td>
            <td>Any string</td>
            <td>Delete image</td>
        </tr>
        <tr>
            <td><code>deleteButtonClass</code></td>
            <td>The class of the delete button element</td>
            <td>String</td>
            <td>Any string</td>
            <td>deleteButton</td>
        </tr>
        <tr>
            <td><code>automaticUpload</code></td>
            <td>One click and the image is uploaded. If this is <code>true</code>, the upload button will be hidden.</td>
            <td>Boolean</td>
            <td>true/false</td>
            <td>false</td>
        </tr>
        <tr>
            <td><code>formClass</code></td>
            <td>The class of the form</td>
            <td>String</td>
            <td>Any string</td>
            <td>controlForm</td>
        </tr>
        <tr>
            <td><code>hideFileInput</code></td>
            <td>If this is <code>true</code> the Browse button will be used and the native file input will be hidden</td>
            <td>Boolean</td>
            <td>true/false</td>
            <td>true</td>
        </tr>
        <tr>
            <td><code>hideDeleteButton</code></td>
            <td>Hide or show the delete button.</td>
            <td>Boolean</td>
            <td>true/false</td>
            <td>false</td>
        </tr>
        <tr>
            <td><code>hover</code></td>
            <td>Show the controls only on hover.</td>
            <td>Boolean</td>
            <td>true/false</td>
            <td>true</td>
        </tr>
        <tr>
            <td><code>addClass</code></td>
            <td>The class that must be added to the wrapper.</td>
            <td>String</td>
            <td>Any string</td>
            <td>jQuery-image-upload</td>
        </tr>
        <tr>
            <td><code>waiter</code></td>
            <td>Path to the gif image that should be used as waiter.</td>
            <td>String</td>
            <td>Path</td>
            <td></td>
        </tr>
    </tbody>
</table>


## Events

The plugin emits the following events:

<table>
    <thead>
        <tr>
            <th>Event Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>imageUpload.reload</td>
            <td>Destroys and inits the plugin</td>
        </tr>
        <tr>
            <td>imageUpload.imageChanged</td>
            <td>Ocurrs after the source of the image was changed (the image was sucessfully uploaded)</td>
        </tr>
        <tr>
            <td>imageUpload.uploadFailed</td>
            <td>This event is emitted when the image upload failed. If there is an error, you can get that too: <code>on("imageUpload.uploadFailed", function (ev, err) {...})</code></td>
        </tr>
        <tr>
            <td>imageUpload.destroy</td>
            <td>Used to destroy an instance of the plugin</td>
        </tr>
    </tbody>
</table>



## How to contribute

1. File an issue in the repository, using the bug tracker, describing the
   contribution you'd like to make. This will help us to get you started on the
   right foot.
2. Fork the project in your account and create a new branch:
   `your-great-feature`.
3. Commit your changes in that branch.
4. Open a pull request, and reference the initial issue in the pull request
   message.

## License
See the [LICENSE](./LICENSE) file.
