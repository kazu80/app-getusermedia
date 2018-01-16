[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/owner/my-element)

# \<app-getusermedia\>

This is wrapper of navigator.getUserMedia

## VERSION

v0.2.1

## DEMO

<!--
```html
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="app-getusermedia.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<app-getusermedia></app-getusermedia>
```

## Installation

```
$ bower install --save monkick/app-getusermedia
```

## Usage

At first. Import it at header.  

```html
    <link rel="import" href="../bower_components/app-getusermedia/app-getusermedia.html">
```

Next. Add the `app-getusermedia` custom tag in body.

```html
    <app-getusermedia></app-getusermedia>
```

## Parameter

* video - take video stream
* audio - tale audio stream
* isUserMedia - status of getusermedia

```html
    <app-getusermedia video audio></app-getusermedia>
```

## Event

* getusermedia - This event fire when successful take media stream.
* error - This event fire when occur errors.

```javascript
    const media = document.getElementById('media');

    // successful event
    media.addEventListener('getusermedia', (event) => {
        console.log(event.detail.stream);
    });

    // error event
    media.addEventListener('error', (event) => {
        console.log(event.detail.message);
    });
```

## Method

start - It is build getusermedia. But auto started when put this element. 