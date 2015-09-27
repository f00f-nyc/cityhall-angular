This is the angluar library for City Hall Enterprise Setting Server

ABOUT

This project uses angular 1.2.28 and can be installed using:
  bower install cityhall
  


 USAGE

The intention is to use the built-in City Hall web site for actual
settings management, and then use this library for consuming those
settings in a web page.  As such, there are only a few commands to 
be familiar with:
   
   settings.login() - Must be called to initiate a session with City
     Hall. The password should be in plaintext, it will be hashed by
     the library.
     
   settings.logout() - To be called when the session is over.
   
   settings.getVal() - This should be the way that a value is returned.
     So, if the intention is to display the value of '/some_app/value1'
     on the page, then the HTML page will have:
        {{ value1 }}
     and the controller will contain:
        settings.getVal('/some_app/value1', $scope, 'value1');
     The library will make an async call to update $scope.value1, and
     the page will display it accordingly.

 For more in depth information about this library, please check the wiki.

 