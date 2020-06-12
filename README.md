# Postman collection for Sophos Central APIs

This is a Postman collection for interacting with Sophos Central's Public APIs. See [https://developer.sophos.com](https://developer.sophos.com).

## Getting started

Once you have been accepted into the Sophos Central Public APIs preview program, you can create a set of API credentials by following the appropriate guide:

- For partners: [https://developer.sophos.com/getting-started](https://developer.sophos.com/getting-started)
- For organizations: [https://developer.sophos.com/getting-started-organization](https://developer.sophos.com/getting-started-organization)
- For tenants: [https://developer.sophos.com/getting-started-tenant](https://developer.sophos.com/getting-started-tenant)

Note the `client_id` and `client_secret` for the API credentials you create.

## Install Postman

To use this collection you will need to install [Postman](https://www.getpostman.com/downloads/) v7.26 or a later stable version.

## Import collection

Clone or download this repository. Then import the file `Sophos Central APIs.postman_collection.json` into Postman.

## Initialize environment

Next edit the `Sophos Central Example.postman_environment.json` file provided to add your `client_id` and `client_secret`.

## Make API calls

We recommend that you make API calls in the following order:

1. Authenticate to obtain an access token.
1. Call the Who-am-I API to find your Sophos-assigned partner, organization, or tenant ID.
1. Enumerate tenants as a partner/organization.
1. Get a specific tenant by ID.
1. Invoke Common API
1. Enumerate endpoints for a tenant.
1. Get a specific endpoint by ID.
1. Invoke Endpoint APIs

## A note on security️

Exercise extreme caution when handling and storing your credentials, in particular `client_secret`, as the theft of these will allow a malicious actor to access or delete sensitive data in your Sophos Central account. We recommend that you:

- Use a password manager, if possible. For example, on macOS, you can use the `security` command from the Terminal app to save the `client_secret` to the macOS KeyChain and later retrieve it from automation scripts.
- Don't use your credentials from an untrusted device or on an untrusted network
- Don't share your credentials with others, especially over insecure communication channels such as email
- Don't check your `client_secret` into source code

## Feedback

Please send any feedback to apis@sophos.com.
