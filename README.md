---
description: >-
  **Commissions** are created when a customer makes a purchase that an
  affiliates hould receive a commission for. Commissions are created
  automatically if you use Stripe for charges or invoicing. You on
---

# Commissions

{% api-method method="get" host="https://app.linkmink.com/api" path="/v0.1.0/commissions" %}
{% api-method-summary %}
Get Commissions
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of commissions using zero or more filters. Filters are combined in an 'AND' fashion - only results matching all of the filters will be returned. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer token using your api key. See "authentication" for instructions on authentication methods.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="max\_date" type="string" required=false %}
return commissions that were created before the supplied date
{% endapi-method-parameter %}

{% api-method-parameter name="min\_date" type="string" required=false %}
return commissions that were created after the supplied date
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}
filter - return only commissions of the given status
{% endapi-method-parameter %}

{% api-method-parameter name="affiliate\_id" type="string" required=false %}
filter - return commissions from the affiliate with a matching affiliate\_id
{% endapi-method-parameter %}

{% api-method-parameter name="affiliate\_email" type="string" required=false %}
filter - return commissions from affiliates with a matching email
{% endapi-method-parameter %}

{% api-method-parameter name="affiliate\_name" type="string" required=false %}
filter - return commissions from affiliates with a matching name
{% endapi-method-parameter %}

{% api-method-parameter name="conversion\_id" type="string" required=false %}
filter - return commissions for the given LinkMink conversion\_id
{% endapi-method-parameter %}

{% api-method-parameter name="customer\_id" type="string" %}
filter - only return commissions for the given Stripe customer
{% endapi-method-parameter %}

{% api-method-parameter name="customer\_email" type="string" %}
filter - return commissions for the given Stripe customer email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% tabs %}
{% tab title="Plain Text" %}
```text

```
{% endtab %}

{% tab title="" %}
```

```
{% endtab %}

{% tab title="" %}
```

```
{% endtab %}
{% endtabs %}



