---
title: EdgePortal Api v0.0.1
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="EdgePortal-Api">EdgePortal Api v0.0.1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

netIOT Edge Portal API Documentation

Base URLs:

* <a href="http://127.0.0.1:5000/v1">http://127.0.0.1:5000/v1</a>

<h1 id="EdgePortal-Api-organisations">organisations</h1>

## getOrganisations

<a id="opIdgetOrganisations"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/organisations \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/organisations HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/organisations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/organisations', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/organisations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organisations`

*Get organisations starting from an organisation id.*

<h3 id="getOrganisations-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|query|number|false|No description|
|page|query|number|false|No description|
|att|query|string|false|No description|
|sort|query|string|false|No description|
|depth|query|string|false|No description|

#### Enumerated Values

|Parameter|Value|
|---|---|
|att|id|
|att|organisationId|
|att|name|
|att|firstname|
|att|email|
|sort|asc|
|sort|desc|
|depth|one|
|depth|all|

> Example responses

<h3 id="getOrganisations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Organisation does not exist.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postOrganisations

<a id="opIdpostOrganisations"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:5000/v1/organisations \
  -H 'Content-Type: application/json' \
  -H 'authorization: string'

```

```http
POST http://127.0.0.1:5000/v1/organisations HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json

authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "parentId": 1
}';
const headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'authorization' => 'string'
}

result = RestClient.post 'http://127.0.0.1:5000/v1/organisations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'authorization': 'string'
}

