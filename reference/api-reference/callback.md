# Callback

## Cashout Callback function

Once the Cashout transaction is processed, a callback is sent to merchants whose URL is configured.

{% hint style="info" %}
The callback url is set by the merchant at the dashboard of the admin portal
{% endhint %}

{% swagger method="post" path="  " baseUrl="/YourCallbackUrl " summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="Transaction Successful" %}
```javascript
{
    "trans_ref_no": "548048484384084",
    "transaction_date": "2021-11-15 09:25:17.1296470",
    "amount": 20,
    "transaction_type": "DR",
    "merchant_trans_ref_no": "343rw34asdygs",
    "transaction_status": "Success"
}
```
{% endswagger-response %}

{% swagger-response status="200: OK" description="Transaction Failed" %}
```javascript
{
    "trans_ref_no": "548048484384084",
    "transaction_date": "2021-11-15 09:25:17.1296470",
    "amount": 20,
    "transaction_type": "DR",
    "merchant_trans_ref_no": "343rw34asdygs",
    "transaction_status": "Failure"
}
```
{% endswagger-response %}
{% endswagger %}
