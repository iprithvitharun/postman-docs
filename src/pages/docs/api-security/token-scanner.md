---
title: "Token Scanner"
order: 115
page_id: "token-scanner"
search_keyword: "password security, secret scanning, secret, API key security"
---
The Postman token scanner scans your public workspaces, collections, environments, and documentation to find accidentally exposed known tokens. This protects your organization and prevents malicious users from exploiting the tokens.

> Token scanner is available for all users.
## Contents

* [Use cases](#use-cases)
* [Supported tokens](#supported-tokens)
    * [Default alerts](#default-alerts)
    * [Custom alerts](#custom-alerts)

## Use cases

A scan is triggered whenever your team members do any of the following actions:

* Change the workspace visibility to Public.
* Share a collection or environment to a public workspace.
* Make changes to a collection or environment that is present in a public workspace.
* Author new documentation for a Postman Collection and make it public.
* Importing collections and environments into a public workspace.

Scan results are displayed in [Security audit reports](/docs/designing-and-developing-your-api/view-and-analyze-api-reports/#security-audit-reports) on the **Reports** section of the web dashboard.

## Supported tokens

The token scanner will scan a variety of tokens by default. You can also add your team's proprietary third-party app tokens that are not supported yet using [custom alerts](#custom-alerts).

### Default alerts

By default, tokens issued by the following service providers are scanned:

* Basic Auth
* Bearer Token
* Google API Key
* Google OAuth Token
* PGP Private Key
* Postman API Key
* RSA Private Key
* Slack Access Token
* Slack Webhook URL
* SSH (DSA) Private Key
* SSH (EC) Private Key
* SSH (OpenSSH) Private Key
* Stripe Restricted Key
* Stripe Secret Key

### Custom alerts

> Custom alerts are available only on the [Enterprise plan](https://www.postman.com/pricing/). Your team can add a total of five alerts.

Custom alerts can be used to scan your team's proprietary and third-party app tokens that are not scanned by default.

To add custom alerts:

1. Go to **Team Settings** > **Token Scanner**.
2. In the **Custom alerts** section, click the **Add alerts** button.
3. In the **Add Alert** page, fill the required details for your custom alert.
4. Click **Add**.
    * **Name:** The name of the sensitive token that will be monitored using this custom alert.
    * **Type:** The type of sensitive token that this custom alert will monitor.
    * **Regex:** The regular expression that the token scanner will use to identify sensitive tokens of this type.
    * **Sample token:** A sample sensitive token that you’d like captured using this custom alert.