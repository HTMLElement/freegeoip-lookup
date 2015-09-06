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
<freegeoip-lookup>
  <div>
    <template is="dom-if" if="!response">
      <div>Looking up location ...</div>
    </template>
    <template is="dom-if" if="response">
      <div>Your location:</div>
      <div>Lat: <span>[[response.latitude]]</span></div>
      <div>Lat: <span>[[response.latitude]]</span></div>
      <pre>[[response]]</pre>
    </template>
  </div>
</freegeoip-lookup>
```
