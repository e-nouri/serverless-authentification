# serverless-oauth
serverless implementation of Oauth 2.0.

This service is the implmentation of Oauth 2.0 using serverless technology.


# But why first ?

## Oauth 2.0 Providers:
Adding loggins for other identity providers, like Facebook, Google and Twitter.
We can also plug Cognito to give access to devs through AWS IAM.

## SSO:
Using Oauth 2.0 will give us the possiblity to add SSO (Single Sign On) using SAML
Without too much trouble and effort.


# How to run  ?
You can use serverless Offline, with local DynamoDB and SNS / SQS offline to test this.
But the best is to deploy to AWS. To deploy run `sls deploy`

# TypeScript
Since this is an implementaion of a protocoal it makes sense to have Interfaces defined.
This project use TypeScript to enforce typing and makes it easy to develop
(autocomplete, VSCode typescript, doc, etc.)

# What is running and what is not ?
In OAuth 2.0 there are 4 modes / grant types, read the OAuth spec/draft for more info.
This is what is currently implmented and what is left :

- [x] Authorization Code: used with server-side Applications
- [x] Refresh Code: refresh token
- [ ] Implicit: used with Mobile Apps or Web Applications (applications that run on the user’s device, whitout redirection)
- [ ] Client Credentials: used with Applications API access
- [ ] Resource Owner Password Credentials: used with trusted Applications, such as those owned by the service itself

