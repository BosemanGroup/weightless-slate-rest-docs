---
title: Weightless v1.0
language_tabs:
  - ruby: Ruby
  - python: Python
  - javascript: JavaScript
  - go: Go
  - shell: " cURL"
language_clients:
  - ruby: ""
  - python: ""
  - javascript: ""
  - go: ""
  - shell: ""
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="weightless">Weightless v1.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="testtesthttps://api.weightless.com">testtesthttps://api.weightless.com</a>

<h1 id="weightless-debts">Debts</h1>

## Retrieve a Debt

<a id="opIdget-debts-by-id"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/debts/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/debts/{id}', headers = headers)

print(r.json())

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/debts/{id}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/debts/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/debts/{id} \
  -H 'Accept: application/json'

```

`GET /debts/{id}`

Retrieves a debt object that you have linked.

<h3 id="retrieve-a-debt-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

> Example responses

> OK

```json
{
  "debt_id": "string",
  "type": "string",
  "subtype": "string",
  "provider_id": 0,
  "provider_name": "string",
  "apr": 0,
  "currency": "string",
  "current_balance": 0,
  "last_statement_balance": 0,
  "last_statement_issue_date": 0,
  "minimum_payment": 0,
  "next_payment_due_date": "string"
}
```

<h3 id="retrieve-a-debt-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="retrieve-a-debt-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» debt_id|string|false|none|none|
|» type|string|false|none|none|
|» subtype|string|false|none|none|
|» provider_id|integer|false|none|none|
|» provider_name|string|false|none|none|
|» apr|number|false|none|none|
|» currency|string|false|none|none|
|» current_balance|number|false|none|none|
|» last_statement_balance|number|false|none|none|
|» last_statement_issue_date|number|false|none|none|
|» minimum_payment|integer|false|none|none|
|» next_payment_due_date|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## List all Debts

<a id="opIdget-debts"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/debts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/debts', headers = headers)

print(r.json())

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/debts',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/debts", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/debts \
  -H 'Accept: application/json'

```

`GET /debts`

Returns a list of debts that you have linked.

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "debt_id": "string",
      "type": "string",
      "subtype": "string",
      "provider_id": 0,
      "provider_name": "string",
      "apr": 0,
      "currency": "string",
      "current_balance": 0,
      "last_statement_balance": 0,
      "last_statement_issue_date": 0,
      "minimum_payment": 0,
      "next_payment_due_date": "string"
    }
  ]
}
```

<h3 id="list-all-debts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="list-all-debts-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» data|[object]|false|none|none|
|»» debt_id|string|false|none|none|
|»» type|string|false|none|none|
|»» subtype|string|false|none|none|
|»» provider_id|integer|false|none|none|
|»» provider_name|string|false|none|none|
|»» apr|number|false|none|none|
|»» currency|string|false|none|none|
|»» current_balance|number|false|none|none|
|»» last_statement_balance|number|false|none|none|
|»» last_statement_issue_date|number|false|none|none|
|»» minimum_payment|integer|false|none|none|
|»» next_payment_due_date|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="weightless-repayments">Repayments</h1>

## Retrieve minimum Repayment

<a id="opIdget-debts-minimum-payment"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/repayments/minimum-amount',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/repayments/minimum-amount', headers = headers)

print(r.json())

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/repayments/minimum-amount',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/repayments/minimum-amount", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/repayments/minimum-amount \
  -H 'Accept: application/json'

```

`GET /repayments/minimum-amount`

Retrieve the minimum repayment amount required for each debt that you have linked.

> Example responses

> 200 Response

```json
{
  "amount": 0,
  "currency": "string"
}
```

<h3 id="retrieve-minimum-repayment-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="retrieve-minimum-repayment-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» amount|integer|false|none|none|
|» currency|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Retrieve Monthly Schedule

<a id="opIdget-debts-monthly-payment"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/repayments/monthly-schedule',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/repayments/monthly-schedule', headers = headers)

print(r.json())

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/repayments/monthly-schedule',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/repayments/monthly-schedule", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/repayments/monthly-schedule \
  -H 'Accept: application/json'

```

`GET /repayments/monthly-schedule`

Retrieve the monthly payment details for debt repayments. 

> Example responses

> OK

```json
{
  "enabled": true,
  "amount": 125.45,
  "currency": "usd",
  "day_of_month": 20
}
```

<h3 id="retrieve-monthly-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="retrieve-monthly-schedule-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» enabled|boolean|false|none|none|
|» amount|number|false|none|none|
|» currency|string|false|none|none|
|» day_of_month|integer|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Update Monthly Schedule

<a id="opIdput-debts-monthly-payment"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'testtesthttps://api.weightless.com/repayments/monthly-schedule',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.put('testtesthttps://api.weightless.com/repayments/monthly-schedule', headers = headers)

print(r.json())

```

