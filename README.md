This is the angluar library for City Hall Enterprise Setting Server

# ABOUT

This project uses angular 1.2.28 and can be installed using:

```
bower install cityhall
```


# USAGE

The intention is to use the built-in City Hall web site for actual
settings management, and then use this library for consuming those
settings in a web page.  As such, there are only a few commands to 
be familiar with:
   
   
 ```javascript
 app.controller('CityHallCtrl', ['$scope', 'settings',
    function($scope, settings) {
 
    //Must be called to initiate a session with City Hall.
    //A user and password may be added, password should be plaintext.
    settings.login('http://path.to.server/api');
 
    //Asynchronously get the value of /test/val1/ and put it in $scope.val1
    settings.getVal('/test/val1', $scope, 'val1');
```

 For more in depth information about this library, please check the wiki.
 You can also check out the usage of this library in the City Hall viewer
 itself at: https://github.com/f00f-nyc/cityhall/
 

 