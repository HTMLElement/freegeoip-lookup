polymer-freegeoip-lookup
========================

Polymer element for client geolocation lookup with [freegeoip.net](http://freegeoip.net/)

Install
-------

```bash
bower install --save polymer-freegeoip-lookup
```

Demo
----

<!--
```html
<custom-element-demo height="75">
  <template>
    <link rel=import href=polymer-freegeoip-lookup.html>
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
      <template is="dom-if" if="{{ !loading }}">
        <div>freeeoip.net thinks <a href$="http://www.google.com/maps/place/[[response.latitude]],[[response.longitude]]">your location</a> is:</div>
        <div>Latitude: <span>[[response.latitude]]</span></div>
        <div>Longitude: <span>[[response.longitude]]</span></div>
      </template>
    </freegeoip-lookup>
  </template>
```
-->
