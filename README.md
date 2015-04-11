# Leaflet.FormBuilder

Helpers to build forms synchronized with Leaflet objects.


# Usage

```
var tilelayerFields = [
    ['options.tilelayer.name', {handler: 'BlurInput', placeholder: 'display name'}],
    ['options.tilelayer.url_template', {handler: 'BlurInput', helpText: 'Supported scheme: http://{s}.domain.com/{z}/{x}/{y}.png', placeholder: 'url'}],
    ['options.tilelayer.maxZoom', {handler: 'BlurIntInput', placeholder: 'max zoom'}],
    ['options.tilelayer.minZoom', {handler: 'BlurIntInput', placeholder: 'min zoom'}],
    ['options.tilelayer.attribution', {handler: 'BlurInput', placeholder: 'attribution'}],
    ['options.tilelayer.tms', {handler: 'CheckBox', helpText: 'TMS format'}]
];
var builder = new L.FormBuilder(myObject, tilelayerFields, {
    callback: myCallback,
    callbackContext: this
});
myContainer.appendChild(builder.build());
```


See more examples of usage:

- https://github.com/yohanboniface/Leaflet.Storage/blob/master/src/js/leaflet.storage.forms.js
- https://github.com/kosmtik/kosmtik/blob/master/src/front/FormBuilder.js
- https://github.com/kosmtik/kosmtik/blob/master/src/front/Core.js#L102-L114
