---
description: This group of endpoints are related to Transactions already carried out
---

# Transactions

## Get Transaction Status

{% swagger method="post" path=" " baseUrl="/GetTransStatus" summary="" %}
{% swagger-description %}
Get the status of a transaction
{% endswagger-description %}

{% swagger-parameter in="body" name="app_id" type="String (16)" required="true" %}
API User ID (Inter pay authentic user)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="app_key" type="String (16)" required="true" %}
API User Password (Inter pay authentic user password)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="order_id" type="String (20)" required="true" %}
Merchant Transaction reference number
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "status_code": "1",
    "status_message": "Settled",
    "payment_date": "2022-01-10 06:43:36.0508350",
    "recipient_name": "Kwame Oppong",
    "recipient_mobile": "+233554110",
    "recipient_id_type": "NHIL",
    "recipient_id_number": "GUG82382",
    "Bank_account_no": "19948349834",
    "Bank_account_title": "Kwesi",
    "recipient _mobile": "+233244994883",
    "Recipient_mobile_operator": "MTN",
    "trans_ref_no": "232389139823811"
    
}
```
{% endswagger-response %}
{% endswagger %}
