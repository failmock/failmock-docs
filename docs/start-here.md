# Start here

FailMock is for one common developer problem:

> How do I test how my app behaves when an external API fails.

In real life, providers time out, return bad responses, go down for a while, rateLimit your traffic, or fail to deliver webhooks. Those cases are hard to reproduce on demand, so many applications do not handle them well until they happen in production.

FailMock gives your app a fake provider that fails on purpose.

## The simple workflow

```text
Create failmock.yaml -> run FailMock locally -> call the fake provider -> activate a failure -> inspect what happened
```

You write the failure you want to test in `failmock.yaml`. Then your application calls FailMock instead of the real provider.

For the smoothest app integration, change only the provider base URL to FailMock and activate the scenario from the Routes page, on the UI. Your app does not need to send a special test header unless you choose the request-trigger approach.