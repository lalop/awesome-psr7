# Awesome [PSR-7](http://www.php-fig.org/psr/psr-7/)
 A curated list of amazingly awesome PHP libraries that implement PSR-7 or at least are compatible with it.
 
 I loved the [StackPHP](http://stackphp.com/) initiative but since PSR-7 is out I think the way to do good middlewares is by building them to handle PSR-7 request/response.
 
 
## PSR-7 implementation

* [Guzzle-psr7](https://github.com/guzzle/psr7)
* [Slim-Http](https://github.com/slimphp/Slim-Http)
* [Zend-diactoros](https://github.com/zendframework/zend-diactoros)

## PSR-7 middleware stack management

This libraries handle a stack of middlewares that will be called successively during the request treatment.
Since PSR-7 is only about the message and it doesn't define middleware. Any way a common signature for a middleware is anything callable that matches this :
```php 
function (
    Psr\Http\Message\ResponseInterface $request,
    Psr\Http\Message\RequestInterface $response,
    callable $next  // the next middleware
) {
    // ...
}
```


* [Relay](http://relayphp.com/)
* [Slim](http://www.slimframework.com/)
* [Zend-stratigility](https://github.com/zendframework/zend-stratigility)
* [Expressive](https://zendframework.github.io/zend-expressive/), based on Zend-stratigility
* [SpiralFramework](https://spiral-framework.com/guide)


## PSR-7 middlewares


### collections of middlewares

* https://github.com/relayphp/Relay.Middleware
* https://github.com/oscarotero/psr7-middlewares

### Authentication

* [PSR-7 Storage-less HTTP Sessions](https://github.com/Ocramius/PSR7Session)

### Security

* [Slim-Csrf](https://github.com/slimphp/Slim-Csrf)
* [Proxy Scheme and Host detection middleware](https://github.com/akrabat/rka-scheme-and-host-detection-middleware)
* [Client IP address middleware](https://github.com/akrabat/rka-ip-address-middleware)
* [PSR-7 Storage-less HTTP CSRF protection](https://github.com/Ocramius/PSR7Csrf)

### Optimisation

* [Slim Framework HTTP Cache](https://github.com/slimphp/Slim-HttpCache)





### HTTP client 

* [Guzzle](http://guzzlephp.org/)
* [HTTPlug](http://httplug.io/)

### Miscellaneous

* [Cross-Origin Resource Sharing](https://github.com/neomerx/cors-psr7)