```javascript
const inputBody = '{
  "enabled": true,
  "amount": 125.45,
  "currency": "usd",
  "day_of_month": 20
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('testtesthttps://api.weightless.com/repayments/monthly-schedule',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "testtesthttps://api.weightless.com/repayments/monthly-schedule", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X PUT testtesthttps://api.weightless.com/repayments/monthly-schedule \
  -H 'Content-Type: application/json'

```

`PUT /repayments/monthly-schedule`

Update 

> Body parameter

```json
{
  "enabled": true,
  "amount": 125.45,
  "currency": "usd",
  "day_of_month": 20
}
```

<h3 id="update-monthly-schedule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» enabled|body|boolean|false|none|
|» amount|body|number|false|none|
|» currency|body|string|false|none|
|» day_of_month|body|integer|false|none|

<h3 id="update-monthly-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

## Update Monthly Schedule Enabled

<a id="opIdput-debts-monthly-payment-enabled"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'testtesthttps://api.weightless.com/repayments/monthly-schedule/enabled',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.put('testtesthttps://api.weightless.com/repayments/monthly-schedule/enabled', headers = headers)

print(r.json())

```

```javascript
const inputBody = '{
  "enabled": true
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('testtesthttps://api.weightless.com/repayments/monthly-schedule/enabled',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "testtesthttps://api.weightless.com/repayments/monthly-schedule/enabled", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X PUT testtesthttps://api.weightless.com/repayments/monthly-schedule/enabled \
  -H 'Content-Type: application/json'

```

`PUT /repayments/monthly-schedule/enabled`

Update the monthly payment details for debt repayments.

> Body parameter

```json
{
  "enabled": true
}
```

<h3 id="update-monthly-schedule-enabled-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» enabled|body|boolean|false|none|

<h3 id="update-monthly-schedule-enabled-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|

<aside class="success">
This operation does not require authentication
</aside>

## Retrieve recommended monthly Repayment

<a id="opIdget-debts-recommended-monthly-payment"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/repayments/recommended',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/repayments/recommended', headers = headers)

print(r.json())

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/repayments/recommended',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/repayments/recommended", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/repayments/recommended \
  -H 'Accept: application/json'

```

`GET /repayments/recommended`

Retrieve the recommended monthly debt repayments. We calculate using xyz

> Example responses

> 200 Response

```json
{
  "amount": 0,
  "currency": "string",
  "description": "string"
}
```

<h3 id="retrieve-recommended-monthly-repayment-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="retrieve-recommended-monthly-repayment-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» amount|integer|false|none|none|
|» currency|string|false|none|none|
|» description|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## List all Repayments

<a id="opIdget-payments"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/repayments',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/repayments', headers = headers)

print(r.json())

