---
title: 'Customer Tag'
parent: e98d4e7b-3e63-4328-bacc-83ace3e2af42
id: 40d75c86-8ed8-4190-8322-66ef6cf300a4
---
## Get a customer
This tag allows you to get a customer by their ID. Remember to provide the `id` parameter which should be the ID of the customer.

```
{{ sc:customer id="ff7ddbf2-cd01-4689-a57f-26cb2e7c96f9" }}
  Your name is {{ name }} and your email is {{ email }}.
{{ /sc:customer }}
```

### Update a customer
This tag allows you to update an existing customer. Remember to provide the `id` parameter which should be the ID of the customer.

```
{{ sc:customer:update id="ff7ddbf2-cd01-4689-a57f-26cb2e7c96f9" }}
  <input type="text" name="name">
{{ /sc:customer:update }}
```

### Get orders by customer
This tag allows you to loop through orders created by a customer. Remember to provide the `customer` parameter which should be the ID of the customer.

```
{{ sc:customer:orders customer="ff7ddbf2-cd01-4689-a57f-26cb2e7c96f9" }}
  {{ title }} - {{ grand_total }}
{{ /sc:customer:orders }}
```

### Get order by customer
This tag allows you to get an order created by a customer. This tag has two parameters. `id` for the ID of the order you want to get and `customer` is the ID of the customer you want to get.

```
{{ sc:customer:order customer="ff7ddbf2-cd01-4689-a57f-26cb2e7c96f9" id="84b28c73-3a04-478f-9447-68df026c44fe" }}
  {{ title }} - {{ grand_total }}
{{ /sc:customer:order }}
```