# About the openFDA API

openFDA is an Elasticsearch-based API that serves public FDA data about nouns like drugs, devices, and foods.

Each of these nouns has one or more categories, which serve unique data-such as data about recall enforcement reports, or about adverse events. Every query to the API must go through one endpoint for one kind of data.

Not all data in openFDA has been validated for clinical or production use. And because openFDA only serves publicly available data, it does not contain data with Personally Identifiable Information about patients or other sensitive information.

"API" is an acronym for Application Programming Interface. An API call is any request sent to the API. Requests are typically sent to the API in one of two ways: 1. Manually using a web browser (such as navigating to the URL https://api.fda.gov/drug/label.json) or 2. Programmatically sending the request via executing code that sends the API call and processes the response. Continue reading this documentation for more details on how to compose an API call for openFDA specifically.

The API returns individual results as JSON by default. The JSON object has two sections:

meta: Metadata about the query, including a disclaimer, link to data license, last-updated date, and total matching records, if applicable.

results: An array of matching results, dependent on which endpoint was queried.


# Authentication
An API key is required to make calls to the openFDA API. The key is free of charge. Your use of the API may be subject to certain limitations on access, calls, or use. These limitations are designed to manage load on the system, promote equitable access, and prevent abuse. Here are openFDA's standard limits:

With no API key: 240 requests per minute, per IP address. 1,000 requests per day, per IP address.

With an API key: 240 requests per minute, per key. 120,000 requests per day, per key.

If you anticipate usage above the limits provided by an API key, please contact us. We’ll work with you to figure out a good solution to your requirements. Signing up for an API key means you agree to our terms of service.

Your API key for ganadilynaif@gmail.com has been e-mailed to you. You can use your API key to begin making web service requests immediately.
Using your API key
Your API key should be passed to the API as the value of the api_key parameter. Include it before other parameters, such as the search parameter. For example:

https://api.fda.gov/drug/event.json?api_key=yourAPIKeyHere&search=...

HTTPS requests only
Alternatively your API key may be provided as a basic auth username. For example:

Authorization: Basic eW91ckFQSUtleUhlcmU6

openFDA requires you to use https://api.fda.gov for all queries to ensure secure communication.

# References:
- https://open.fda.gov/apis/
- https://open.fda.gov/apis/authentication/