---
title: netIOT DI-Portal API Documentation v1.2.1978
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

<h1 id="netIOT-DI-Portal-API-Documentation">netIOT DI-Portal API Documentation v1.2.1978</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="https://api.di-portal.com/v2">https://api.di-portal.com/v2</a>

# Authentication

* API Key (api_key)
    - Parameter Name: **api_key**, in: header. 

* API Key (jwt)
    - Parameter Name: **Authorization**, in: header. 

<h1 id="netIOT-DI-Portal-API-Documentation-apiKeys">apiKeys</h1>

## getApikeys

<a id="opIdgetApikeys"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/apiKeys \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/apiKeys HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/apiKeys',
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

fetch('https://api.di-portal.com/v2/apiKeys',
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

result = RestClient.get 'https://api.di-portal.com/v2/apiKeys',
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

r = requests.get('https://api.di-portal.com/v2/apiKeys', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/apiKeys");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/apiKeys", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /apiKeys`

*Retrieve list of API Key from User*

<h3 id="getApikeys-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|userId|query|integer|false|No description|

> Example responses

<h3 id="getApikeys-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getApikeysRequests

<a id="opIdgetApikeysRequests"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/apiKeys/requests \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/apiKeys/requests HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/apiKeys/requests',
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

fetch('https://api.di-portal.com/v2/apiKeys/requests',
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

result = RestClient.get 'https://api.di-portal.com/v2/apiKeys/requests',
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

r = requests.get('https://api.di-portal.com/v2/apiKeys/requests', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/apiKeys/requests");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/apiKeys/requests", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /apiKeys/requests`

*Retrieve list of API Key Request*

<h3 id="getApikeysRequests-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|userId|query|integer|false|No description|

> Example responses

<h3 id="getApikeysRequests-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postApikeysRequests

<a id="opIdpostApikeysRequests"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/apiKeys/requests \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/apiKeys/requests HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/apiKeys/requests',
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
  "keyType": "frontend",
  "httpRef": "string",
  "host": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/apiKeys/requests',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/apiKeys/requests',
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

r = requests.post('https://api.di-portal.com/v2/apiKeys/requests', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/apiKeys/requests");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/apiKeys/requests", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /apiKeys/requests`

*Send API Key Request*

> Body parameter

```json
{
  "keyType": "frontend",
  "httpRef": "string",
  "host": "string"
}
```

<h3 id="postApikeysRequests-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_6](#schemamodel_6)|false|No description|

> Example responses

<h3 id="postApikeysRequests-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getApikeysRequestsRequestid

<a id="opIdgetApikeysRequestsRequestid"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/apiKeys/requests/{requestId} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/apiKeys/requests/{requestId} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/apiKeys/requests/{requestId}',
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

fetch('https://api.di-portal.com/v2/apiKeys/requests/{requestId}',
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

result = RestClient.get 'https://api.di-portal.com/v2/apiKeys/requests/{requestId}',
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

r = requests.get('https://api.di-portal.com/v2/apiKeys/requests/{requestId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/apiKeys/requests/{requestId}");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/apiKeys/requests/{requestId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /apiKeys/requests/{requestId}`

*Get API Key Request by id*

<h3 id="getApikeysRequestsRequestid-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|requestId|path|integer|true|Id of the API key request|

> Example responses

<h3 id="getApikeysRequestsRequestid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## putApikeysRequestsRequestid

<a id="opIdputApikeysRequestsRequestid"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://api.di-portal.com/v2/apiKeys/requests/{requestId}?status=accepted \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT https://api.di-portal.com/v2/apiKeys/requests/{requestId}?status=accepted HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/apiKeys/requests/{requestId}',
  method: 'put',
  data: '?status=accepted',
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

fetch('https://api.di-portal.com/v2/apiKeys/requests/{requestId}?status=accepted',
{
  method: 'PUT',

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

result = RestClient.put 'https://api.di-portal.com/v2/apiKeys/requests/{requestId}',
  params: {
  'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.put('https://api.di-portal.com/v2/apiKeys/requests/{requestId}', params={
  'status': 'accepted'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/apiKeys/requests/{requestId}?status=accepted");
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
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://api.di-portal.com/v2/apiKeys/requests/{requestId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /apiKeys/requests/{requestId}`

*Update API Key information*

<h3 id="putApikeysRequestsRequestid-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|requestId|path|integer|true|Id of the API key request|
|status|query|string|true|No description|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|accepted|
|status|rejected|

> Example responses

<h3 id="putApikeysRequestsRequestid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## deleteApikeysApikeyid

<a id="opIddeleteApikeysApikeyid"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.di-portal.com/v2/apiKeys/{apiKeyId} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE https://api.di-portal.com/v2/apiKeys/{apiKeyId} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/apiKeys/{apiKeyId}',
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

fetch('https://api.di-portal.com/v2/apiKeys/{apiKeyId}',
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

result = RestClient.delete 'https://api.di-portal.com/v2/apiKeys/{apiKeyId}',
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

r = requests.delete('https://api.di-portal.com/v2/apiKeys/{apiKeyId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/apiKeys/{apiKeyId}");
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
    req, err := http.NewRequest("DELETE", "https://api.di-portal.com/v2/apiKeys/{apiKeyId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /apiKeys/{apiKeyId}`

*Delete an API Key*

<h3 id="deleteApikeysApikeyid-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|apiKeyId|path|integer|true|Id of the API key|

> Example responses

<h3 id="deleteApikeysApikeyid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## deleteApikeysRequestsApikeyrequestid

<a id="opIddeleteApikeysRequestsApikeyrequestid"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.di-portal.com/v2/apiKeys/requests/{apiKeyRequestId} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE https://api.di-portal.com/v2/apiKeys/requests/{apiKeyRequestId} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/apiKeys/requests/{apiKeyRequestId}',
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

fetch('https://api.di-portal.com/v2/apiKeys/requests/{apiKeyRequestId}',
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

result = RestClient.delete 'https://api.di-portal.com/v2/apiKeys/requests/{apiKeyRequestId}',
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

r = requests.delete('https://api.di-portal.com/v2/apiKeys/requests/{apiKeyRequestId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/apiKeys/requests/{apiKeyRequestId}");
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
    req, err := http.NewRequest("DELETE", "https://api.di-portal.com/v2/apiKeys/requests/{apiKeyRequestId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /apiKeys/requests/{apiKeyRequestId}`

*Delete API Key Request*

<h3 id="deleteApikeysRequestsApikeyrequestid-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|apiKeyRequestId|path|integer|true|Id of the API key request|

> Example responses

<h3 id="deleteApikeysRequestsApikeyrequestid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-networks">networks</h1>

## getNetworks

<a id="opIdgetNetworks"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/networks \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/networks HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/networks',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/networks',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/networks',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/networks', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/networks");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/networks", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /networks`

*Returns a list of all network types, this includes search fields and item columns*

> Example responses

<h3 id="getNetworks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-search">search</h1>

## getSearch

<a id="opIdgetSearch"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/search \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/search HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/search',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/search',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/search");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /search`

*Search over all published products*

Use lucene syntax to filter for products.

<h3 id="getSearch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|search|query|string|false|No description|
|searchType|query|string|false|No description|
|filter|query|string|false|No description|
|orderBy|query|string|false|No description|
|skip|query|integer|false|Number of elements to skip for pagination|

> Example responses

<h3 id="getSearch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-terms">terms</h1>

## getTerms

<a id="opIdgetTerms"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/terms \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/terms HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/terms',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/terms',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/terms',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/terms', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/terms");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/terms", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /terms`

*Get the latest terms and conditions*

> Example responses

<h3 id="getTerms-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postTerms

<a id="opIdpostTerms"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/terms \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/terms HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/terms',
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
  "translations": [
    {
      "content": "string",
      "language": "de"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/terms',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/terms',
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

r = requests.post('https://api.di-portal.com/v2/terms', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/terms");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/terms", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /terms`

*Create a new version of the terms and conditions*

> Body parameter

```json
{
  "translations": [
    {
      "content": "string",
      "language": "de"
    }
  ]
}
```

<h3 id="postTerms-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_3](#schemamodel_3)|false|No description|

> Example responses

<h3 id="postTerms-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## deleteTermsTermsid

<a id="opIddeleteTermsTermsid"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.di-portal.com/v2/terms/{termsId} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE https://api.di-portal.com/v2/terms/{termsId} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/terms/{termsId}',
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

fetch('https://api.di-portal.com/v2/terms/{termsId}',
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

result = RestClient.delete 'https://api.di-portal.com/v2/terms/{termsId}',
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

r = requests.delete('https://api.di-portal.com/v2/terms/{termsId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/terms/{termsId}");
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
    req, err := http.NewRequest("DELETE", "https://api.di-portal.com/v2/terms/{termsId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /terms/{termsId}`

*Entirely delete a Terms entry with a given termsId*

<h3 id="deleteTermsTermsid-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|termsId|path|number|true|No description|

> Example responses

<h3 id="deleteTermsTermsid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-vendors">vendors</h1>

## getVendors

<a id="opIdgetVendors"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/vendors \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/vendors HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/vendors',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/vendors',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/vendors',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/vendors', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/vendors");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/vendors", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /vendors`

*Get a list of Vendors*

<h3 id="getVendors-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|networkTypeId|query|integer|false|No description|

> Example responses

<h3 id="getVendors-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getVendorsUserid

<a id="opIdgetVendorsUserid"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/vendors/{userId} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/vendors/{userId} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/vendors/{userId}',
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

fetch('https://api.di-portal.com/v2/vendors/{userId}',
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

result = RestClient.get 'https://api.di-portal.com/v2/vendors/{userId}',
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

r = requests.get('https://api.di-portal.com/v2/vendors/{userId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/vendors/{userId}");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/vendors/{userId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /vendors/{userId}`

*Get all information about a vendor*

<h3 id="getVendorsUserid-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|false|No description|
|userId|path|integer|true|No description|

> Example responses

<h3 id="getVendorsUserid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-categories">categories</h1>

## getCategoriesDevices

<a id="opIdgetCategoriesDevices"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/categories/devices \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/categories/devices HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/categories/devices',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/categories/devices',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/categories/devices',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/categories/devices', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/categories/devices");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/categories/devices", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /categories/devices`

*Retrieve list of device categories*

> Example responses

<h3 id="getCategoriesDevices-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getCategoriesExternallinks

<a id="opIdgetCategoriesExternallinks"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/categories/externalLinks \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/categories/externalLinks HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/categories/externalLinks',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/categories/externalLinks',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/categories/externalLinks',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/categories/externalLinks', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/categories/externalLinks");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/categories/externalLinks", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /categories/externalLinks`

*Retrieve list of file categories*

> Example responses

<h3 id="getCategoriesExternallinks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getCategoriesFiles

<a id="opIdgetCategoriesFiles"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/categories/files \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/categories/files HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/categories/files',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/categories/files',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/categories/files',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/categories/files', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/categories/files");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/categories/files", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /categories/files`

*Retrieve list of file categories*

> Example responses

<h3 id="getCategoriesFiles-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-devices">devices</h1>

## getDevicesList

<a id="opIdgetDevicesList"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/devices/list \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/devices/list HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/devices/list',
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

fetch('https://api.di-portal.com/v2/devices/list',
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

result = RestClient.get 'https://api.di-portal.com/v2/devices/list',
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

r = requests.get('https://api.di-portal.com/v2/devices/list', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/list");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/devices/list", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/list`

*Returns a list of devices from store*

Use lucene syntax to filter for devices.

<h3 id="getDevicesList-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|false|No description|
|search|query|string|false|No description|
|searchType|query|string|false|No description|
|networkTypeId|query|integer|false|Network type supported by portal|
|filter|query|string|false|No description|
|orderBy|query|string|false|No description|
|skip|query|integer|false|Number of elements to skip for pagination|

> Example responses

<h3 id="getDevicesList-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getDevicesReparsedevices

<a id="opIdgetDevicesReparsedevices"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/devices/reparseDevices?networkTypeId=1 \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/devices/reparseDevices?networkTypeId=1 HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/devices/reparseDevices',
  method: 'get',
  data: '?networkTypeId=1',
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

fetch('https://api.di-portal.com/v2/devices/reparseDevices?networkTypeId=1',
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

result = RestClient.get 'https://api.di-portal.com/v2/devices/reparseDevices',
  params: {
  'networkTypeId' => 'integer'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('https://api.di-portal.com/v2/devices/reparseDevices', params={
  'networkTypeId': '1'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/reparseDevices?networkTypeId=1");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/devices/reparseDevices", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/reparseDevices`

*Returns a list of devices from store*

Re-parsing all files for the given Networktype id

<h3 id="getDevicesReparsedevices-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|false|No description|
|networkTypeId|query|integer|true|Network type supported by portal|
|skip|query|integer|false|Network type supported by portal|

> Example responses

<h3 id="getDevicesReparsedevices-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getDevicesSuggest

<a id="opIdgetDevicesSuggest"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/devices/suggest?networkTypeId=1 \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/devices/suggest?networkTypeId=1 HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/devices/suggest',
  method: 'get',
  data: '?networkTypeId=1',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/devices/suggest?networkTypeId=1',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/devices/suggest',
  params: {
  'networkTypeId' => 'integer'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/devices/suggest', params={
  'networkTypeId': '1'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/suggest?networkTypeId=1");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/devices/suggest", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/suggest`

*Provides suggestions for search input*

<h3 id="getDevicesSuggest-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|search|query|string|false|No description|
|searchType|query|string|false|No description|
|networkTypeId|query|integer|true|Network type supported by portal|

> Example responses

<h3 id="getDevicesSuggest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getDevicesId

<a id="opIdgetDevicesId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/devices/{id} \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/devices/{id} HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/devices/{id}',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/devices/{id}',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/devices/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/devices/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/{id}");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/devices/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/{id}`

*Returns a device from store*

<h3 id="getDevicesId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|No description|

> Example responses

<h3 id="getDevicesId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getDevicesIdVersions

<a id="opIdgetDevicesIdVersions"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/devices/{id}/versions \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/devices/{id}/versions HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/devices/{id}/versions',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/devices/{id}/versions',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/devices/{id}/versions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/devices/{id}/versions', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/{id}/versions");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/devices/{id}/versions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/{id}/versions`

*Retrieve list of device versions*

<h3 id="getDevicesIdVersions-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|No description|

> Example responses

<h3 id="getDevicesIdVersions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getDevicesIdExternallinks

<a id="opIdgetDevicesIdExternallinks"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/devices/{id}/externalLinks \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/devices/{id}/externalLinks HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/devices/{id}/externalLinks',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/devices/{id}/externalLinks',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/devices/{id}/externalLinks',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/devices/{id}/externalLinks', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/{id}/externalLinks");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/devices/{id}/externalLinks", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/{id}/externalLinks`

*Gets a list of all external links on this device*

<h3 id="getDevicesIdExternallinks-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|Id of the device to add external links to|

> Example responses

<h3 id="getDevicesIdExternallinks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postDevicesIdExternallinks

<a id="opIdpostDevicesIdExternallinks"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/devices/{id}/externalLinks \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/devices/{id}/externalLinks HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/devices/{id}/externalLinks',
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
  "externalLinks": [
    {
      "name": "string",
      "url": "string",
      "categoryId": "001",
      "isLink": true
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/devices/{id}/externalLinks',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/devices/{id}/externalLinks',
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

r = requests.post('https://api.di-portal.com/v2/devices/{id}/externalLinks', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/{id}/externalLinks");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/devices/{id}/externalLinks", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /devices/{id}/externalLinks`

*Add external links to a device*

> Body parameter

```json
{
  "externalLinks": [
    {
      "name": "string",
      "url": "string",
      "categoryId": "001",
      "isLink": true
    }
  ]
}
```

<h3 id="postDevicesIdExternallinks-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|Id of the device to add external links to|
|body|body|[Model_18](#schemamodel_18)|false|No description|

> Example responses

<h3 id="postDevicesIdExternallinks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## deleteDevicesIdExternallinks

<a id="opIddeleteDevicesIdExternallinks"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.di-portal.com/v2/devices/{id}/externalLinks \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE https://api.di-portal.com/v2/devices/{id}/externalLinks HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/devices/{id}/externalLinks',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "externalLinkIds": [
    "string"
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/devices/{id}/externalLinks',
{
  method: 'DELETE',
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

result = RestClient.delete 'https://api.di-portal.com/v2/devices/{id}/externalLinks',
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

r = requests.delete('https://api.di-portal.com/v2/devices/{id}/externalLinks', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/{id}/externalLinks");
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
        "Content-Type": []string{"application/json"},
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://api.di-portal.com/v2/devices/{id}/externalLinks", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /devices/{id}/externalLinks`

*Remove external links from a device*

> Body parameter

```json
{
  "externalLinkIds": [
    "string"
  ]
}
```

<h3 id="deleteDevicesIdExternallinks-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|Id of the device to remove external links from|
|body|body|[Model_21](#schemamodel_21)|false|No description|

> Example responses

<h3 id="deleteDevicesIdExternallinks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getDevicesIdProtocolspecificinfo

<a id="opIdgetDevicesIdProtocolspecificinfo"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/devices/{id}/protocolSpecificInfo \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/devices/{id}/protocolSpecificInfo HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/devices/{id}/protocolSpecificInfo',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/devices/{id}/protocolSpecificInfo',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/devices/{id}/protocolSpecificInfo',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/devices/{id}/protocolSpecificInfo', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/{id}/protocolSpecificInfo");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/devices/{id}/protocolSpecificInfo", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /devices/{id}/protocolSpecificInfo`

*Returns protocolspecific information for a device*

<h3 id="getDevicesIdProtocolspecificinfo-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|No description|

> Example responses

<h3 id="getDevicesIdProtocolspecificinfo-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postDevicesDeviceidAdditionalfile

<a id="opIdpostDevicesDeviceidAdditionalfile"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/devices/{deviceId}/additionalfile?categoryId=001 \
  -H 'Content-Type: multipart/form-data' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/devices/{deviceId}/additionalfile?categoryId=001 HTTP/1.1
Host: api.di-portal.com
Content-Type: multipart/form-data
Accept: */*
authorization: string

```

```javascript
var headers = {
  'Content-Type':'multipart/form-data',
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/devices/{deviceId}/additionalfile',
  method: 'post',
  data: '?categoryId=001',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "file": "string"
}';
const headers = {
  'Content-Type':'multipart/form-data',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/devices/{deviceId}/additionalfile?categoryId=001',
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
  'Content-Type' => 'multipart/form-data',
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/devices/{deviceId}/additionalfile',
  params: {
  'categoryId' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'multipart/form-data',
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.post('https://api.di-portal.com/v2/devices/{deviceId}/additionalfile', params={
  'categoryId': '001'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/devices/{deviceId}/additionalfile?categoryId=001");
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
        "Content-Type": []string{"multipart/form-data"},
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/devices/{deviceId}/additionalfile", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /devices/{deviceId}/additionalfile`

*Upload an additional file*

> Body parameter

```yaml
file: string

```

<h3 id="postDevicesDeviceidAdditionalfile-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|deviceId|path|string|true|No description|
|categoryId|query|string|true|No description|
|body|body|object|false|No description|
|» file|body|string(binary)|true|Additional file|

#### Enumerated Values

|Parameter|Value|
|---|---|
|categoryId|001|
|categoryId|002|
|categoryId|003|
|categoryId|004|
|categoryId|005|
|categoryId|006|

> Example responses

<h3 id="postDevicesDeviceidAdditionalfile-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-files">files</h1>

## getFilesId

<a id="opIdgetFilesId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/files/{id}?file=string \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/files/{id}?file=string HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/files/{id}',
  method: 'get',
  data: '?file=string',
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

fetch('https://api.di-portal.com/v2/files/{id}?file=string',
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

result = RestClient.get 'https://api.di-portal.com/v2/files/{id}',
  params: {
  'file' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('https://api.di-portal.com/v2/files/{id}', params={
  'file': 'string'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/files/{id}?file=string");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/files/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /files/{id}`

*Returns a file that belongs to a device*

<h3 id="getFilesId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|false|Add auth header for logged-in user|
|id|path|string|true|No description|
|file|query|string|true|No description|
|format|query|string|false|No description|

#### Enumerated Values

|Parameter|Value|
|---|---|
|format|base64|

> Example responses

<h3 id="getFilesId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-logos">logos</h1>

## getLogosUsagerights

<a id="opIdgetLogosUsagerights"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/logos/usageRights \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/logos/usageRights HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/logos/usageRights',
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

fetch('https://api.di-portal.com/v2/logos/usageRights',
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

result = RestClient.get 'https://api.di-portal.com/v2/logos/usageRights',
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

r = requests.get('https://api.di-portal.com/v2/logos/usageRights', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/logos/usageRights");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/logos/usageRights", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /logos/usageRights`

*Gets a list of all Logo Usage Rights a user has granted*

<h3 id="getLogosUsagerights-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|false|No description|
|onlyLatest|query|boolean|false|No description|

> Example responses

<h3 id="getLogosUsagerights-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postLogosUsagerights

<a id="opIdpostLogosUsagerights"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/logos/usageRights \
  -H 'Content-Type: multipart/form-data' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/logos/usageRights HTTP/1.1
Host: api.di-portal.com
Content-Type: multipart/form-data
Accept: */*
authorization: string

```

```javascript
var headers = {
  'Content-Type':'multipart/form-data',
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/logos/usageRights',
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
  "username": "string",
  "password": "string",
  "forDIP": true,
  "forPublications": true,
  "forPromotional": true,
  "forTradeShows": true,
  "forDigitalAndPrinted": true,
  "annotations": "string",
  "file": "string"
}';
const headers = {
  'Content-Type':'multipart/form-data',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/logos/usageRights',
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
  'Content-Type' => 'multipart/form-data',
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/logos/usageRights',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'multipart/form-data',
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.post('https://api.di-portal.com/v2/logos/usageRights', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/logos/usageRights");
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
        "Content-Type": []string{"multipart/form-data"},
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/logos/usageRights", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /logos/usageRights`

*Adds a Logo Usage Right to a user and revokes old Logo Usage Rights*

> Body parameter

```yaml
username: string
password: string
forDIP: true
forPublications: true
forPromotional: true
forTradeShows: true
forDigitalAndPrinted: true
annotations: string
file: string

```

<h3 id="postLogosUsagerights-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|object|false|No description|
|» username|body|string|true|No description|
|» password|body|string|true|No description|
|» forDIP|body|boolean|true|No description|
|» forPublications|body|boolean|true|No description|
|» forPromotional|body|boolean|true|No description|
|» forTradeShows|body|boolean|true|No description|
|» forDigitalAndPrinted|body|boolean|true|No description|
|» annotations|body|string|true|No description|
|» file|body|string(binary)|true|No description|

> Example responses

<h3 id="postLogosUsagerights-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## putLogosUsagerights

<a id="opIdputLogosUsagerights"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://api.di-portal.com/v2/logos/usageRights?logoUsageRightsId=string&status=DENIED \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT https://api.di-portal.com/v2/logos/usageRights?logoUsageRightsId=string&status=DENIED HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/logos/usageRights',
  method: 'put',
  data: '?logoUsageRightsId=string&status=DENIED',
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

fetch('https://api.di-portal.com/v2/logos/usageRights?logoUsageRightsId=string&status=DENIED',
{
  method: 'PUT',

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

result = RestClient.put 'https://api.di-portal.com/v2/logos/usageRights',
  params: {
  'logoUsageRightsId' => 'string',
'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.put('https://api.di-portal.com/v2/logos/usageRights', params={
  'logoUsageRightsId': 'string',  'status': 'DENIED'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/logos/usageRights?logoUsageRightsId=string&status=DENIED");
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
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://api.di-portal.com/v2/logos/usageRights", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /logos/usageRights`

*Updates the status of a logo usage rights entry*

<h3 id="putLogosUsagerights-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|logoUsageRightsId|query|string|true|No description|
|status|query|string|true|No description|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|ACCEPTED|
|status|DENIED|

> Example responses

<h3 id="putLogosUsagerights-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getLogosLogoid

<a id="opIdgetLogosLogoid"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/logos/{logoId} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/logos/{logoId} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/logos/{logoId}',
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

fetch('https://api.di-portal.com/v2/logos/{logoId}',
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

result = RestClient.get 'https://api.di-portal.com/v2/logos/{logoId}',
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

r = requests.get('https://api.di-portal.com/v2/logos/{logoId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/logos/{logoId}");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/logos/{logoId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /logos/{logoId}`

*Download a logo*

<h3 id="getLogosLogoid-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|false|No description|
|logoId|path|string|true|No description|

> Example responses

<h3 id="getLogosLogoid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getLogosAdminUsagerights

<a id="opIdgetLogosAdminUsagerights"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/logos/admin/usageRights \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/logos/admin/usageRights HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/logos/admin/usageRights',
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

fetch('https://api.di-portal.com/v2/logos/admin/usageRights',
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

result = RestClient.get 'https://api.di-portal.com/v2/logos/admin/usageRights',
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

r = requests.get('https://api.di-portal.com/v2/logos/admin/usageRights', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/logos/admin/usageRights");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/logos/admin/usageRights", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /logos/admin/usageRights`

*Get a list of all logo usage rights over all users and statuses*

<h3 id="getLogosAdminUsagerights-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|status|query|string|false|No description|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|ACCEPTED|
|status|DENIED|
|status|PENDING|
|status|REVOKED|

> Example responses

<h3 id="getLogosAdminUsagerights-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-products">products</h1>

## getProductsList

<a id="opIdgetProductsList"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/products/list?networkTypeId=1 \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/products/list?networkTypeId=1 HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/products/list',
  method: 'get',
  data: '?networkTypeId=1',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/products/list?networkTypeId=1',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/products/list',
  params: {
  'networkTypeId' => 'integer'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/products/list', params={
  'networkTypeId': '1'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/products/list?networkTypeId=1");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/products/list", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /products/list`

*Returns a list of products from store*

Use lucene syntax to filter for products.

<h3 id="getProductsList-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|search|query|string|false|No description|
|searchType|query|string|false|No description|
|networkTypeId|query|integer|true|Network type supported by portal|
|filter|query|string|false|No description|
|orderBy|query|string|false|No description|
|skip|query|integer|false|Number of elements to skip for pagination|

> Example responses

<h3 id="getProductsList-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getProductsSuggest

<a id="opIdgetProductsSuggest"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/products/suggest \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/products/suggest HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/products/suggest',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/products/suggest',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/products/suggest',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/products/suggest', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/products/suggest");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/products/suggest", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /products/suggest`

*Provides suggestions for search input*

<h3 id="getProductsSuggest-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|search|query|string|false|No description|
|searchType|query|string|false|No description|
|networkTypeId|query|integer|false|Network type supported by portal|

> Example responses

<h3 id="getProductsSuggest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getProductsId

<a id="opIdgetProductsId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/products/{id} \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/products/{id} HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/products/{id}',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/products/{id}',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/products/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/products/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/products/{id}");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/products/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /products/{id}`

*Returns a product from store*

<h3 id="getProductsId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|No description|

> Example responses

<h3 id="getProductsId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getProductsIdExternallinks

<a id="opIdgetProductsIdExternallinks"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/products/{id}/externalLinks \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/products/{id}/externalLinks HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/products/{id}/externalLinks',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/products/{id}/externalLinks',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/products/{id}/externalLinks',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/products/{id}/externalLinks', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/products/{id}/externalLinks");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/products/{id}/externalLinks", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /products/{id}/externalLinks`

*Gets a list of all external links associated to the product and it's device*

<h3 id="getProductsIdExternallinks-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|No description|

> Example responses

<h3 id="getProductsIdExternallinks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postProductsIdExternallinks

<a id="opIdpostProductsIdExternallinks"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/products/{id}/externalLinks \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/products/{id}/externalLinks HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/products/{id}/externalLinks',
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
  "externalLinks": [
    {
      "name": "string",
      "url": "string",
      "categoryId": "001",
      "isLink": true
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/products/{id}/externalLinks',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/products/{id}/externalLinks',
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

r = requests.post('https://api.di-portal.com/v2/products/{id}/externalLinks', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/products/{id}/externalLinks");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/products/{id}/externalLinks", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /products/{id}/externalLinks`

*Add external links to a product*

> Body parameter

```json
{
  "externalLinks": [
    {
      "name": "string",
      "url": "string",
      "categoryId": "001",
      "isLink": true
    }
  ]
}
```

<h3 id="postProductsIdExternallinks-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|body|body|[Model_18](#schemamodel_18)|false|No description|

> Example responses

<h3 id="postProductsIdExternallinks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## deleteProductsIdExternallinks

<a id="opIddeleteProductsIdExternallinks"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.di-portal.com/v2/products/{id}/externalLinks \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE https://api.di-portal.com/v2/products/{id}/externalLinks HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/products/{id}/externalLinks',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "externalLinkIds": [
    "string"
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/products/{id}/externalLinks',
{
  method: 'DELETE',
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

result = RestClient.delete 'https://api.di-portal.com/v2/products/{id}/externalLinks',
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

r = requests.delete('https://api.di-portal.com/v2/products/{id}/externalLinks', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/products/{id}/externalLinks");
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
        "Content-Type": []string{"application/json"},
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://api.di-portal.com/v2/products/{id}/externalLinks", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /products/{id}/externalLinks`

*Remove external links from a product*

> Body parameter

```json
{
  "externalLinkIds": [
    "string"
  ]
}
```

<h3 id="deleteProductsIdExternallinks-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|body|body|[Model_21](#schemamodel_21)|false|No description|

> Example responses

<h3 id="deleteProductsIdExternallinks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getProductsIdVersions

<a id="opIdgetProductsIdVersions"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/products/{id}/versions \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/products/{id}/versions HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/products/{id}/versions',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/products/{id}/versions',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/products/{id}/versions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/products/{id}/versions', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/products/{id}/versions");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/products/{id}/versions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /products/{id}/versions`

*Retrieve list of product versions*

<h3 id="getProductsIdVersions-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|No description|

> Example responses

<h3 id="getProductsIdVersions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-tokens">tokens</h1>

## getTokensRefresh

<a id="opIdgetTokensRefresh"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/tokens/refresh \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/tokens/refresh HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/tokens/refresh',
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

fetch('https://api.di-portal.com/v2/tokens/refresh',
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

result = RestClient.get 'https://api.di-portal.com/v2/tokens/refresh',
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

r = requests.get('https://api.di-portal.com/v2/tokens/refresh', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/tokens/refresh");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/tokens/refresh", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /tokens/refresh`

*Returns a list of all network types, this includes search fields and item columns*

<h3 id="getTokensRefresh-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|rememberMe|path|boolean|true|No description|

> Example responses

<h3 id="getTokensRefresh-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-users">users</h1>

## getUsersEmailconfirmation

<a id="opIdgetUsersEmailconfirmation"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/users/emailConfirmation?token=string \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
GET https://api.di-portal.com/v2/users/emailConfirmation?token=string HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/emailConfirmation',
  method: 'get',
  data: '?token=string',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/users/emailConfirmation?token=string',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'https://api.di-portal.com/v2/users/emailConfirmation',
  params: {
  'token' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.get('https://api.di-portal.com/v2/users/emailConfirmation', params={
  'token': 'string'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/emailConfirmation?token=string");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/users/emailConfirmation", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/emailConfirmation`

*E-Mail confirmation*

<h3 id="getUsersEmailconfirmation-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|No description|

> Example responses

<h3 id="getUsersEmailconfirmation-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getUsersList

<a id="opIdgetUsersList"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/users/list \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/users/list HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/list',
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

fetch('https://api.di-portal.com/v2/users/list',
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

result = RestClient.get 'https://api.di-portal.com/v2/users/list',
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

r = requests.get('https://api.di-portal.com/v2/users/list', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/list");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/users/list", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/list`

*Get user profile by id*

<h3 id="getUsersList-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|filter|query|string|false|No description|
|orderBy|query|string|false|No description|

> Example responses

<h3 id="getUsersList-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getUsersLogout

<a id="opIdgetUsersLogout"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/users/logout \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/users/logout HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/logout',
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

fetch('https://api.di-portal.com/v2/users/logout',
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

result = RestClient.get 'https://api.di-portal.com/v2/users/logout',
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

r = requests.get('https://api.di-portal.com/v2/users/logout', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/logout");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/users/logout", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/logout`

*Logout an logged-in-user*

<h3 id="getUsersLogout-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|

> Example responses

<h3 id="getUsersLogout-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getUsersId

<a id="opIdgetUsersId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/users/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/users/{id} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/{id}',
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

fetch('https://api.di-portal.com/v2/users/{id}',
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

result = RestClient.get 'https://api.di-portal.com/v2/users/{id}',
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

r = requests.get('https://api.di-portal.com/v2/users/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/{id}");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/users/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/{id}`

*Get user profile by id*

<h3 id="getUsersId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|integer|true|No description|

> Example responses

<h3 id="getUsersId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## deleteUsersId

<a id="opIddeleteUsersId"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.di-portal.com/v2/users/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE https://api.di-portal.com/v2/users/{id} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/{id}',
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

fetch('https://api.di-portal.com/v2/users/{id}',
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

result = RestClient.delete 'https://api.di-portal.com/v2/users/{id}',
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

r = requests.delete('https://api.di-portal.com/v2/users/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/{id}");
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
    req, err := http.NewRequest("DELETE", "https://api.di-portal.com/v2/users/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /users/{id}`

*Delete a user from the store*

<h3 id="deleteUsersId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|integer|true|No description|

> Example responses

<h3 id="deleteUsersId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getUsersDevicesList

<a id="opIdgetUsersDevicesList"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/users/devices/list?networkTypeId=1 \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/users/devices/list?networkTypeId=1 HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/devices/list',
  method: 'get',
  data: '?networkTypeId=1',
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

fetch('https://api.di-portal.com/v2/users/devices/list?networkTypeId=1',
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

result = RestClient.get 'https://api.di-portal.com/v2/users/devices/list',
  params: {
  'networkTypeId' => 'integer'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('https://api.di-portal.com/v2/users/devices/list', params={
  'networkTypeId': '1'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/devices/list?networkTypeId=1");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/users/devices/list", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/devices/list`

*Returns a list of devices from store*

Use lucene syntax to filter for devices.

<h3 id="getUsersDevicesList-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|search|query|string|false|No description|
|searchType|query|string|false|No description|
|networkTypeId|query|integer|true|Network type supported by portal|
|filter|query|string|false|No description|
|orderBy|query|string|false|No description|
|skip|query|integer|false|Number of elements to skip for pagination|

> Example responses

<h3 id="getUsersDevicesList-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getUsersDevicesId

<a id="opIdgetUsersDevicesId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/users/devices/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/users/devices/{id} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/devices/{id}',
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

fetch('https://api.di-portal.com/v2/users/devices/{id}',
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

result = RestClient.get 'https://api.di-portal.com/v2/users/devices/{id}',
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

r = requests.get('https://api.di-portal.com/v2/users/devices/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/devices/{id}");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/users/devices/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/devices/{id}`

*Returns a device from store*

<h3 id="getUsersDevicesId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="getUsersDevicesId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## deleteUsersDevicesId

<a id="opIddeleteUsersDevicesId"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.di-portal.com/v2/users/devices/{id} \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
DELETE https://api.di-portal.com/v2/users/devices/{id} HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/devices/{id}',
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

fetch('https://api.di-portal.com/v2/users/devices/{id}',
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

result = RestClient.delete 'https://api.di-portal.com/v2/users/devices/{id}',
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

r = requests.delete('https://api.di-portal.com/v2/users/devices/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/devices/{id}");
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
    req, err := http.NewRequest("DELETE", "https://api.di-portal.com/v2/users/devices/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /users/devices/{id}`

*Delete a existing device and the related files*

<h3 id="deleteUsersDevicesId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="deleteUsersDevicesId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## putUsersDevicesId

<a id="opIdputUsersDevicesId"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://api.di-portal.com/v2/users/devices/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT https://api.di-portal.com/v2/users/devices/{id} HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/devices/{id}',
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
  "category": {
    "id": "string",
    "subcategory": {
      "id": "string"
    }
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/devices/{id}',
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

result = RestClient.put 'https://api.di-portal.com/v2/users/devices/{id}',
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

r = requests.put('https://api.di-portal.com/v2/users/devices/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/devices/{id}");
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
    req, err := http.NewRequest("PUT", "https://api.di-portal.com/v2/users/devices/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /users/devices/{id}`

*Partial update of the content of a Device*

> Body parameter

```json
{
  "category": {
    "id": "string",
    "subcategory": {
      "id": "string"
    }
  }
}
```

<h3 id="putUsersDevicesId-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|
|body|body|[Model_24](#schemamodel_24)|false|No description|

> Example responses

<h3 id="putUsersDevicesId-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getUsersIdCreatelogousagepdf

<a id="opIdgetUsersIdCreatelogousagepdf"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/users/{id}/createLogoUsagePdf \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/users/{id}/createLogoUsagePdf HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/{id}/createLogoUsagePdf',
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

fetch('https://api.di-portal.com/v2/users/{id}/createLogoUsagePdf',
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

result = RestClient.get 'https://api.di-portal.com/v2/users/{id}/createLogoUsagePdf',
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

r = requests.get('https://api.di-portal.com/v2/users/{id}/createLogoUsagePdf', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/{id}/createLogoUsagePdf");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/users/{id}/createLogoUsagePdf", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/{id}/createLogoUsagePdf`

*Create and get the Logo Usage Contract as a PDF*

<h3 id="getUsersIdCreatelogousagepdf-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|integer|true|No description|

> Example responses

<h3 id="getUsersIdCreatelogousagepdf-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## getUsersDevicesIdVersions

<a id="opIdgetUsersDevicesIdVersions"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/users/devices/{id}/versions \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/users/devices/{id}/versions HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/devices/{id}/versions',
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

fetch('https://api.di-portal.com/v2/users/devices/{id}/versions',
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

result = RestClient.get 'https://api.di-portal.com/v2/users/devices/{id}/versions',
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

r = requests.get('https://api.di-portal.com/v2/users/devices/{id}/versions', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/devices/{id}/versions");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/users/devices/{id}/versions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/devices/{id}/versions`

*Retrieve list of device versions*

<h3 id="getUsersDevicesIdVersions-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|id|path|string|true|No description|

> Example responses

<h3 id="getUsersDevicesIdVersions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsers

<a id="opIdpostUsers"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
POST https://api.di-portal.com/v2/users HTTP/1.1
Host: api.di-portal.com
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users',
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
  "username": "string",
  "email": "string",
  "redirectUrl": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword",
  "termsAccepted": true,
  "requestIP": "string",
  "asContentProvider": false,
  "companyName": "string",
  "companyWebsite": "string",
  "vatNo": "string",
  "phoneNumber": "string",
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "vendorIds": [
    {
      "networkTypeId": 0,
      "vendorId": "string"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/users',
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
  'Accept' => '*/*',
  'Authorization' => 'API_KEY'
}

result = RestClient.post 'https://api.di-portal.com/v2/users',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.post('https://api.di-portal.com/v2/users', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users`

*Add new user*

> Body parameter

```json
{
  "name": "string",
  "username": "string",
  "email": "string",
  "redirectUrl": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword",
  "termsAccepted": true,
  "requestIP": "string",
  "asContentProvider": false,
  "companyName": "string",
  "companyWebsite": "string",
  "vatNo": "string",
  "phoneNumber": "string",
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "vendorIds": [
    {
      "networkTypeId": 0,
      "vendorId": "string"
    }
  ]
}
```

<h3 id="postUsers-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Model_5](#schemamodel_5)|false|No description|

> Example responses

<h3 id="postUsers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## putUsers

<a id="opIdputUsers"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://api.di-portal.com/v2/users \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT https://api.di-portal.com/v2/users HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users',
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
  "isContentProvider": true,
  "username": "string",
  "password": "string",
  "newUsername": "string",
  "email": "string",
  "name": "string",
  "companyWebsite": "string",
  "companyName": "string",
  "phoneNumber": "string",
  "vatNo": "string",
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "redirectUrl": "string",
  "rememberMe": false
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users',
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

result = RestClient.put 'https://api.di-portal.com/v2/users',
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

r = requests.put('https://api.di-portal.com/v2/users', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users");
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
    req, err := http.NewRequest("PUT", "https://api.di-portal.com/v2/users", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /users`

*Update existing user*

> Body parameter

```json
{
  "isContentProvider": true,
  "username": "string",
  "password": "string",
  "newUsername": "string",
  "email": "string",
  "name": "string",
  "companyWebsite": "string",
  "companyName": "string",
  "phoneNumber": "string",
  "vatNo": "string",
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "redirectUrl": "string",
  "rememberMe": false
}
```

<h3 id="putUsers-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_22](#schemamodel_22)|false|No description|

> Example responses

<h3 id="putUsers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersChangepassword

<a id="opIdpostUsersChangepassword"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/changePassword \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/users/changePassword HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/changePassword',
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
  "oldPassword": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/changePassword',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/changePassword',
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

r = requests.post('https://api.di-portal.com/v2/users/changePassword', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/changePassword");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/changePassword", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/changePassword`

*Change user password*

> Body parameter

```json
{
  "oldPassword": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword"
}
```

<h3 id="postUsersChangepassword-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_9](#schemamodel_9)|false|No description|

> Example responses

<h3 id="postUsersChangepassword-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersDevices

<a id="opIdpostUsersDevices"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/devices?networkTypeId=1&ownerId=1 \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/users/devices?networkTypeId=1&ownerId=1 HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/devices',
  method: 'post',
  data: '?networkTypeId=1&ownerId=1',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "device": {
    "deviceId": "string",
    "name": "string",
    "products": [
      {
        "productId": "string",
        "name": "string",
        "productUrl": "string",
        "imgUrl": "string"
      }
    ]
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/devices?networkTypeId=1&ownerId=1',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/devices',
  params: {
  'networkTypeId' => 'integer',
'ownerId' => 'integer'
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

r = requests.post('https://api.di-portal.com/v2/users/devices', params={
  'networkTypeId': '1',  'ownerId': '1'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/devices?networkTypeId=1&ownerId=1");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/devices", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/devices`

*Create new device*

> Body parameter

```json
{
  "device": {
    "deviceId": "string",
    "name": "string",
    "products": [
      {
        "productId": "string",
        "name": "string",
        "productUrl": "string",
        "imgUrl": "string"
      }
    ]
  }
}
```

<h3 id="postUsersDevices-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|networkTypeId|query|integer|true|Network type supported by portal|
|ownerId|query|integer|true|No description|
|body|body|[Model_11](#schemamodel_11)|false|No description|

> Example responses

<h3 id="postUsersDevices-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersFile

<a id="opIdpostUsersFile"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/file?networkTypeId=1 \
  -H 'Content-Type: multipart/form-data' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/users/file?networkTypeId=1 HTTP/1.1
Host: api.di-portal.com
Content-Type: multipart/form-data
Accept: */*
authorization: string

```

```javascript
var headers = {
  'Content-Type':'multipart/form-data',
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/file',
  method: 'post',
  data: '?networkTypeId=1',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "file": "string"
}';
const headers = {
  'Content-Type':'multipart/form-data',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/file?networkTypeId=1',
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
  'Content-Type' => 'multipart/form-data',
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/file',
  params: {
  'networkTypeId' => 'integer'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'multipart/form-data',
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.post('https://api.di-portal.com/v2/users/file', params={
  'networkTypeId': '1'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/file?networkTypeId=1");
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
        "Content-Type": []string{"multipart/form-data"},
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/file", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/file`

*Upload a device description file*

> Body parameter

```yaml
file: string

```

<h3 id="postUsersFile-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|networkTypeId|query|integer|true|Network type supported by portal|
|categoryId|query|string|false|No description|
|subcategoryId|query|string|false|No description|
|override|query|boolean|false|No description|
|body|body|[postCrawlersFile](#schemapostcrawlersfile)|false|No description|
|» file|body|string(binary)|false|Device description file|

> Example responses

<h3 id="postUsersFile-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersLogin

<a id="opIdpostUsersLogin"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
POST https://api.di-portal.com/v2/users/login HTTP/1.1
Host: api.di-portal.com
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/login',
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
  "username": "string",
  "password": "string",
  "rememberMe": false
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/users/login',
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
  'Accept' => '*/*',
  'Authorization' => 'API_KEY'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/login',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.post('https://api.di-portal.com/v2/users/login', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/login");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/login", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/login`

*Login an existing user*

> Body parameter

```json
{
  "username": "string",
  "password": "string",
  "rememberMe": false
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
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersPasswordforgot

<a id="opIdpostUsersPasswordforgot"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/passwordForgot \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
POST https://api.di-portal.com/v2/users/passwordForgot HTTP/1.1
Host: api.di-portal.com
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/passwordForgot',
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
  "redirectUrl": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/users/passwordForgot',
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
  'Accept' => '*/*',
  'Authorization' => 'API_KEY'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/passwordForgot',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.post('https://api.di-portal.com/v2/users/passwordForgot', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/passwordForgot");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/passwordForgot", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/passwordForgot`

*Send a password reset email to the email address*

> Body parameter

```json
{
  "email": "string",
  "redirectUrl": "string"
}
```

<h3 id="postUsersPasswordforgot-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Model_13](#schemamodel_13)|false|No description|

> Example responses

<h3 id="postUsersPasswordforgot-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersPasswordreset

<a id="opIdpostUsersPasswordreset"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/passwordReset \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
POST https://api.di-portal.com/v2/users/passwordReset HTTP/1.1
Host: api.di-portal.com
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/users/passwordReset',
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
  "token": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/users/passwordReset',
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
  'Accept' => '*/*',
  'Authorization' => 'API_KEY'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/passwordReset',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.post('https://api.di-portal.com/v2/users/passwordReset', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/passwordReset");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/passwordReset", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/passwordReset`

*Rest user password*

> Body parameter

```json
{
  "token": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword"
}
```

<h3 id="postUsersPasswordreset-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Model_14](#schemamodel_14)|false|No description|

> Example responses

<h3 id="postUsersPasswordreset-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersTerms

<a id="opIdpostUsersTerms"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/terms \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/users/terms HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/terms',
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
  "requestIP": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/terms',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/terms',
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

r = requests.post('https://api.di-portal.com/v2/users/terms', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/terms");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/terms", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/terms`

*Indicate the acceptance of the latest terms and conditions*

> Body parameter

```json
{
  "requestIP": "string"
}
```

<h3 id="postUsersTerms-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_15](#schemamodel_15)|false|No description|

> Example responses

<h3 id="postUsersTerms-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersUpgrade

<a id="opIdpostUsersUpgrade"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/upgrade \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/users/upgrade HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/upgrade',
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
  "companyName": "string",
  "companyWebsite": "string",
  "phoneNumber": "string",
  "vendorIds": [
    {
      "networkTypeId": 0,
      "vendorId": "string"
    }
  ],
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "vatNo": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/upgrade',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/upgrade',
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

r = requests.post('https://api.di-portal.com/v2/users/upgrade', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/upgrade");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/upgrade", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/upgrade`

*Upgrade a user to a content provider*

> Body parameter

```json
{
  "companyName": "string",
  "companyWebsite": "string",
  "phoneNumber": "string",
  "vendorIds": [
    {
      "networkTypeId": 0,
      "vendorId": "string"
    }
  ],
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "vatNo": "string"
}
```

<h3 id="postUsersUpgrade-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_16](#schemamodel_16)|false|No description|

> Example responses

<h3 id="postUsersUpgrade-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersUpgradeConfirm

<a id="opIdpostUsersUpgradeConfirm"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/upgrade/confirm \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/users/upgrade/confirm HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/upgrade/confirm',
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
  "userId": 1
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/upgrade/confirm',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/upgrade/confirm',
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

r = requests.post('https://api.di-portal.com/v2/users/upgrade/confirm', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/upgrade/confirm");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/upgrade/confirm", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/upgrade/confirm`

*Confirm the upgrade of a user*

> Body parameter

```json
{
  "userId": 1
}
```

<h3 id="postUsersUpgradeConfirm-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_19](#schemamodel_19)|false|No description|

> Example responses

<h3 id="postUsersUpgradeConfirm-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postUsersUpgradeDeny

<a id="opIdpostUsersUpgradeDeny"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/users/upgrade/deny \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/users/upgrade/deny HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/upgrade/deny',
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
  "userId": 1,
  "reason": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/upgrade/deny',
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
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/users/upgrade/deny',
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

r = requests.post('https://api.di-portal.com/v2/users/upgrade/deny', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/upgrade/deny");
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
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/users/upgrade/deny", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /users/upgrade/deny`

*Deny the upgrade of a user*

> Body parameter

```json
{
  "userId": 1,
  "reason": "string"
}
```

<h3 id="postUsersUpgradeDeny-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_20](#schemamodel_20)|false|No description|

> Example responses

<h3 id="postUsersUpgradeDeny-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## putUsersDevicesPublish

<a id="opIdputUsersDevicesPublish"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://api.di-portal.com/v2/users/devices/publish \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT https://api.di-portal.com/v2/users/devices/publish HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/devices/publish',
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
  "devices": [
    "string"
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/devices/publish',
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

result = RestClient.put 'https://api.di-portal.com/v2/users/devices/publish',
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

r = requests.put('https://api.di-portal.com/v2/users/devices/publish', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/devices/publish");
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
    req, err := http.NewRequest("PUT", "https://api.di-portal.com/v2/users/devices/publish", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /users/devices/publish`

*Publishes a list of devices*

> Body parameter

```json
{
  "devices": [
    "string"
  ]
}
```

<h3 id="putUsersDevicesPublish-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_23](#schemamodel_23)|false|No description|

> Example responses

<h3 id="putUsersDevicesPublish-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## putUsersDevicesUnpublish

<a id="opIdputUsersDevicesUnpublish"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://api.di-portal.com/v2/users/devices/unpublish \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
PUT https://api.di-portal.com/v2/users/devices/unpublish HTTP/1.1
Host: api.di-portal.com
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
  url: 'https://api.di-portal.com/v2/users/devices/unpublish',
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
  "devices": [
    "string"
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/users/devices/unpublish',
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

result = RestClient.put 'https://api.di-portal.com/v2/users/devices/unpublish',
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

r = requests.put('https://api.di-portal.com/v2/users/devices/unpublish', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/users/devices/unpublish");
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
    req, err := http.NewRequest("PUT", "https://api.di-portal.com/v2/users/devices/unpublish", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /users/devices/unpublish`

*Unpublishes a list of devices*

> Body parameter

```json
{
  "devices": [
    "string"
  ]
}
```

<h3 id="putUsersDevicesUnpublish-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|body|body|[Model_23](#schemamodel_23)|false|No description|

> Example responses

<h3 id="putUsersDevicesUnpublish-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-crawlers">crawlers</h1>

## getCrawlersDevicesList

<a id="opIdgetCrawlersDevicesList"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.di-portal.com/v2/crawlers/devices/list?networkTypeId=1 \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
GET https://api.di-portal.com/v2/crawlers/devices/list?networkTypeId=1 HTTP/1.1
Host: api.di-portal.com

Accept: */*
authorization: string

```

```javascript
var headers = {
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/crawlers/devices/list',
  method: 'get',
  data: '?networkTypeId=1',
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

fetch('https://api.di-portal.com/v2/crawlers/devices/list?networkTypeId=1',
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

result = RestClient.get 'https://api.di-portal.com/v2/crawlers/devices/list',
  params: {
  'networkTypeId' => 'integer'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.get('https://api.di-portal.com/v2/crawlers/devices/list', params={
  'networkTypeId': '1'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/crawlers/devices/list?networkTypeId=1");
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
    req, err := http.NewRequest("GET", "https://api.di-portal.com/v2/crawlers/devices/list", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /crawlers/devices/list`

*Returns a list of devices from store*

Use lucene syntax to filter for devices.

<h3 id="getCrawlersDevicesList-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|search|query|string|false|No description|
|searchType|query|string|false|No description|
|networkTypeId|query|integer|true|Network type supported by portal|
|filter|query|string|false|No description|
|orderBy|query|string|false|No description|
|skip|query|integer|false|Number of elements to skip for pagination|

> Example responses

<h3 id="getCrawlersDevicesList-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postCrawlersFile

<a id="opIdpostCrawlersFile"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/crawlers/file?networkTypeId=1&ownerId=1 \
  -H 'Content-Type: multipart/form-data' \
  -H 'Accept: */*' \
  -H 'authorization: string'

```

```http
POST https://api.di-portal.com/v2/crawlers/file?networkTypeId=1&ownerId=1 HTTP/1.1
Host: api.di-portal.com
Content-Type: multipart/form-data
Accept: */*
authorization: string

```

```javascript
var headers = {
  'Content-Type':'multipart/form-data',
  'Accept':'*/*',
  'authorization':'string'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/crawlers/file',
  method: 'post',
  data: '?networkTypeId=1&ownerId=1',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "file": "string"
}';
const headers = {
  'Content-Type':'multipart/form-data',
  'Accept':'*/*',
  'authorization':'string'

};

fetch('https://api.di-portal.com/v2/crawlers/file?networkTypeId=1&ownerId=1',
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
  'Content-Type' => 'multipart/form-data',
  'Accept' => '*/*',
  'authorization' => 'string'
}

result = RestClient.post 'https://api.di-portal.com/v2/crawlers/file',
  params: {
  'networkTypeId' => 'integer',
'ownerId' => 'integer'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'multipart/form-data',
  'Accept': '*/*',
  'authorization': 'string'
}

r = requests.post('https://api.di-portal.com/v2/crawlers/file', params={
  'networkTypeId': '1',  'ownerId': '1'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/crawlers/file?networkTypeId=1&ownerId=1");
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
        "Content-Type": []string{"multipart/form-data"},
        "Accept": []string{"*/*"},
        "authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/crawlers/file", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /crawlers/file`

*Upload a device description file*

> Body parameter

```yaml
file: string

```

<h3 id="postCrawlersFile-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|authorization|header|string|true|No description|
|networkTypeId|query|integer|true|Network type supported by portal|
|ownerId|query|integer|true|No description|
|fileSourceUri|query|string|false|Source of the file|
|body|body|[postCrawlersFile](#schemapostcrawlersfile)|false|No description|
|» file|body|string(binary)|false|Device description file|

> Example responses

<h3 id="postCrawlersFile-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-contact">contact</h1>

## postContact

<a id="opIdpostContact"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/contact \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
POST https://api.di-portal.com/v2/contact HTTP/1.1
Host: api.di-portal.com
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/contact',
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
  "subject": "string",
  "email": "string",
  "text": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/contact',
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
  'Accept' => '*/*',
  'Authorization' => 'API_KEY'
}

result = RestClient.post 'https://api.di-portal.com/v2/contact',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.post('https://api.di-portal.com/v2/contact', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/contact");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/contact", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /contact`

*Send contact form*

> Body parameter

```json
{
  "subject": "string",
  "email": "string",
  "text": "string"
}
```

<h3 id="postContact-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Model_1](#schemamodel_1)|false|No description|

> Example responses

<h3 id="postContact-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

<h1 id="netIOT-DI-Portal-API-Documentation-newsletter">newsletter</h1>

## postNewsletterSignup

<a id="opIdpostNewsletterSignup"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/newsletter/signup \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
POST https://api.di-portal.com/v2/newsletter/signup HTTP/1.1
Host: api.di-portal.com
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/newsletter/signup',
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
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/newsletter/signup',
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
  'Accept' => '*/*',
  'Authorization' => 'API_KEY'
}

result = RestClient.post 'https://api.di-portal.com/v2/newsletter/signup',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.post('https://api.di-portal.com/v2/newsletter/signup', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/newsletter/signup");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/newsletter/signup", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /newsletter/signup`

*Signup for our newsletter*

> Body parameter

```json
{
  "email": "string"
}
```

<h3 id="postNewsletterSignup-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Model_7](#schemamodel_7)|false|No description|

> Example responses

<h3 id="postNewsletterSignup-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## postNewsletterUnsubscribe

<a id="opIdpostNewsletterUnsubscribe"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.di-portal.com/v2/newsletter/unsubscribe \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
POST https://api.di-portal.com/v2/newsletter/unsubscribe HTTP/1.1
Host: api.di-portal.com
Content-Type: application/json
Accept: */*

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/newsletter/unsubscribe',
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
  "redirectUrl": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/newsletter/unsubscribe',
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
  'Accept' => '*/*',
  'Authorization' => 'API_KEY'
}

result = RestClient.post 'https://api.di-portal.com/v2/newsletter/unsubscribe',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.post('https://api.di-portal.com/v2/newsletter/unsubscribe', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/newsletter/unsubscribe");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.di-portal.com/v2/newsletter/unsubscribe", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /newsletter/unsubscribe`

*Send email request to unsubscribe from newsletter*

> Body parameter

```json
{
  "email": "string",
  "redirectUrl": "string"
}
```

<h3 id="postNewsletterUnsubscribe-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Model_8](#schemamodel_8)|false|No description|

> Example responses

<h3 id="postNewsletterUnsubscribe-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

## deleteNewsletterUnsubscribe

<a id="opIddeleteNewsletterUnsubscribe"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.di-portal.com/v2/newsletter/unsubscribe?email=string&code=string \
  -H 'Accept: */*' \
  -H 'Authorization: API_KEY'

```

```http
DELETE https://api.di-portal.com/v2/newsletter/unsubscribe?email=string&code=string HTTP/1.1
Host: api.di-portal.com

Accept: */*

```

```javascript
var headers = {
  'Accept':'*/*',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'https://api.di-portal.com/v2/newsletter/unsubscribe',
  method: 'delete',
  data: '?email=string&code=string',
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
  'Authorization':'API_KEY'

};

fetch('https://api.di-portal.com/v2/newsletter/unsubscribe?email=string&code=string',
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
  'Authorization' => 'API_KEY'
}

result = RestClient.delete 'https://api.di-portal.com/v2/newsletter/unsubscribe',
  params: {
  'email' => 'string',
'code' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': '*/*',
  'Authorization': 'API_KEY'
}

r = requests.delete('https://api.di-portal.com/v2/newsletter/unsubscribe', params={
  'email': 'string',  'code': 'string'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://api.di-portal.com/v2/newsletter/unsubscribe?email=string&code=string");
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
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://api.di-portal.com/v2/newsletter/unsubscribe", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /newsletter/unsubscribe`

*Unsubscribe from newsletter*

<h3 id="deleteNewsletterUnsubscribe-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|email|query|string|true|No description|
|code|query|string|true|No description|

> Example responses

<h3 id="deleteNewsletterUnsubscribe-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Successful|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
jwt
</aside>

# Schemas

<h2 id="tocStranslations">translations</h2>

<a id="schematranslations"></a>

```json
[
  {
    "content": "string",
    "language": "de"
  }
]
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Model_2](#schemamodel_2)]|false|No description|

<h2 id="tocSvendorids">vendorIds</h2>

<a id="schemavendorids"></a>

```json
[
  {
    "networkTypeId": 0,
    "vendorId": "string"
  }
]
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Model_4](#schemamodel_4)]|false|No description|

<h2 id="tocSproducts">products</h2>

<a id="schemaproducts"></a>

```json
[
  {
    "productId": "string",
    "name": "string",
    "productUrl": "string",
    "imgUrl": "string"
  }
]
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Model_10](#schemamodel_10)]|false|No description|

<h2 id="tocSdevice">device</h2>

<a id="schemadevice"></a>

```json
{
  "deviceId": "string",
  "name": "string",
  "products": [
    {
      "productId": "string",
      "name": "string",
      "productUrl": "string",
      "imgUrl": "string"
    }
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|deviceId|string|false|No description|
|name|string|true|No description|
|products|[products](#schemaproducts)|true|No description|

<h2 id="tocSexternallinks">externalLinks</h2>

<a id="schemaexternallinks"></a>

```json
[
  {
    "name": "string",
    "url": "string",
    "categoryId": "001",
    "isLink": true
  }
]
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Model_17](#schemamodel_17)]|false|No description|

<h2 id="tocSexternallinkids">externalLinkIds</h2>

<a id="schemaexternallinkids"></a>

```json
[
  "string"
]
```

### Properties

*None*

<h2 id="tocSdevices">devices</h2>

<a id="schemadevices"></a>

```json
[
  "string"
]
```

### Properties

*None*

<h2 id="tocSsubcategory">subcategory</h2>

<a id="schemasubcategory"></a>

```json
{
  "id": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|true|No description|

<h2 id="tocScategory">category</h2>

<a id="schemacategory"></a>

```json
{
  "id": "string",
  "subcategory": {
    "id": "string"
  }
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|true|No description|
|subcategory|[subcategory](#schemasubcategory)|false|No description|

<h2 id="tocSmodel_1">Model_1</h2>

<a id="schemamodel_1"></a>

```json
{
  "subject": "string",
  "email": "string",
  "text": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|subject|string|true|No description|
|email|string|true|No description|
|text|string|true|No description|

<h2 id="tocSmodel_2">Model_2</h2>

<a id="schemamodel_2"></a>

```json
{
  "content": "string",
  "language": "de"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|content|string|true|No description|
|language|string|true|No description|

#### Enumerated Values

|Property|Value|
|---|---|
|language|de|
|language|en|

<h2 id="tocSmodel_3">Model_3</h2>

<a id="schemamodel_3"></a>

```json
{
  "translations": [
    {
      "content": "string",
      "language": "de"
    }
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|translations|[translations](#schematranslations)|false|No description|

<h2 id="tocSmodel_4">Model_4</h2>

<a id="schemamodel_4"></a>

```json
{
  "networkTypeId": 0,
  "vendorId": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|networkTypeId|integer|true|No description|
|vendorId|string|true|No description|

<h2 id="tocSmodel_5">Model_5</h2>

<a id="schemamodel_5"></a>

```json
{
  "name": "string",
  "username": "string",
  "email": "string",
  "redirectUrl": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword",
  "termsAccepted": true,
  "requestIP": "string",
  "asContentProvider": false,
  "companyName": "string",
  "companyWebsite": "string",
  "vatNo": "string",
  "phoneNumber": "string",
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "vendorIds": [
    {
      "networkTypeId": 0,
      "vendorId": "string"
    }
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|name|string|true|No description|
|username|string|true|No description|
|email|string|true|No description|
|redirectUrl|string|true|No description|
|newPassword|string|true|No description|
|confirmPassword|string|true|No description|
|termsAccepted|boolean|false|No description|
|requestIP|string|true|No description|
|asContentProvider|boolean|false|No description|
|companyName|string|false|No description|
|companyWebsite|string|false|No description|
|vatNo|string|false|No description|
|phoneNumber|string|false|No description|
|street|string|false|No description|
|houseNumber|string|false|No description|
|zipCode|string|false|No description|
|city|string|false|No description|
|country|string|false|No description|
|vendorIds|[vendorIds](#schemavendorids)|false|No description|

#### Enumerated Values

|Property|Value|
|---|---|
|confirmPassword|ref:newPassword|

<h2 id="tocSmodel_6">Model_6</h2>

<a id="schemamodel_6"></a>

```json
{
  "keyType": "frontend",
  "httpRef": "string",
  "host": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|keyType|string|true|No description|
|httpRef|string|false|No description|
|host|string|false|No description|

#### Enumerated Values

|Property|Value|
|---|---|
|keyType|frontend|
|keyType|App|
|keyType|Crawler|

<h2 id="tocSmodel_7">Model_7</h2>

<a id="schemamodel_7"></a>

```json
{
  "email": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|

<h2 id="tocSmodel_8">Model_8</h2>

<a id="schemamodel_8"></a>

```json
{
  "email": "string",
  "redirectUrl": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|
|redirectUrl|string|true|No description|

<h2 id="tocSmodel_9">Model_9</h2>

<a id="schemamodel_9"></a>

```json
{
  "oldPassword": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|oldPassword|string|true|No description|
|newPassword|string|true|No description|
|confirmPassword|string|true|No description|

#### Enumerated Values

|Property|Value|
|---|---|
|confirmPassword|ref:newPassword|

<h2 id="tocSmodel_10">Model_10</h2>

<a id="schemamodel_10"></a>

```json
{
  "productId": "string",
  "name": "string",
  "productUrl": "string",
  "imgUrl": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|productId|string|false|No description|
|name|string|false|No description|
|productUrl|string|false|No description|
|imgUrl|string|false|No description|

<h2 id="tocSmodel_11">Model_11</h2>

<a id="schemamodel_11"></a>

```json
{
  "device": {
    "deviceId": "string",
    "name": "string",
    "products": [
      {
        "productId": "string",
        "name": "string",
        "productUrl": "string",
        "imgUrl": "string"
      }
    ]
  }
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|device|[device](#schemadevice)|false|No description|

<h2 id="tocSmodel_12">Model_12</h2>

<a id="schemamodel_12"></a>

```json
{
  "username": "string",
  "password": "string",
  "rememberMe": false
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|username|string|true|No description|
|password|string|true|No description|
|rememberMe|boolean|false|No description|

<h2 id="tocSmodel_13">Model_13</h2>

<a id="schemamodel_13"></a>

```json
{
  "email": "string",
  "redirectUrl": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|
|redirectUrl|string|false|No description|

<h2 id="tocSmodel_14">Model_14</h2>

<a id="schemamodel_14"></a>

```json
{
  "token": "string",
  "newPassword": "string",
  "confirmPassword": "ref:newPassword"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|token|string|true|No description|
|newPassword|string|true|No description|
|confirmPassword|string|true|No description|

#### Enumerated Values

|Property|Value|
|---|---|
|confirmPassword|ref:newPassword|

<h2 id="tocSmodel_15">Model_15</h2>

<a id="schemamodel_15"></a>

```json
{
  "requestIP": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|requestIP|string|true|No description|

<h2 id="tocSmodel_16">Model_16</h2>

<a id="schemamodel_16"></a>

```json
{
  "companyName": "string",
  "companyWebsite": "string",
  "phoneNumber": "string",
  "vendorIds": [
    {
      "networkTypeId": 0,
      "vendorId": "string"
    }
  ],
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "vatNo": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|companyName|string|true|No description|
|companyWebsite|string|false|No description|
|phoneNumber|string|true|No description|
|vendorIds|[vendorIds](#schemavendorids)|true|No description|
|street|string|true|No description|
|houseNumber|string|true|No description|
|zipCode|string|true|No description|
|city|string|true|No description|
|country|string|true|No description|
|vatNo|string|true|No description|

<h2 id="tocSmodel_17">Model_17</h2>

<a id="schemamodel_17"></a>

```json
{
  "name": "string",
  "url": "string",
  "categoryId": "001",
  "isLink": true
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|name|string|true|No description|
|url|string|true|No description|
|categoryId|string|true|No description|
|isLink|boolean|false|No description|

#### Enumerated Values

|Property|Value|
|---|---|
|categoryId|001|
|categoryId|002|
|categoryId|003|
|categoryId|004|
|categoryId|005|
|categoryId|006|
|isLink|false|
|isLink|true|

<h2 id="tocSmodel_18">Model_18</h2>

<a id="schemamodel_18"></a>

```json
{
  "externalLinks": [
    {
      "name": "string",
      "url": "string",
      "categoryId": "001",
      "isLink": true
    }
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|externalLinks|[externalLinks](#schemaexternallinks)|false|No description|

<h2 id="tocSmodel_19">Model_19</h2>

<a id="schemamodel_19"></a>

```json
{
  "userId": 1
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|userId|integer|true|No description|

<h2 id="tocSmodel_20">Model_20</h2>

<a id="schemamodel_20"></a>

```json
{
  "userId": 1,
  "reason": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|userId|integer|true|No description|
|reason|string|true|No description|

<h2 id="tocSmodel_21">Model_21</h2>

<a id="schemamodel_21"></a>

```json
{
  "externalLinkIds": [
    "string"
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|externalLinkIds|[externalLinkIds](#schemaexternallinkids)|true|No description|

<h2 id="tocSmodel_22">Model_22</h2>

<a id="schemamodel_22"></a>

```json
{
  "isContentProvider": true,
  "username": "string",
  "password": "string",
  "newUsername": "string",
  "email": "string",
  "name": "string",
  "companyWebsite": "string",
  "companyName": "string",
  "phoneNumber": "string",
  "vatNo": "string",
  "street": "string",
  "houseNumber": "string",
  "zipCode": "string",
  "city": "string",
  "country": "string",
  "redirectUrl": "string",
  "rememberMe": false
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|isContentProvider|boolean|true|No description|
|username|string|true|No description|
|password|string|true|No description|
|newUsername|string|false|No description|
|email|string|false|No description|
|name|string|false|No description|
|companyWebsite|string|false|No description|
|companyName|string|false|No description|
|phoneNumber|string|false|No description|
|vatNo|string|false|No description|
|street|string|false|No description|
|houseNumber|string|false|No description|
|zipCode|string|false|No description|
|city|string|false|No description|
|country|string|false|No description|
|redirectUrl|string|false|No description|
|rememberMe|boolean|false|No description|

<h2 id="tocSmodel_23">Model_23</h2>

<a id="schemamodel_23"></a>

```json
{
  "devices": [
    "string"
  ]
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|devices|[devices](#schemadevices)|true|No description|

<h2 id="tocSmodel_24">Model_24</h2>

<a id="schemamodel_24"></a>

```json
{
  "category": {
    "id": "string",
    "subcategory": {
      "id": "string"
    }
  }
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|category|[category](#schemacategory)|false|No description|

<h2 id="tocSschema1">schema1</h2>

<a id="schemaschema1"></a>

```json
{
  "networkTypeId": 0,
  "vendorId": "string"
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|networkTypeId|integer|true|No description|
|vendorId|string|true|No description|

<h2 id="tocSschema2">schema2</h2>

<a id="schemaschema2"></a>

```json
[
  {
    "networkTypeId": 0,
    "vendorId": "string"
  }
]
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[schema1](#schemaschema1)]|false|No description|