```

```javascript
const inputBody = '{
  "debt_ids": [
    "123",
    "456"
  ],
  "count": 100,
  "offset": 0,
  "start_date": "2020-04-13",
  "end_date": "2020-04-13",
  "amount": null
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/repayments',
{
  method: 'GET',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/repayments", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/repayments \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

`GET /repayments`

Returns a list of debt repayments

> Body parameter

```json
{
  "debt_ids": [
    "123",
    "456"
  ],
  "count": 100,
  "offset": 0,
  "start_date": "2020-04-13",
  "end_date": "2020-04-13",
  "amount": null
}
```

<h3 id="list-all-repayments-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» debt_ids|body|[string]|false|none|
|» count|body|integer|false|none|
|» offset|body|integer|false|none|
|» start_date|body|string|false|none|
|» end_date|body|string|false|none|

> Example responses

> OK

```json
{
  "data": [
    {
      "debt_id": "123e4567-e89b-12d3-a456-426614174000",
      "amount": 125.45,
      "currency": "usd",
      "date_created": "2020-04-13"
    }
  ]
}
```

<h3 id="list-all-repayments-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="list-all-repayments-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» data|[object]|false|none|none|
|»» debt_id|string|false|none|none|
|»» amount|number|false|none|none|
|»» currency|string|false|none|none|
|»» date_created|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Create a Payment

<a id="opIdpost-payments"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'testtesthttps://api.weightless.com/repayments',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('testtesthttps://api.weightless.com/repayments', headers = headers)

print(r.json())

```

```javascript
const inputBody = '{
  "debt_id": "123e4567-e89b-12d3-a456-426614174000",
  "amount": 125.45,
  "currency": "usd",
  "date_created": "2020-04-13"
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('testtesthttps://api.weightless.com/repayments',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "testtesthttps://api.weightless.com/repayments", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X POST testtesthttps://api.weightless.com/repayments \
  -H 'Content-Type: application/json'

```

`POST /repayments`

Manually create a repayment towards your debts. We will calculate which debt or debts this repayment will be made towards to reduce the overall amount you need to repay to be debt free.

> Body parameter

```json
{
  "debt_id": "123e4567-e89b-12d3-a456-426614174000",
  "amount": 125.45,
  "currency": "usd",
  "date_created": "2020-04-13"
}
```

<h3 id="create-a-payment-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» debt_id|body|string|false|none|
|» amount|body|number|false|none|
|» currency|body|string|false|none|
|» date_created|body|string|false|none|

<h3 id="create-a-payment-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|

<aside class="success">
This operation does not require authentication
</aside>

## Retrieve time to be debt free

<a id="opIdget-debts-debt-free"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/repayments/debt-free',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/repayments/debt-free', headers = headers)

print(r.json())

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/repayments/debt-free',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/repayments/debt-free", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/repayments/debt-free \
  -H 'Accept: application/json'

```

`GET /repayments/debt-free`

Retrieve the forecasted date to be debt free with the current monthly repayment schedule.

> Example responses

> OK

```json
{
  "end_date": "2020-04-13"
}
```

<h3 id="retrieve-time-to-be-debt-free-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="retrieve-time-to-be-debt-free-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» end_date|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="weightless-link">Link</h1>

## Create Link Token

<a id="opIdpost-link-token"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'testtesthttps://api.weightless.com/link/token',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('testtesthttps://api.weightless.com/link/token', headers = headers)

print(r.json())

```

```javascript
const inputBody = '{
  "type": "credit"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/link/token',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "testtesthttps://api.weightless.com/link/token", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X POST testtesthttps://api.weightless.com/link/token \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

`POST /link/token`

Returns a link_token, which is required as a parameter when initializing Link. Once Link has been initialized, it returns a public_token, this should be included in a request to the /link/public_token endpoint so we can access your linked data.

> Body parameter

```json
{
  "type": "credit"
}
```

<h3 id="create-link-token-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» type|body|string|false|none|

> Example responses

> OK

```json
{
  "link_token": "link-sandbox-af1a0311-da53-4636-b754-dd15cc058176",
  "expiration": "2020-03-27T12:56:34Z"
}
```

<h3 id="create-link-token-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="create-link-token-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» link_token|string|false|none|none|
|» expiration|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Save Link Public Token

<a id="opIdpost-item-public_token"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'testtesthttps://api.weightless.com/link/public_token',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('testtesthttps://api.weightless.com/link/public_token', headers = headers)

print(r.json())

```

```javascript
const inputBody = '{
  "public_token": "public-sandbox-8ab976e6-64bc-4b38-98f7-731e7a349970"
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('testtesthttps://api.weightless.com/link/public_token',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "testtesthttps://api.weightless.com/link/public_token", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X POST testtesthttps://api.weightless.com/link/public_token \
  -H 'Content-Type: application/json'

```

`POST /link/public_token`

Save a Link public token that has been obtained from the onSuccess callback of Link. The public_token expires after 30 minutes. The public token allows us to access your linked data.

> Body parameter

```json
{
  "public_token": "public-sandbox-8ab976e6-64bc-4b38-98f7-731e7a349970"
}
```

<h3 id="save-link-public-token-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» public_token|body|string|false|none|

<h3 id="save-link-public-token-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="weightless-tips">Tips</h1>

## Retrieve Tips

<a id="opIdget-tips"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/tips',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/tips', headers = headers)

print(r.json())

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/tips',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/tips", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/tips \
  -H 'Accept: application/json'

```

`GET /tips`

Retrieve the tip of the month, detailing recommendations on how you can improve your debt repayments. 

> Example responses

> 200 Response

```json
{}
```

<h3 id="retrieve-tips-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="retrieve-tips-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="weightless-refinance">Refinance</h1>

## Retrieve refinance estimate

<a id="opIdget-refinancing"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'testtesthttps://api.weightless.com/refinance',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('testtesthttps://api.weightless.com/refinance', headers = headers)

print(r.json())

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('testtesthttps://api.weightless.com/refinance',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "testtesthttps://api.weightless.com/refinance", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

```shell
# You can also use wget
curl -X GET testtesthttps://api.weightless.com/refinance \
  -H 'Accept: application/json'

```

`GET /refinance`

> Example responses

> OK

```json
{
  "apr_percentage": 10.5,
  "fee": 25225,
  "currency": "usd"
}
```

<h3 id="retrieve-refinance-estimate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="retrieve-refinance-estimate-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» apr_percentage|number|false|none|none|
|» fee|integer|false|none|none|
|» currency|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

