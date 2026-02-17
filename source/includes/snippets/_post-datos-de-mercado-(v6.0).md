> Ejemplo de petición

```shell
curl -X POST -H "Authorization: Token YOUR_TOKEN" "https://clientela.admetricks.com/market-report/data/v6/?day=2022-10-01&country=1&device=1&ad_type=1"
```

```python
import requests

headers = {
    'Authorization': 'Token YOUR_TOKEN',
    'content-type': 'application/json'
}

params = (
    ('day', '2022-10-01'),
    ('country', '1'),
    ('device', '1'),
    ('ad_type', '1'),
)

response = requests.post(
  'https://clientela.admetricks.com/market-report/data/v6/',
  headers=headers,
  params=params
)
```

```javascript
const endpoint =
  "https://clientela.admetricks.com/market-report/data/v6/?day=2022-10-01&country=1&device=1&ad_type=1";

fetch(endpoint, {
  method: "POST",
  headers: {
    Authorization: "Token YOUR_TOKEN",
    "content-type": "application/json",
  },
});
```

```php
<?php

include('vendor/rmccue/requests/library/Requests.php');
Requests::register_autoloader();

$headers = array(
    'authorization' => 'Token YOUR_TOKEN',
    'content-type' => 'application/json;charset=UTF-8'
);
$endpoint = 'https://clientela.admetricks.com/market-report/data/v6/?day=2022-10-01&country=1&device=1&ad_type=1'

$response = Requests::post($endpoint, $headers);

?>
```

> Ejemplo de petición filtrando por industrias

```shell
curl -X POST -H "Authorization: Token YOUR_TOKEN" "https://clientela.admetricks.com/market-report/data/v6/?day=2022-10-01&country=1&device=1&ad_type=1&industries=281,282,288,289"
```

```python
import requests

headers = {
    'Authorization': 'Token YOUR_TOKEN',
    'content-type': 'application/json'
}

params = (
    ('day', '2022-10-01'),
    ('country', '1'),
    ('device', '1'),
    ('ad_type', '1'),
    ('industries', '281,282,288,289')
)

response = requests.post(
  'https://clientela.admetricks.com/market-report/data/v6/',
  headers=headers,
  params=params
)
```

```javascript
const endpoint =
  "https://clientela.admetricks.com/market-report/data/v6/?day=2022-10-01&country=1&device=1&ad_type=1&industries=281,282,288,289";

fetch(endpoint, {
  method: "POST",
  headers: {
    Authorization: "Token YOUR_TOKEN",
    "content-type": "application/json",
  },
});
```

```php
<?php

include('vendor/rmccue/requests/library/Requests.php');
Requests::register_autoloader();

$headers = array(
    'authorization' => 'Token YOUR_TOKEN',
    'content-type' => 'application/json;charset=UTF-8'
);
$endpoint = 'https://clientela.admetricks.com/market-report/data/v6/?day=2022-10-01&country=1&device=1&ad_type=1&industries=281,282,288,289'

$response = Requests::post($endpoint, $headers);

?>
```

> Ejemplo de petición filtrando por websites

```shell
curl -X POST -H "Authorization: Token YOUR_TOKEN" "https://clientela.admetricks.com/market-report/data/v6/?day=2026-01-01&country=3&device=1&ad_type=1&websites=1098,1106,8277"
```

```python
import requests

headers = {
    'Authorization': 'Token YOUR_TOKEN',
    'content-type': 'application/json'
}

params = (
    ('day', '2026-01-01'),
    ('country', '3'),
    ('device', '1'),
    ('ad_type', '1'),
    ('websites', '1098,1106,8277')
)

response = requests.post(
  'https://clientela.admetricks.com/market-report/data/v6/',
  headers=headers,
  params=params
)
```

```javascript
const endpoint =
  "https://clientela.admetricks.com/market-report/data/v6/?day=2026-01-01&country=3&device=1&ad_type=1&websites=1098,1106,8277";

fetch(endpoint, {
  method: "POST",
  headers: {
    Authorization: "Token YOUR_TOKEN",
    "content-type": "application/json",
  },
});
```

```php
<?php

include('vendor/rmccue/requests/library/Requests.php');
Requests::register_autoloader();

$headers = array(
    'authorization' => 'Token YOUR_TOKEN',
    'content-type' => 'application/json;charset=UTF-8'
);
$endpoint = 'https://clientela.admetricks.com/market-report/data/v6/?day=2026-01-01&country=3&device=1&ad_type=1&websites=1098,1106,8277'

$response = Requests::post($endpoint, $headers);

?>
```


> Ejemplo de respuesta exitosa

```json
{
  "data": [
    {
        "date": "2022-10-01",
        "industry_id": 294,
        "industry": "textil y vestimenta - relojería y joyería",
        "brand_id": 435694,
        "brand": "casiog shock",
        "campaign_id": 10602653,
        "campaign_name": "Iniciar sesión • Instagram",
        "campaign_landing_page": "instagram.com/gshockperuoficial",
        "campaign_language": "es",
        "website_id": 1905,
        "website": "milenio.com",
        "ad_link": "https://ads.admetricks.com/banner_eee1835b8b77936e328370559019ab95.jpg",
        "screenshot_link": "https://screenshots.admetricks.com/cache_id2284eb2b81014698bb1fa9e9ad9da48a.jpg",
        "ad_type_id": 1,
        "device_id": 1,
        "country_id": 6,
        "country": "peru",
        "ad_type": "display",
        "device": "desktop",
        "metrics_valuation": 529.3551,
        "metrics_impressions": 79056,
        "metrics_valuation_usd": 138.755,
        "metrics_count": 27,
        "metrics_impact": 5728,
        "ad_sizes": "300x250,160x600",
        "sold_bys": "google",
        "website_sections": "article",
        "advertiser": "Not classified",
        "publisher": "multimedios",
        "web_report": "https://web.admetricks.com/#/campaign?name=Iniciar%20sesi%C3%B3n%20%E2%80%A2%20Instagram&request_filters=eyJjYW1wYWlnbnMiOiB7ImluY2x1ZGUiOiBbeyJpZCI6IDEwNjAyNjUzfV19LCAiZGF0ZV9yYW5nZSI6IHsic3RhcnQiOiAiMjAyMi0xMC0wMVQwMDowMDowMC4wMDBaIiwgImVuZCI6ICIyMDIyLTEwLTAxVDIzOjU5OjU5Ljk5OVoifSwgImFkX3R5cGVzIjogeyJpbmNsdWRlIjogW3siaWQiOiAxfV19LCAiZGV2aWNlcyI6IHsiaW5jbHVkZSI6IFt7ImlkIjogMX1dfSwgImNvdW50cmllcyI6IHsiaW5jbHVkZSI6IFt7ImlkIjogNn1dfX0%3D",
        "skip": 0.0,
        "hosted_by": "googleadservices.com,doubleclick.net",
        "duration": "0",
        "position": "First scroll: 0.00%, Second scroll: 0.00%, Third or more: 100.00%",
        "campaign_tags": ""
        "is_fixed_ad": 1
    }
  ]
}
```
