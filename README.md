# Patreon Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Patreon Scraper](https://oxylabs.io/products/scraper-api/web/patreon?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Patreon website effortlessly. This brief guide showcases how Patreon Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Patreon results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Patreon page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.patreon.com/pricing'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/patreon-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\" style=\"overflow-x:hidden\"><head><meta charSet=\"utf-8\"/><meta name=\"vi ... </html>",
      "created_at": "2024-01-10 09:35:00",
      "updated_at": "2024-01-10 09:35:02",
      "page": 1,
      "url": "https://www.patreon.com/pricing",
      "job_id": "7150782069029805057",
      "status_code": 200
    }
  ]
}
```
With our Patreon Scraper, you can seamlessly extract public data from any Patreon web page. Gather essential information about creators, such as their earnings, number of patrons, or content details, to understand your market and stay competitive. If you need assistance, our support team is here to help. Reach out via live chat or email us at hello@oxylabs.io.