r = requests.post('http://127.0.0.1:5000/v1/organisations', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:5000/v1/organisations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organisations`

*Create an organisation.*

> Body parameter

```json
{
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "parentId": 1
}
```

<h3 id="postOrganisations-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_8](#schemamodel_8)|false|No description|

<h3 id="postOrganisations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Organisation created.|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getOrganisationsId

<a id="opIdgetOrganisationsId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/organisations/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/organisations/{id} HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations/{id}',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/organisations/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/organisations/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/organisations/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organisations/{id}`

*Get organisation by id.*

<h3 id="getOrganisationsId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="getOrganisationsId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Organisation does not exist.|None|

<aside class="success">
This operation does not require authentication
</aside>

## putOrganisationsId

<a id="opIdputOrganisationsId"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT http://127.0.0.1:5000/v1/organisations/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT http://127.0.0.1:5000/v1/organisations/{id} HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json
Accept: */*
authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "parentId": 1
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations/{id}',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.put 'http://127.0.0.1:5000/v1/organisations/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.put('http://127.0.0.1:5000/v1/organisations/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "http://127.0.0.1:5000/v1/organisations/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organisations/{id}`

*Modify an organisations data.*

> Body parameter

```json
{
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "parentId": 1
}
```

<h3 id="putOrganisationsId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|body|body|[Model_2](#schemamodel_2)|false|No description|

> Example responses

<h3 id="putOrganisationsId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Organisation modified.|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteOrganisationsId

<a id="opIddeleteOrganisationsId"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE http://127.0.0.1:5000/v1/organisations/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE http://127.0.0.1:5000/v1/organisations/{id} HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations/{id}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.delete 'http://127.0.0.1:5000/v1/organisations/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.delete('http://127.0.0.1:5000/v1/organisations/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://127.0.0.1:5000/v1/organisations/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organisations/{id}`

*Delete organisation by id.*

<h3 id="deleteOrganisationsId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="deleteOrganisationsId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Organisation found and deleted.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Organisation does not exist.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getOrganisationsIdUsers

<a id="opIdgetOrganisationsIdUsers"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/organisations/{id}/users \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/organisations/{id}/users HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations/{id}/users',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations/{id}/users',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/organisations/{id}/users',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/organisations/{id}/users', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations/{id}/users");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/organisations/{id}/users", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organisations/{id}/users`

*Get users by organisation id.*

<h3 id="getOrganisationsIdUsers-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|page|query|number|false|No description|
|att|query|string|false|No description|
|sort|query|string|false|No description|
|depth|query|string|false|No description|

#### Enumerated Values

|Parameter|Value|
|---|---|
|att|id|
|att|organisationId|
|att|name|
|att|firstname|
|att|email|
|sort|asc|
|sort|desc|
|depth|one|
|depth|all|

> Example responses

<h3 id="getOrganisationsIdUsers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Organisation does not exist.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getOrganisationsIdDevices

<a id="opIdgetOrganisationsIdDevices"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/organisations/{id}/devices \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/organisations/{id}/devices HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations/{id}/devices',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations/{id}/devices',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/organisations/{id}/devices',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/organisations/{id}/devices', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations/{id}/devices");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/organisations/{id}/devices", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organisations/{id}/devices`

*Get devices by organisation id.*

<h3 id="getOrganisationsIdDevices-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|page|query|number|false|No description|
|att|query|string|false|No description|
|sort|query|string|false|No description|
|depth|query|string|false|No description|

#### Enumerated Values

|Parameter|Value|
|---|---|
|att|id|
|att|deviceId|
|att|name|
|att|productName|
|att|serialNumber|
|sort|asc|
|sort|desc|
|depth|one|
|depth|all|

> Example responses

<h3 id="getOrganisationsIdDevices-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Organisation does not exist.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getOrganisationsIdLock

<a id="opIdgetOrganisationsIdLock"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/organisations/{id}/lock \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/organisations/{id}/lock HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations/{id}/lock',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations/{id}/lock',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/organisations/{id}/lock',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/organisations/{id}/lock', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations/{id}/lock");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/organisations/{id}/lock", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organisations/{id}/lock`

*Get organisationlock.*

<h3 id="getOrganisationsIdLock-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="getOrganisationsIdLock-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Organisation not found.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postOrganisationsIdLock

<a id="opIdpostOrganisationsIdLock"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:5000/v1/organisations/{id}/lock \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST http://127.0.0.1:5000/v1/organisations/{id}/lock HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations/{id}/lock',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations/{id}/lock',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'http://127.0.0.1:5000/v1/organisations/{id}/lock',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.post('http://127.0.0.1:5000/v1/organisations/{id}/lock', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations/{id}/lock");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:5000/v1/organisations/{id}/lock", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organisations/{id}/lock`

*Lock an organisation (subtree).*

<h3 id="postOrganisationsIdLock-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="postOrganisationsIdLock-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Organisation locked.|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Organisation not found.|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Already locked or common error.|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteOrganisationsIdLock

<a id="opIddeleteOrganisationsIdLock"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE http://127.0.0.1:5000/v1/organisations/{id}/lock \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE http://127.0.0.1:5000/v1/organisations/{id}/lock HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/organisations/{id}/lock',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/organisations/{id}/lock',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.delete 'http://127.0.0.1:5000/v1/organisations/{id}/lock',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.delete('http://127.0.0.1:5000/v1/organisations/{id}/lock', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/organisations/{id}/lock");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://127.0.0.1:5000/v1/organisations/{id}/lock", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organisations/{id}/lock`

*Delete an organisationlock.*

<h3 id="deleteOrganisationsIdLock-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="deleteOrganisationsIdLock-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OrganisationLock found and deleted.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="EdgePortal-Api-devices">devices</h1>

## getDevicesId

<a id="opIdgetDevicesId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/devices/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/devices/{id} HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/devices/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/devices/{id}',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/devices/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/devices/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/devices/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/devices/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/{id}`

*Get device by id.*

<h3 id="getDevicesId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="getDevicesId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Device not found.|None|

<aside class="success">
This operation does not require authentication
</aside>

## putDevicesId

<a id="opIdputDevicesId"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT http://127.0.0.1:5000/v1/devices/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT http://127.0.0.1:5000/v1/devices/{id} HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json
Accept: */*
authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/devices/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "organisationId": 1,
  "name": "string",
  "productName": "string",
  "firmwareVersion": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/devices/{id}',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.put 'http://127.0.0.1:5000/v1/devices/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.put('http://127.0.0.1:5000/v1/devices/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/devices/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "http://127.0.0.1:5000/v1/devices/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /devices/{id}`

*Modify a devices data.*

> Body parameter

```json
{
  "organisationId": 1,
  "name": "string",
  "productName": "string",
  "firmwareVersion": "string"
}
```

<h3 id="putDevicesId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|body|body|[Model_1](#schemamodel_1)|false|No description|

> Example responses

<h3 id="putDevicesId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Device modified.|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteDevicesId

<a id="opIddeleteDevicesId"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE http://127.0.0.1:5000/v1/devices/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE http://127.0.0.1:5000/v1/devices/{id} HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/devices/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/devices/{id}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.delete 'http://127.0.0.1:5000/v1/devices/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.delete('http://127.0.0.1:5000/v1/devices/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/devices/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://127.0.0.1:5000/v1/devices/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /devices/{id}`

*Delete device by id.*

<h3 id="deleteDevicesId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="deleteDevicesId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Device found and deleted.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Device not found.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getDevicesIdSysteminformation

<a id="opIdgetDevicesIdSysteminformation"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/devices/{id}/systemInformation \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/devices/{id}/systemInformation HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/devices/{id}/systemInformation', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/devices/{id}/systemInformation");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/devices/{id}/systemInformation", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/{id}/systemInformation`

*Get systeminformation by id.*

<h3 id="getDevicesIdSysteminformation-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="getDevicesIdSysteminformation-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Device not found.|None|

<aside class="success">
This operation does not require authentication
</aside>

## putDevicesIdSysteminformation

<a id="opIdputDevicesIdSysteminformation"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT http://127.0.0.1:5000/v1/devices/{id}/systemInformation \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT http://127.0.0.1:5000/v1/devices/{id}/systemInformation HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json
Accept: */*
authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "serialNumber": "string",
  "name": "string",
  "systemTime": "string",
  "firmwareVersion": "string",
  "processorName": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.put 'http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.put('http://127.0.0.1:5000/v1/devices/{id}/systemInformation', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/devices/{id}/systemInformation");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "http://127.0.0.1:5000/v1/devices/{id}/systemInformation", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /devices/{id}/systemInformation`

*Modify a devices data.*

> Body parameter

```json
{
  "serialNumber": "string",
  "name": "string",
  "systemTime": "string",
  "firmwareVersion": "string",
  "processorName": "string"
}
```

<h3 id="putDevicesIdSysteminformation-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|body|body|[Model_6](#schemamodel_6)|false|No description|

> Example responses

<h3 id="putDevicesIdSysteminformation-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Device modified.|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postDevicesIdSysteminformation

<a id="opIdpostDevicesIdSysteminformation"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:5000/v1/devices/{id}/systemInformation \
  -H 'Content-Type: application/json' \
  -H 'authorization: string'

```

```http
POST http://127.0.0.1:5000/v1/devices/{id}/systemInformation HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json

authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "serialNumber": "string",
  "name": "string",
  "systemTime": "string",
  "firmwareVersion": "string",
  "processorName": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'authorization' => 'string'
}

result = RestClient.post 'http://127.0.0.1:5000/v1/devices/{id}/systemInformation',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'authorization': 'string'
}

r = requests.post('http://127.0.0.1:5000/v1/devices/{id}/systemInformation', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/devices/{id}/systemInformation");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:5000/v1/devices/{id}/systemInformation", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /devices/{id}/systemInformation`

*Create a systeminformation.*

> Body parameter

```json
{
  "serialNumber": "string",
  "name": "string",
  "systemTime": "string",
  "firmwareVersion": "string",
  "processorName": "string"
}
```

<h3 id="postDevicesIdSysteminformation-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|body|body|[Model_13](#schemamodel_13)|false|No description|

<h3 id="postDevicesIdSysteminformation-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Systeminformation created.|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postDevices

<a id="opIdpostDevices"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:5000/v1/devices \
  -H 'Content-Type: application/json' \
  -H 'authorization: string'

```

```http
POST http://127.0.0.1:5000/v1/devices HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json

authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/devices',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "serialNumber": "string",
  "organisationId": 1,
  "name": "string",
  "productName": "string",
  "firmwareVersion": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/devices',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'authorization' => 'string'
}

result = RestClient.post 'http://127.0.0.1:5000/v1/devices',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'authorization': 'string'
}

r = requests.post('http://127.0.0.1:5000/v1/devices', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/devices");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:5000/v1/devices", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /devices`

*Create a device.*

> Body parameter

```json
{
  "serialNumber": "string",
  "organisationId": 1,
  "name": "string",
  "productName": "string",
  "firmwareVersion": "string"
}
```

<h3 id="postDevices-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_7](#schemamodel_7)|false|No description|

<h3 id="postDevices-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Device created.|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="EdgePortal-Api-roles">roles</h1>

## getRolesName

<a id="opIdgetRolesName"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/roles/{name} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/roles/{name} HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/roles/{name}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/roles/{name}',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/roles/{name}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/roles/{name}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/roles/{name}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/roles/{name}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /roles/{name}`

*Get a role.*

<h3 id="getRolesName-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|name|path|string|true|No description|

> Example responses

<h3 id="getRolesName-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found.|None|

<aside class="success">
This operation does not require authentication
</aside>

## putRolesName

<a id="opIdputRolesName"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT http://127.0.0.1:5000/v1/roles/{name} \
  -H 'Content-Type: application/json' \
  -H 'authorization: string'

```

```http
PUT http://127.0.0.1:5000/v1/roles/{name} HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json

authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/roles/{name}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "resourcesAdd": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ],
  "resourcesDelete": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/roles/{name}',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'authorization' => 'string'
}

result = RestClient.put 'http://127.0.0.1:5000/v1/roles/{name}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'authorization': 'string'
}

r = requests.put('http://127.0.0.1:5000/v1/roles/{name}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/roles/{name}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "http://127.0.0.1:5000/v1/roles/{name}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /roles/{name}`

*Update a role.*

> Body parameter

```json
{
  "resourcesAdd": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ],
  "resourcesDelete": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ]
}
```

<h3 id="putRolesName-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|name|path|string|true|No description|
|body|body|[Model_4](#schemamodel_4)|false|No description|

<h3 id="putRolesName-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Role created.|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request.|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteRolesName

<a id="opIddeleteRolesName"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE http://127.0.0.1:5000/v1/roles/{name} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE http://127.0.0.1:5000/v1/roles/{name} HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/roles/{name}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/roles/{name}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.delete 'http://127.0.0.1:5000/v1/roles/{name}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.delete('http://127.0.0.1:5000/v1/roles/{name}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/roles/{name}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://127.0.0.1:5000/v1/roles/{name}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /roles/{name}`

*Delete role.*

<h3 id="deleteRolesName-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|name|path|string|true|No description|

> Example responses

<h3 id="deleteRolesName-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Role deleted.|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Role not found.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postRoles

<a id="opIdpostRoles"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:5000/v1/roles \
  -H 'Content-Type: application/json' \
  -H 'authorization: string'

```

```http
POST http://127.0.0.1:5000/v1/roles HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json

authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/roles',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "name": "string",
  "resources": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/roles',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'authorization' => 'string'
}

result = RestClient.post 'http://127.0.0.1:5000/v1/roles',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'authorization': 'string'
}

r = requests.post('http://127.0.0.1:5000/v1/roles', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/roles");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:5000/v1/roles", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /roles`

*Create a role.*

> Body parameter

```json
{
  "name": "string",
  "resources": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ]
}
```

<h3 id="postRoles-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_9](#schemamodel_9)|false|No description|

<h3 id="postRoles-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Role created.|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request.|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="EdgePortal-Api-users">users</h1>

Api users interface.

## getUsersResetpassword

<a id="opIdgetUsersResetpassword"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/users/reset-password \
  -H 'Accept: */*'

```

```http
GET http://127.0.0.1:5000/v1/users/reset-password HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/users/reset-password',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*'

};

