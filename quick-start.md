# Quick Start

## Get your **APP\_ID** and **APP\_KEY**

In all API method calls, you have to always pass the **app\_id** and **app\_key**. Any request that doesn't include **app\_id** and **app\_key** will not be processed.

You can generate an API key from your Dashboard at any time.

The best way to interact with our API is to use one of our official libraries:

## Make your first request

To make your first request, send an authenticated request to the /CreateCashoutTrans endpoint. This will create a Cashout Transaction.

{% swagger baseUrl="/CreatePaymentTrans" method="post" path=" " summary="Create Payment" %}
{% swagger-description %}
Creates a new pet.
{% endswagger-description %}

{% swagger-parameter in="body" name="app_id" required="true" type="String (64)" %}
API User ID (Inter pay authentic user)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="app_key" required="true" type="String (64)" %}
API User Key
{% endswagger-parameter %}

{% swagger-parameter in="body" name="client_timestamp" required="false" type="String (20)" %}
Transaction Date and time in following format YYYY-MM-SS Thh:mm:ss.sss
{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" required="false" type="String (100)" %}
Customer Full name
{% endswagger-parameter %}

{% swagger-parameter in="body" name="mobile_network" type="String (20)" required="true" %}
Telco Code
{% endswagger-parameter %}

{% swagger-parameter in="body" name="mobile" type="String (100)" required="true" %}
Customer Mobile number
{% endswagger-parameter %}

{% swagger-parameter in="body" name="email" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="feetypecode" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="amount" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="voucher_code" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="order_id" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="order_desc" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="signature" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="Pet successfully created" %}
```javascript
{
    "name"="Wilson",
    "owner": {
        "id": "sha7891bikojbkreuy",
        "name": "Samuel Passet",
    "species": "Dog",}
    "breed": "Golden Retriever",
}
```
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %}
{% endswagger %}

Take a look at how you might call this method using our official libraries, or via `curl`:

{% tabs %}
{% tab title="curl" %}
```
curl https://api.myapi.com/v1/pet  
    -u YOUR_API_KEY:  
    -d name='Wilson'  
    -d species='dog'  
    -d owner_id='sha7891bikojbkreuy'  
```
{% endtab %}

{% tab title="Node" %}
```javascript
// require the myapi module and set it up with your API key
const myapi = require('myapi')(YOUR_API_KEY);

const newPet = away myapi.pet.create({
    name: 'Wilson',
    owner_id: 'sha7891bikojbkreuy',
    species: 'Dog',
    breed: 'Golden Retriever',
})
```
{% endtab %}

{% tab title="Python" %}
```python
// Set your API key before making the request
myapi.api_key = YOUR_API_KEY

myapi.Pet.create(
    name='Wilson',
    owner_id='sha7891bikojbkreuy',
    species='Dog',
    breed='Golden Retriever',
)
```
{% endtab %}
{% endtabs %}
