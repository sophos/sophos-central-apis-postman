# Postman collection for Sophos Central APIs

This is a Postman collection for interacting with Sophos Central's Public APIs. See [https://developer.sophos.com](https://developer.sophos.com).

## Getting started

Use one of these Getting Started guides to set up your API credentials:

- Sophos Partners use [this](https://developer.sophos.com/getting-started) guide. You must be enrolled in the Sophos Partner Program to call our Partner APIs.
- Enterprise customers use [this](https://developer.sophos.com/getting-started-organization) guide. You should have Enterprise Admin enabled for one or more tenants in your organization.
- If neither profile fits you, use [this](https://developer.sophos.com/getting-started-tenant) guide for tenants.

Note down the `client_id` and `client_secret` for the API credentials you create.

## Install Postman

To use this collection you will need to install [Postman](https://www.getpostman.com/downloads/) v9.25 or a later stable version.

## Import collection

Clone or download this repository. Then import the file `Sophos Central APIs.postman_collection.json` into Postman.

## Initialize environment

Next edit the `Sophos Central Example.postman_environment.json` file provided to add your `client_id` and `client_secret`.

## Make API calls

We recommend that you make API calls in the following order:

1. Authenticate to obtain an access token.
1. Call the Who-am-I API to find your Sophos-assigned partner, organization, or tenant ID. This will add your account ID and the time-limited access token to the Postman environment, making it easier to click through many of the other API requests.
1. Enumerate tenants as a partner/organization and get a specific tenant by ID. (Tip: Set `tenant_id` in the Postman environment for convenience)
1. Call the Common API to list alerts, users and groups.
1. Enumerate endpoints for a tenant using the Endpoint API.
1. Configure endpoint global settings and perform actions, such as starting a scan.
1. See [this](https://developer.sophos.com/getting-started-with-live-discover) to run a Live Discover query.

## A note on security️

Exercise extreme caution when handling and storing your credentials, in particular `client_secret`, as the theft of these will allow a malicious actor to access or delete sensitive data in your Sophos Central account. We recommend that you:

- Use a password manager, if possible. For example, on macOS, you can use the `security` command from the Terminal app to save the `client_secret` to the macOS KeyChain and later retrieve it from automation scripts.
- Don't use your credentials from an untrusted device or on an untrusted network
- Don't share your credentials with others, especially over insecure communication channels such as email
- Don't check your `client_secret` into source code

## Feedback

Please send us feedback through the [community forum](https://community.sophos.com/developer/sophos-central-api/f/feedback-issues/120782/help-feedback).