fetch('http://127.0.0.1:5000/v1/users/reset-password',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/users/reset-password',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*'
}

r = requests.get('http://127.0.0.1:5000/v1/users/reset-password', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/users/reset-password");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/users/reset-password", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/reset-password`

*Reset the users password.*

> Example responses

<h3 id="getUsersResetpassword-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Password reset.|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Token invalid.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getUsersId

<a id="opIdgetUsersId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://127.0.0.1:5000/v1/users/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET http://127.0.0.1:5000/v1/users/{id} HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/users/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/users/{id}',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.get 'http://127.0.0.1:5000/v1/users/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('http://127.0.0.1:5000/v1/users/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/users/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://127.0.0.1:5000/v1/users/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/{id}`

*Get user by id.*

<h3 id="getUsersId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="getUsersId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Return data.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found.|None|

<aside class="success">
This operation does not require authentication
</aside>

## putUsersId

<a id="opIdputUsersId"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT http://127.0.0.1:5000/v1/users/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT http://127.0.0.1:5000/v1/users/{id} HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json
Accept: */*
authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/users/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string",
  "firstname": "string",
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "password": "string",
  "organisationId": 1,
  "rolesAdd": [
    "string"
  ],
  "rolesDelete": [
    "string"
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/users/{id}',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.put 'http://127.0.0.1:5000/v1/users/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.put('http://127.0.0.1:5000/v1/users/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/users/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "http://127.0.0.1:5000/v1/users/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /users/{id}`

*Modify a users data.*

> Body parameter

```json
{
  "email": "string",
  "firstname": "string",
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "password": "string",
  "organisationId": 1,
  "rolesAdd": [
    "string"
  ],
  "rolesDelete": [
    "string"
  ]
}
```

<h3 id="putUsersId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|body|body|[Model_5](#schemamodel_5)|false|No description|

> Example responses

<h3 id="putUsersId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User modified.|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found.|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteUsersId

<a id="opIddeleteUsersId"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE http://127.0.0.1:5000/v1/users/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE http://127.0.0.1:5000/v1/users/{id} HTTP/1.1
Host: 127.0.0.1:5000

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/users/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'*/*',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/users/{id}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.delete 'http://127.0.0.1:5000/v1/users/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.delete('http://127.0.0.1:5000/v1/users/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/users/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://127.0.0.1:5000/v1/users/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /users/{id}`

*Delete user by id.*

<h3 id="deleteUsersId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="deleteUsersId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User found and deleted.|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Please login.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postUsers

<a id="opIdpostUsers"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:5000/v1/users \
  -H 'Content-Type: application/json' \
  -H 'authorization: string'

```

```http
POST http://127.0.0.1:5000/v1/users HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json

authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/users',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "login": "string",
  "email": "string",
  "firstname": "string",
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "password": "string",
  "organisationId": 1,
  "roles": [
    "string"
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'authorization':'string'

};

fetch('http://127.0.0.1:5000/v1/users',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'authorization' => 'string'
}

result = RestClient.post 'http://127.0.0.1:5000/v1/users',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'authorization': 'string'
}

