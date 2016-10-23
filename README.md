polymer-freegeoip-lookup
========================

Polymer element for client geolocation lookup with [freegeoip.net](http://freegeoip.net/)

Install
-------

```bash
bower install --save polymer-freegeoip-lookup
```

Usage
-----

```html
<link rel="import" href="freegeoip-lookup.html">
<freegeoip-lookup></freegeoip-lookup>
<script type="text/javascript">
  let el = document.querySelector('freegeoip-lookup');
  el.addEventListener('response-changed', (response) => {
    if(el.error) {
      alert('There was an error getting your location. Check your Ad-Blocker.');
    } else {
      alert('Freegeoip.net thinks you are at ' + el.response.latitude + ',' + el.response.longitude);
    }
  });
</script>

```

Configuration
-------------

The component can be configured via attributes on the HTMLElement.

|      Option      |           Default            |                              Description                               |
|------------------|------------------------------|------------------------------------------------------------------------|
| url              | `https://freegeoip.net/json` | lookup url, [self-host freegeoip](https://github.com/fiorix/freegeoip) |
| disable-autoload | `false`                      | does not automatically fire lookup on-load                             |

By calling the element's `lookup()` function a new request is sent to the IP lookup API. Changing the `url` attribute at runtime does not automatically trigger a new request.

Output
------

| Attribute |                                 Description                                 |
|-----------|-----------------------------------------------------------------------------|
| response  | An Object containing the server response. `{ latitude: 12, longitude: 34 }` |
| error     | Boolean value that is true, if there was an error requesting the location   |
| loading   | Boolean value that is true during active lookups                            |

Events
------

- response-changed
- loading-changed
- error-changed

```javascript
document.querySelector('freegeoip-lookup').addEventListener('response-changed', doSomething);
```

Demo
----

<!--
```html
<custom-element-demo height="75">
  <template>
    <link rel=import href=freegeoip-lookup.html>
    <div>
      <next-code-block></next-code-block>
    </div>
  </template>
</custom-element-demo>
```
```html
  <template is="dom-bind">
    <freegeoip-lookup response="{{response}}" loading="{{loading}}">
      <template is="dom-if" if="{{ loading }}">
        <div>Looking up your location on freegeoip.net ...</div>
      </template>
      <template is="dom-if" if="{{ !loading and  }}">
        <div>freeeoip.net thinks <a href$="http://www.google.com/maps/place/[[response.latitude]],[[response.longitude]]" target="_blank">your location</a> is:</div>
        <div>Latitude: <span>[[response.latitude]]</span></div>
        <div>Longitude: <span>[[response.longitude]]</span></div>
      </template>
    </freegeoip-lookup>
  </template>
```
-->
