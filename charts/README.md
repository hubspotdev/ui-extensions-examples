# Charts App Card
Build seamless customized experiences for all customers with [app cards powered by UI Extensions](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview). Discover how to fetch data from a third-party system to create customized charts.

Want a video tutorial? [Check out our video on the HubSpot Developers YouTube channel](https://youtu.be/5P6WuKyOiDE)!

![UIE Public App Card - Charts](https://github.com/user-attachments/assets/15f5289e-6cd2-4e82-886d-f1c2ab472598)

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
cd charts
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

### Using the Charts App Card
This card is configured to be viewed on Contact records. To view the card for development, navigate to any contact record and select `Customize record`. Select the view you'd like to update from the table and choose `Add cards`.
![Add App Card Screenshot](https://github.com/user-attachments/assets/deb4a103-f399-472b-88bb-86939a886760)

Then, navigate to any contact record page to view the card in the middle column.
![UIE Public App Card - Charts](https://github.com/user-attachments/assets/15f5289e-6cd2-4e82-886d-f1c2ab472598)

## Learn More About App Cards Powered by UI Extensions

To learn more about building public app cards, visit the [HubSpot app cards landing page](https://developers.hubspot.com/build-app-cards) and check out the [HubSpot app cards developer documentation](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview).

**Created By:** `Brooke Bond`