r = requests.post('http://127.0.0.1:5000/v1/users', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/users");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:5000/v1/users", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users`

*Create a user.*

> Body parameter

```json
{
  "login": "string",
  "email": "string",
  "firstname": "string",
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "password": "string",
  "organisationId": 1,
  "roles": [
    "string"
  ]
}
```

<h3 id="postUsers-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_10](#schemamodel_10)|false|No description|

<h3 id="postUsers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|User created.|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Bad data.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postUsersForgotpassword

<a id="opIdpostUsersForgotpassword"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:5000/v1/users/forgot-password \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'

```

```http
POST http://127.0.0.1:5000/v1/users/forgot-password HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/users/forgot-password',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'

};

fetch('http://127.0.0.1:5000/v1/users/forgot-password',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}

result = RestClient.post 'http://127.0.0.1:5000/v1/users/forgot-password',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}

r = requests.post('http://127.0.0.1:5000/v1/users/forgot-password', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/users/forgot-password");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "Accept": []string{"*/*"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:5000/v1/users/forgot-password", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/forgot-password`

*User forgot password => generate Link to reset the password.*

> Body parameter

```json
{
  "email": "string"
}
```

<h3 id="postUsersForgotpassword-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Model_11](#schemamodel_11)|false|No description|

> Example responses

<h3 id="postUsersForgotpassword-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Reset-password-link generated.|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Wrong email.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postUsersLogin

<a id="opIdpostUsersLogin"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:5000/v1/users/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'

```

```http
POST http://127.0.0.1:5000/v1/users/login HTTP/1.1
Host: 127.0.0.1:5000
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'

};

