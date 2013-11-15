Callsign.js
===========

A js library for getting FCC callsign info.

All requests are proxied due to the lack of JSONp support on fcc.gov.


### Usage ###

``` javascript
var callmgr = new Callsign(opts);

callmgr.get('<callsign>', function(info) {
	console.log(info);
});
```

### Options ###

Options that can be passed in:

	* url: must contain two "variables", %S and %C. %S being the callsign to
	be looked up and %C being the callback to call.
	* map: list of field mappings from the raw JSON to "pretty" names.
	* callback: callback to use for the JSONP request.

