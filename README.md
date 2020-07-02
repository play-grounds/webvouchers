# webvouchers
webvouchers playground

# lnurl

## lnurlw

### lnurlw object

bech32 secret url

### lnurlw secret url object

secret url which points to an object containing the callback url object

it is a preflight request before sending an invoice to learn more about the parameters and where the endpoint is

### lnurlw callback url object

What is it?

It's an object that allows you to cash in an invoice

How do you use it?

Using the key (k1) and the callbackUri (callback) you can send an HTTP request which will fulfil the terms of the lightning network invoice

http://secretUri.example a capabilityUri
   desc: voucher
   callback: <uri> # endpoint
   k1: k1234
   min: 100
   max: 1000
   sameAs urn:voucher:k1234

{
    "@id": "http://secretUri.example",
    "callback": "http://callbackuri.example",
    "k1": "k1234",
    "min": 0,
    "max": 100
}

### lnurlw invoice url object

http://callbackuri.example a capabilityUri
  url: http://callbackuri.example
  pr: paymentrequest