$.ajax({
  url: 'http://127.0.0.1:5000/v1/users/login',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'

};

fetch('http://127.0.0.1:5000/v1/users/login',
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

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}

result = RestClient.post 'http://127.0.0.1:5000/v1/users/login',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}

r = requests.post('http://127.0.0.1:5000/v1/users/login', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://127.0.0.1:5000/v1/users/login");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

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
        "Accept": []string{"*/*"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:5000/v1/users/login", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/login`

*Login a user.*

> Body parameter

```json
{
  "email": "string",
  "password": "string"
}
```

<h3 id="postUsersLogin-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Model_12](#schemamodel_12)|false|No description|

> Example responses

<h3 id="postUsersLogin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User logged in.|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Invalid credentials.|None|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocSpermissions">permissions</h2>

<a id="schemapermissions"></a>

```json
[
  "string"
]
```

### Properties

*None*

<h2 id="tocSresourcesadd">resourcesAdd</h2>

<a id="schemaresourcesadd"></a>

```json
[
  {
    "resource": "string",
    "permissions": [
      "string"
    ]
  }
]
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Model_3](#schemamodel_3)]|false|No description|

<h2 id="tocSrolesadd">rolesAdd</h2>

<a id="schemarolesadd"></a>

```json
[
  "string"
]
```

### Properties

*None*

<h2 id="tocSresources">resources</h2>

<a id="schemaresources"></a>

```json
[
  {
    "resource": "string",
    "permissions": [
      "string"
    ]
  }
]
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Model_3](#schemamodel_3)]|false|No description|

<h2 id="tocSmodel_1">Model_1</h2>

<a id="schemamodel_1"></a>

```json
{
  "organisationId": 1,
  "name": "string",
  "productName": "string",
  "firmwareVersion": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|organisationId|number|false|No description|
|name|string|false|No description|
|productName|string|false|No description|
|firmwareVersion|string|false|No description|

<h2 id="tocSmodel_2">Model_2</h2>

<a id="schemamodel_2"></a>

```json
{
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "parentId": 1
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|name|string|false|No description|
|phoneNumber|string|false|No description|
|street|string|false|No description|
|zipCode|string|false|No description|
|city|string|false|No description|
|parentId|number|false|No description|

<h2 id="tocSmodel_3">Model_3</h2>

<a id="schemamodel_3"></a>

```json
{
  "resource": "string",
  "permissions": [
    "string"
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|resource|string|true|No description|
|permissions|[permissions](#schemapermissions)|false|No description|

<h2 id="tocSmodel_4">Model_4</h2>

<a id="schemamodel_4"></a>

```json
{
  "resourcesAdd": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ],
  "resourcesDelete": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|resourcesAdd|[resourcesAdd](#schemaresourcesadd)|false|No description|
|resourcesDelete|[resourcesAdd](#schemaresourcesadd)|false|No description|

<h2 id="tocSmodel_5">Model_5</h2>

<a id="schemamodel_5"></a>

```json
{
  "email": "string",
  "firstname": "string",
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "password": "string",
  "organisationId": 1,
  "rolesAdd": [
    "string"
  ],
  "rolesDelete": [
    "string"
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|email|string|false|No description|
|firstname|string|false|No description|
|name|string|false|No description|
|phoneNumber|string|false|No description|
|street|string|false|No description|
|zipCode|string|false|No description|
|city|string|false|No description|
|password|string|false|No description|
|organisationId|number|false|No description|
|rolesAdd|[rolesAdd](#schemarolesadd)|false|No description|
|rolesDelete|[rolesAdd](#schemarolesadd)|false|No description|

<h2 id="tocSmodel_6">Model_6</h2>

<a id="schemamodel_6"></a>

```json
{
  "serialNumber": "string",
  "name": "string",
  "systemTime": "string",
  "firmwareVersion": "string",
  "processorName": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|serialNumber|string|false|No description|
|name|string|false|No description|
|systemTime|string|false|No description|
|firmwareVersion|string|false|No description|
|processorName|string|false|No description|

<h2 id="tocSmodel_7">Model_7</h2>

<a id="schemamodel_7"></a>

```json
{
  "serialNumber": "string",
  "organisationId": 1,
  "name": "string",
  "productName": "string",
  "firmwareVersion": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|serialNumber|string|true|No description|
|organisationId|number|true|No description|
|name|string|false|No description|
|productName|string|false|No description|
|firmwareVersion|string|false|No description|

<h2 id="tocSmodel_8">Model_8</h2>

<a id="schemamodel_8"></a>

```json
{
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "parentId": 1
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|name|string|true|No description|
|phoneNumber|string|true|No description|
|street|string|true|No description|
|zipCode|string|true|No description|
|city|string|true|No description|
|parentId|number|true|No description|

<h2 id="tocSmodel_9">Model_9</h2>

<a id="schemamodel_9"></a>

```json
{
  "name": "string",
  "resources": [
    {
      "resource": "string",
      "permissions": [
        "string"
      ]
    }
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|name|string|true|No description|
|resources|[resources](#schemaresources)|false|No description|

<h2 id="tocSmodel_10">Model_10</h2>

<a id="schemamodel_10"></a>

```json
{
  "login": "string",
  "email": "string",
  "firstname": "string",
  "name": "string",
  "phoneNumber": "string",
  "street": "string",
  "zipCode": "string",
  "city": "string",
  "password": "string",
  "organisationId": 1,
  "roles": [
    "string"
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|login|string|true|No description|
|email|string|true|No description|
|firstname|string|true|No description|
|name|string|true|No description|
|phoneNumber|string|true|No description|
|street|string|true|No description|
|zipCode|string|true|No description|
|city|string|true|No description|
|password|string|true|No description|
|organisationId|number|true|No description|
|roles|[rolesAdd](#schemarolesadd)|false|No description|

<h2 id="tocSmodel_11">Model_11</h2>

<a id="schemamodel_11"></a>

```json
{
  "email": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|

<h2 id="tocSmodel_12">Model_12</h2>

<a id="schemamodel_12"></a>

```json
{
  "email": "string",
  "password": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|
|password|string|true|No description|

<h2 id="tocSmodel_13">Model_13</h2>

<a id="schemamodel_13"></a>

```json
{
  "serialNumber": "string",
  "name": "string",
  "systemTime": "string",
  "firmwareVersion": "string",
  "processorName": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|serialNumber|string|true|No description|
|name|string|false|No description|
|systemTime|string|false|No description|
|firmwareVersion|string|false|No description|
|processorName|string|false|No description|

