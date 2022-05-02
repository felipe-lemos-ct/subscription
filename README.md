## Todo

- [Authenticate](https://youtu.be/zi9ndn2obdk?t=204) the cloud run service (Felipe)
- Update [Deploy.README.md](https://github.com/harm-meijer/subscription/blob/master/Deploy/Readme.md) (Felipe)
- Rebase into one commit (last after Felipe is done) (Harm)

# Subscription demo

## Installation

1. After cloning the repo run `yarn install` and in Deploy/server run `yarn install` again.

2. Create a .env file in root of the project (.env.local does not work!) with the content of an admin api key [generated](https://docs.commercetools.com/getting-started/create-api-client#create-an-api-client) in mc center (export as Sunrise SPA)

3. Run `yarn build` in the project root

4. Follow the [deploy](https://github.com/harm-meijer/subscription/blob/master/Deploy/Readme.md) instructions to deploy this code on cloud run.

5. Create a Google pub sub [topic](https://console.cloud.google.com/cloudpubsub/topic/list?referrer=search&project=ct-sales-207211) and create a subscription, make it a push subscription and use the url of the published cloud run project.

6. Use the [subscription.json](https://github.com/harm-meijer/subscription/blob/master/commercetools/subscription.json) create a subscription on the [api playground](https://impex.europe-west1.gcp.commercetools.com/playground) (use it as payload).

7. Use the [customerPointsType.json](https://github.com/harm-meijer/subscription/blob/master/commercetools/customerPointsType.json) to create a type on the [api playground](https://impex.europe-west1.gcp.commercetools.com/playground) (use it as payload).
