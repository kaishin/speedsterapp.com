---
layout: default
---

# FAQ

If your question is not answered below, feel free to [get in touch](/support).

<hr>

## What is SpeedOfMe?

[SpeedOfMe](http://SpeedOfMe) is the API that Speedster uses to test your connection speed. It works by loading a hidden Web view that injects the SpeedOfMe script and sends the data to the native UI. As of now, this is the only viable approach to interact with the API.

<hr>

## Do I need a SpeedOfMe API key to use Speedster?

No. You can use Speedster by purchasing consumable test packs. However it's preferable that you use your own key in case in-app purchases are deprecated in the future.

<hr>

## How do I get a SpeedOfMe API key?

To use your own API key, you need:

- A [SpeedOfMe](http://speedof.me) API key (not affiliated with Speedster).
- A test page hosted in a unique domain associated to your key.

The next two sections will detail each requirement.

### Getting a SpeedOfMe API key

1. Head to the SpeedOfMe [plans and pricing page](http://speedof.me/api-plans.html). There is a **free trial** in case you are not ready to subscribe yet.
2. Click "Start Free Trial" on the plan that you are interested in. Pick with "Developer" if unsure.
3. In the sign up page, enter your personal details. Enter `speedsterapp.nfshost.com` in the *Domain* field for now.
4. Validate your email.

### Getting a unique test page domain

1. Head to the [speedster-test-page](https://github.com/kaishin/speedster-test-page) repository.
2. Follow the setup instructions in the [README](https://github.com/kaishin/speedster-test-page/blob/gh-pages/README.md).
3. Update the *Domain* field in both SpeedOfMe and Speedter. See the [README](https://github.com/kaishin/speedster-test-page/blob/gh-pages/README.md) for more details.

<hr>

## Can I use my own key alongside in-app purchases?

Yes. You can toggle the *Use SpeedOfMe API key* option in the app Preferences. When turned off, tests you run will not count towards your API usage, provided that you have previously made a in-app purchase on Speedster.

<hr>

## Will my in-app purchases get synced across computers?

No. As long as app is not making enough to cover API costs, this feature will not be added.

<hr>

## Can I restore my in-app purchases?

You can only restore Speedster Hero. Consumable in-app purchases such as test packs are not restorable. That's how Apple designed them to work.

<hr>

## This app is not for me, can you refund my purchase?

I can't. Please contact Apple to get your refund.

<hr>

## Can I change the test server?

No. The SpeedOfMe API doesn't support that as of now.

<hr>

## Why are the results often slower than other speed testing services?

That's how SpeedOfMe is [designed to work](http://speedof.me/howitworks.html).

## What data does Speedster collect?

Speedster does not collect any user data. Take a look at the [privacy policy](/privacy) for the details. SPEED OF ME, LLC might collect anonymous data and you are welcome to read the details on their own [privacy policy](http://speedof.me/privacy.html).
