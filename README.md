AngularJS_IE_cache_ajax_GET
===========================
For AngularJS app that use $http.get, IE8/9 caches Ajax GET request and returns the result from browser cache with a 304 http response, rather than going to the server.

# Note:

Using Angularjs $http with cache = false does **NOT** work with IE. 

````$http({method: 'GET', url: url, cache: false});````

The other option could fall back to JQuery with cache = false

````
$.ajax({
  url: '/some/url',
	type: 'GET',
	cache: false,
	success: function(status) {
	 ...
	}
});	
````
