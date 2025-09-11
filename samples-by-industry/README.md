# App Card by Industry
A collection of [app cards](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview), built with HubSpot’s [UI Extensions](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/ui-extensions-sdk), representing various industries designed to get you started and spark your creativity, including:

* **Education**: Enhance administrative efficiency by tracking student recruitment progress, managing communication, and providing insights into course enrollment and student performance.
* **Manufacturing**: Streamline operations by managing furniture returns, reviewing product details and images, and tracking manufacturing order production status with progress indicators and detailed steps.
* **Professional Services**: Track client interactions, manage service delivery schedules, and monitor project timelines by providing project snapshots, displaying project status and milestones, and logging billed hours with progress indicators.
* **Healthcare**: Improve patient management with tools such as a patient referral form to streamline patient referrals.

## Education Cards
### Recruiting Outlook

A student's progress through the recruitment process, displayed in a progress bar, accompanied by student details in a property list, and related financial assistance within a table.

Please note, this card utilizes a [CRM Property List](https://developers.hubspot.com/beta-docs/reference/ui-components/crm-data-components/crm-property-list), a [CRM data component](https://developers.hubspot.com/beta-docs/reference/ui-components/crm-data-components/overview) that queries HubSpot for data properties. To see this component in your portal, replace the `toObjectTypeId` and `toObjectType` properties on the [`<CrmPropertyList />`](https://github.com/hubspotdev/uie-industry-card-samples/blob/61389c9f2eeb838f791a74d750b891a0c96fb932/education/src/app/extensions/Recruiting_Outlook.jsx#L55) component with your desired object selections.

<img width="400" alt="Recruiting outlook card" src="https://github.com/user-attachments/assets/f6c8119e-bbf4-49fa-98fc-5bd01111ec42">

### Course Enrollment

A collection of course statistics accompanied by a table of a student's current and past courseload


<img width="400" alt="Course enrollment card" src="https://github.com/user-attachments/assets/1849cab3-01e5-4053-8224-0f39aa19e1c2">

## Manufacturing Cards
### Returns

A form used to initiate a furniture return after purchase, accompanied by a table of associated furniture pieces

<img width="400" alt="Returns card" src="https://github.com/user-attachments/assets/0c7830b3-5563-4904-b86c-100ec4d190de">

### Product Review

Displays furniture properties in a property list with an image of the piece

Please note, this card utilizes a [CRM Property List](https://developers.hubspot.com/beta-docs/reference/ui-components/crm-data-components/crm-property-list), a [CRM data component](https://developers.hubspot.com/beta-docs/reference/ui-components/crm-data-components/overview) that queries HubSpot for data properties. To see this component in your portal, replace the `toObjectTypeId` and `toObjectType` properties on the [`<CrmPropertyList />`](https://github.com/hubspotdev/ui-extensions-examples/blob/db10fb8b2648ff9d47cb73cf157dc46d7ba82f86/samples-by-industry/src/app/cards/ManufacturingProductReviewCard.tsx#L25) component with your desired object selections.

<img width="400" alt="Product review card" src="https://github.com/user-attachments/assets/6c2c325d-bc26-4090-8549-2aa5d6985609">

### Production

Manufacturing order production status displayed with progress bars and further details in a step indicator and table

<img width="400" alt="Manufacturing card" src="https://github.com/user-attachments/assets/abcb5414-3604-40b6-af1d-f363c25aade8">


## Healthcare Cards
### Patient Referral

A form used to initiate a patient referral

<img width="400" alt="Patient referral card" src="https://github.com/user-attachments/assets/a1ca478f-9c9b-4540-8ff3-52e0f990b4f6">

## Requirements

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
cd samples-by-industry
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

## Learn More About App Cards Powered by UI Extensions


To learn more about building public app cards, visit the [HubSpot app cards landing page](https://developers.hubspot.com/build-app-cards) and check out the [HubSpot app cards developer documentation](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview).
