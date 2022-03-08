---
description: This group of endpoints are related to Payment Transactions
---

# Payments

## Create Payment

{% swagger baseUrl="/CreatePaymentTrans" method="post" path=" " summary="This will create a new Momo Payment Transaction" %}
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

## Get Transaction Status

{% swagger method="post" path=" " baseUrl="/CashoutTransStatus " summary="" %}
{% swagger-description %}
Get the status of a transaction
{% endswagger-description %}

{% swagger-parameter in="body" name="app_id" type="String (16)" required="true" %}
API User ID (Inter pay authentic user)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="app_key" type="String (16)" required="true" %}
API User Password (Inter pay authentic user password)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="merch_trans_ref_no" type="String (20)" required="true" %}
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
