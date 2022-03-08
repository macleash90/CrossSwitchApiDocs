# Balance Enquiry

### Get Balance

To check the available balance in EPA Collection Account for the Merchant

{% swagger method="post" path=" " baseUrl="/CheckAvailableBalance " summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="app_id" required="true" type="String (16)" %}
API User ID (EPA authentic user)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="app_key" required="true" type="String (16)" %}
API User Password (EPA authentic user password)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
```javascript
{
   "status_code": "1",
   "status_message": "Success",
   "Available_Balance": 432
}
```
{% endswagger-response %}

{% swagger-response status="200: OK" description="Error" %}
```javascript
{
   "status_code": "0",
   "status_message": "Error description"
}
```
{% endswagger-response %}
{% endswagger %}
