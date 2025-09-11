# Book Quotes to HubSpot Deals Generator

## Overview

This [app card](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview), built with HubSpot’s [UI Extensions](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/ui-extensions-sdk), use the free, open-source [Open Library](https://openlibrary.org/) API to search for books, add them to a quote, and generate a deal from a Contact record.

### Project Structure

This project is split into two parts:

1. `book-quote-api/` \-  A backend built with [NextJS](https://nextjs.org/) to expose endpoints to both HubSpot and open-source APIs
2. `src/` \- The frontend [public app](https://developers.hubspot.com/docs/guides/apps/public-apps/overview?utm_campaign=Global+%28en%29+%7C+Developers+%7C+DevRel+GitHub&utm_source=GitHub&utm_medium=gh_repo&utm_content=uie_public_app_charts) containing one app card that works on contact records


### Requirements

There are a few things that must be set up before you can make use of this project.

* You must have an active HubSpot account.
* You must have the [HubSpot CLI](https://www.npmjs.com/package/@hubspot/cli) installed and set up.
* You must have an OAuth flow which will be used to obtain a HubSpot Access Token. To learn more about OAuth, visit our [documentation](https://developers.hubspot.com/docs/apps/developer-platform/build-apps/authentication/oauth/working-with-oauth). To get up and running with our [NodeJS OAuth Quick Start](https://developers.hubspot.com/docs/apps/developer-platform/build-apps/authentication/oauth/oauth-quickstart-guide), check out the [GitHub repo](https://github.com/HubSpot/oauth-quickstart-nodejs).

### Running the NextJS Backend Locally

1. With your [OAuth flow running](https://developers.hubspot.com/docs/apps/developer-platform/build-apps/authentication/oauth/working-with-oauth) in the background, navigate to the `book-quotes-api/` directory and run `npm install` to install the required dependencies for the NextJS project.
2. Create a `.env.local` file in this directory to house your HubSpot Access Token (generated from the OAuth workflow). You can find an example of this file in `sample.env.local`.

```
HUBSPOT_ACCESS_TOKEN='YOUR_ACCESS_TOKEN'
```

3. Now, you’re ready to start the development server\! Be sure to take note of the port the project is running on, as the local proxy will need to be configured later.

```
npm run dev
```

### Running the HubSpot App Card Locally

1. Clone this project to your local machine for local development

```
git clone https://github.com/hubspotdev/ui-extensions-examples
```

2. Navigate to the app card extensions directory

```
cd deal-generator
```

3. If you haven’t already done so, install the HubSpot CLI globally with NPM

```
npm install -g @hubspot/cli@latest
```

4. Connect your HubSpot account with the HubSpot CLI. This will prompt you to open your browser and copy/paste your account’s personal access key.

```
hs account auth
```

5. Install project dependencies with the HubSpot CLI

```
hs project install-deps
```

6. Upload the project to your connected HubSpot account. This should automatically trigger a deployment of the project as well.

```
hs project upload
```

7. Start the local development server. If the project did not previously exist on the connected HubSpot account, this will prompt you to install the app onto your connected HubSpot account. Connect the app, and select `Return Home`.

```
hs project dev
```

8. Add the app card(s) to a Contact record by going to `Settings` \> `Integrations` \> `Connected Apps` and selecting the desired app. Navigate to `App Cards` and find all app cards available with the project. To add a card to a record view, select `Manage Location` and add the card to your desired view and location. Navigate to a Contact record where the card was recently added and ensure there is a `Local Development` badge next to the title of the card. You’re ready to start coding\!


#### Note

When making changes to configuration files (`{CARD_NAME}-hsmeta.json` and `app-hsmeta.json`), be sure to stop the development server and use hs project upload to update the project before restarting the development server.

### Using the Book Quotes Card

This app card offers users the ability to:
 **Search for books:** Search for books by title, author, or ISBN using the OpenLibrary API

<br/>

![search for books](https://github.com/user-attachments/assets/07ee50ac-59c9-41b6-bb82-f7a864d594c7)


**Build a Cart:** Add or remove books from the cart and toggle between the book search and cart views

<br/>

![add to cart](https://github.com/user-attachments/assets/e7e1e6bb-85fc-4bdf-a11e-8f7f9e0ee641)


 **Generate a quote deal from the cart items:** Generate a quote deal from the cart items and add it to the contact record with the HubSpot Deals API. After the quote is generated, click the link in the banner to view the deal in HubSpot.

<br/>

![create a deal](https://github.com/user-attachments/assets/953fde36-f6bc-4443-80f7-42b0a2c3a5ce)

## Learn More About App Cards Powered by UI Extensions

To learn more about building app cards with UI Extensions, visit the [HubSpot app cards landing page](https://developers.hubspot.com/build-app-cards) and check out the [HubSpot app cards developer documentation](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview).

---

**Created By:** `Bree Hall`

