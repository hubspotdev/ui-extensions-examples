# Tabbed Product Carousel

A HubSpot UI Extensions app card that displays product information in a tabbed interface with an image carousel, allowing users to browse through device specifications and photos.

<img width="679" alt="Completed product carousel card using HubSpot's UI Extensions" src="https://github.com/user-attachments/assets/dd4cc161-f795-4417-9e82-6e345e0b4097" />


## Overview

This [app card](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview), built with HubSpot’s [UI Extensions](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/ui-extensions-sdk), combines a dynamic photo carousel with a tabbed interface that displays device information in list format.

### Project Structure

The main extension logic lives in `tabbed-photo-carousel/src/app/PhotoCarouselCard.tsx`, which is the entry point and container component. The UI is broken down into components stored in the `components` directory, including:

* `PhotoCarousel` for dynamic photo carousel
* `ProductSpecsTabs` for the description lists containing device specs and information

### Requirements

There are a few things that must be set up before you can make use of this project.

* You must have an active HubSpot account.
* You must have the [HubSpot CLI](https://www.npmjs.com/package/@hubspot/cli) installed and set up.

### Running the HubSpot App Card Locally

1. Clone this project to your local machine for local development

```
git clone https://github.com/hubspotdev/ui-extensions-examples
```

2. Navigate to the app card extensions directory

```
cd tabbed-photo-carousel
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

### Using the Product Carousel Card
This app card allows you to select one of five devices from a drop-down list. When a device is selected, you can browse through a carousel of images and view data about it, separated into tabs.

<img src="https://github.com/user-attachments/assets/726ee079-5875-4f79-9925-377d46fb9c53" width="500"/>

## Learn More About App Cards Powered by UI Extensions

To learn more about building app cards with UI Extensions, visit the [HubSpot app cards landing page](https://developers.hubspot.com/build-app-cards) and check out the [HubSpot app cards developer documentation](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview).

---

**Created By:** `Bree Hall` & `Paul Gaskin`
