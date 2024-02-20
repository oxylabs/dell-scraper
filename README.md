# Dell Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Dell Scraper](https://oxylabs.io/products/scraper-api/ecommerce/dell?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Dell website effortlessly. This brief guide showcases how Dell Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Dell results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Dell page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.dell.com/en-us/shop/dell-laptops/sc/laptops'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/dell-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<!--[if IE ]> <![endif]-->\n<html dir=\"ltr\" lang=\"en-us\" class=\"no-js\">\n<head>\n    <m ... </html>",
      "created_at": "2024-02-20 12:47:41",
      "updated_at": "2024-02-20 12:47:48",
      "page": 1,
      "url": "https://www.dell.com/en-us/shop/dell-laptops/sc/laptops",
      "job_id": "7165688463033904129",
      "status_code": 200
    }
  ]
}
```
With our Dell Scraper, you can seamlessly pull public data from any Dell webpage. Gather the necessary product details like cost, ratings, or features, to study the market and stay a step ahead of your business rivals. If you require any assistance, reach out to our support team through live chat or drop us an email at hello@oxylabs.io.