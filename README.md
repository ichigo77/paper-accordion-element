
##&lt;paper-accordion-element&gt;

`paper-accordion-element` is a container with a header and a content part. By default the content is hidden and after clicking on the header text the content appears.  

###Attributes
In order to pass the header text and additional header icons, the following attributes can be used. 

| Attribute | Description | Value | Accessibility |
| --- | --- | --- | --- |
| `header-text` | pass the text which is displayed in the header | each string | read/write |
| `default-icon` | icon which is located next to the header text | an icon of the iron-icon set | read/write | 
| `open-icon` | icon which is shown after collapsing content | an icon of the iron-icon set | read/write |
| `content-collapsed` |  gets info if content is collapsed | true/false | read |

Example - only text:

```html
<paper-accordion-element header-text="Some header text">
  Some content
</paper-accordion-element>
```

Example - header text with default icon:

```html
<paper-accordion-element header-text="Some header text" default-icon="expand-less">
  Some content
  </paper-accordion-element>
```

Example - header text with default  and open icon:

```html
<paper-accordion-element header-text="Some header text" default-icon="expand-less" open-icon="expand-more">
  Some content
  </paper-accordion-element>
```

### Styling

The following custom properties and mixins are available for styling:

| Custom property | Description | Default |
| --- | --- | --- |
`--accordion-header` | mixin for the header | `{}`
`--accordion-header-text` | mixin for the header text | `{}`
`--accordion-header-ripple-color` | sets the color of the ripple | `#4285f4`
`--accordion-duration` | Transition duration time which defines how long the opening transition takes | `300ms`  

### Dependencies
The element `paper-accordion-element` requires the following references.

*  `polymer`
*  `paper-card`
*  `paper-ripple`
*  `iron-icon`
* `iron-icons`
* `iron-flex-layout`  

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

### Playing

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/paper-accordion-element/`

### Testing 
The tests are located in the directory `/test`  
Please use the [web-component-tester](https://github.com/Polymer/web-component-tester) to run the tests. WCT can be installed via npm:

    npm install -g web-component-tester

Then, you can run your tests on *all* of your local browsers via:

    wct   
       
##&lt;paper-accordion-container&gt;##
`paper-accordion-container` is a wrapper element which can be used to gain the behavior that only one `paper-accordion-element` can be collapsed.

Example

```html
  <paper-accordion-container>
    <paper-accordion-element header-text="Some header text">
        Some content
    </paper-accordion-element>
    <paper-accordion-element header-text="Some header text #2">
        Some content
    </paper-accordion-element>
    <paper-accordion-element header-text="Some header text #3">
        <paper-accordion-container>
               <paper-accordion-element header-text="Some header text #3.1">
                 Some content
              </paper-accordion-element>
              <paper-accordion-element header-text="Some header text #3.2">
                 Some content
              </paper-accordion-element>
        <paper-accordion-container>
    </paper-accordion-element>
  </paper-accordion-container>
```

### Styling

The following custom property is available for styling:

| Custom property | Description | Default |
| --- | --- | --- |
|`--accordion-container-element-margin` | sets the margin between the `paper-accordion-element` items | 5px |

### Dependencies
The element `paper-accordion-container` requires the following reference.

*  `polymer`

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

### Playing

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/paper-accordion-element/`

### Testing 
The tests are located in the directory `/test`  
Please use the [web-component-tester](https://github.com/Polymer/web-component-tester) to run the tests. WCT can be installed via npm:

    npm install -g web-component-tester

Then, you can run your tests on *all* of your local browsers via:

    wct

