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
```
<custom-element-demo>
  <template>
    <link rel=import href=polymer-freegeoip-lookup.html>
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
  </template>    
</custom-element-demo>
```
-->

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
