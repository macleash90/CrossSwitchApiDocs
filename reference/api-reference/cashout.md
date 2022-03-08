---
description: This group of endpoints are related to Payment Transactions
---

# Cashout

## Create Cashout Transaction

{% swagger baseUrl="/CreateCashoutTrans" method="post" path=" " summary="This will create a new Cashout Transaction" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="app_id" required="true" type="String (16)" %}
API User ID (Inter pay authentic user)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="app_key" required="true" type="String (16)" %}
API User Password (Inter pay authentic user password)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="String (100)" %}
Customer Full name
{% endswagger-parameter %}

{% swagger-parameter in="body" name="mobile_network" type="String (20)" required="true" %}
Telco Code

Options are "MTN", "AIRTEL", "VODAFONE" ."TIGO"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="mobile" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="email" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="amount" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="order_id" required="true" %}
Merchant Transaction Reference Number (Unique)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="order_desc" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="signature" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="Payment successfully requested" %}
```javascript
{
    "status_code"="1",
    "status_message": "Success",
    "trans_ref_no": "E756WL987NL8",
    "Signature": "ahlpA6J1Fq6OYI1HFrMSGgBt0WY",
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "status_code"="0",
    "status_message": "Error Message"
}
```
{% endswagger-response %}
{% endswagger %}
