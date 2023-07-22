
# Simple HTTP client for PHP

Install  
```
composer require krishnan/http-client
```  

Import class  
```php
use Krishnan\Http\Http;
```

### GET request
```php
$url    = "https://jsonplaceholder.typicode.com/comments";
$data   = [ 'postId' => 1 ];

$response = HTTP::get( $url, $data );
```
### POST request
```php
$url    = "https://jsonplaceholder.typicode.com/posts";
$data   = [ 'title' => 'This is post title' ];

$response = HTTP::post( $url, $data );
```

### More options
```php
$response = HTTP::get( $url, $data, $headers, $curlOptions );
$response = HTTP::post( $url, $data, $headers, $curlOptions );
```

### Useful methods
```php
$response->getStatusCode(); // to get response code
$response->getHeaders(); // to get all headers as array
$response->getHeader($name); // to get specific header
$response->getBody(); // to get raw response body
$response->getJson(); // to get body as assoc array
$response->getObject(); // to get body as object
```

### Credits
This repository is a clone of https://github.com/haruncpi/http. Kudos to the original builder to build a very simple and efficient http client which can be easily understood and implemented by even a new programmer. I have cloned it as I will be making some changes for my projects. 