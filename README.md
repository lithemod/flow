# Lithe Flow

This module provides interfaces for handling HTTP requests and responses in Lithe. It is useful for creating middlewares and offers a consistent way to manage HTTP interactions in your application.

## Features

- Defines interfaces for handling HTTP requests
- Supports middleware creation
- Ensures a consistent API for HTTP interactions

## Installation

To install the `flow` module, you can use Composer. Run the following command:

```bash
composer require lithemod/flow
```

### Requirements

- PHP 8 or higher
- Composer

## Configuration

After installation, you can configure the HTTP interfaces as needed in your Lithe application.

## Usage

### Example

Here’s a basic example of how to use the interfaces to create a middleware:

```php
use Lithe\Http\Request;
use Lithe\Http\Response;

function my_middleware($options) {
    return function (\Lithe\Http\Request $req, \Lithe\Http\Response $res, closure $next) use ($options) {
        // Middleware implementation based on the options array

        // Example: Modify the response
        $res->setHeader('X-Custom-Header', 'Value');
        
        // Call the next middleware
        $next();
    };
};
```

Refer to the documentation for detailed usage examples and best practices.

## Contributing

If you would like to contribute to the HTTP Interfaces module, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.