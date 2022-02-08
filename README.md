# Sentry

This integration allows you to send alerts to users in xMatters and then resolve issues in Sentry.


---------

<kbd>
<a href="https://support.xmatters.com/hc/en-us/community/topics">
   <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</a>
</kbd>

---------

An updated version of this integration is available. You can install the new one-way version right from the Workflow Templates directory within your xMatters instance. [Learn more](http://help.xmatters.com/integrations/#cshid=Sentry).

---------

# Files

* [Sentry.zip](Sentry.zip) - Workflow zip file with the step and example flow
* [sentry.png](/sentry.png) - Sentry logo


# Installation

## Sentry Setup

This requires an account with [sentry.io](https://sentry.io).

These instructions are adapted from the sentry documentation. Check the [docs](https://docs.sentry.io/guides/alert-notifications/routing-alerts/#webhooks) out for more details.

1. When signed in, go to Settings > Developer Settings.
2. Create a new Internal Integration.
3. In the Name field put something that will help you identify it. We recommend **xMatters**.
4. Add a webhook URL from xMatters here. This is found in step 4 of the xMatters setup instructions below. Now would be a good time to follow the xMatters setup steps 1-4.
5. Under **Permissions > Issue & Event** select **Read & Write**. Do the same with **Permissions > Project**, and **Permissions > Organization**. This allows xMatters to resolve an alert.
6. Save the Integration and open it again.
7. Copy the Token near the end of the page. This will be used in the xMatters setup on step 5.
8. Attach this integration to rules in order to alert whenever you would like.

## xMatters Setup
1. Download the [Sentry.zip](Sentry.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded
4. Open the Alert Flow, then open the Inbound from Sentry step and copy the URL. This is used in step 4 of the Sentry Setup instructions above.
5. Take the Token you got from step 7 in the Sentry setup instructions and put it in the xMatters constant **Sentry API Token**
6. Adjust the recipients in the **Create Event - Alert** step.
7. Adjust the timezone in the **Moment - Convert Time** step.


## Example
This is what the integration looks like in xMatters.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

