# Gist Analytics API Connection

The client class interacts with the Gist Analytics Platform to get and set data

## Installation

Install using composer

```bash
composer require gist/analytics
```

## Usage

Sign up for Gist Analytics at https://analytics.gist-apps.com/register

Register your application, and make note of the Access token generated. This
token will only be displayed once, so make sure to save the record of it.

```php
use Gist\Analytics;

$client = new Analytics\Client([
  'api_key' => 'Your API key'
]);

// Insert a new record
$event = $client->insert($name, $value, $meta = []);

// Query for existing records.
$event = $client->query($name, $startDate, $endDate, $query = [], $meta = [], $format = "default");

```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
