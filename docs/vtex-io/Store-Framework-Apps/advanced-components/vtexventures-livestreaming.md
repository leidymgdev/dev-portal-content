---
title: "Live Shopping"
slug: "vtexventures-livestreaming"
hidden: false
createdAt: "2021-05-13T18:20:06.128Z"
updatedAt: "2022-10-13T22:39:05.115Z"
---

The Live Shopping app allows businesses to broadcast live on the store website, increasing selling rates, enhancing user experience, and boosting customer interaction simultaneously and in real-time.

The app works on both devices, desktop, and mobile.

![live-streaming-web](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-0.png)

![mobile-livestreaming](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-1.png)

## Installation

1. Access the [Live Shopping app page on the VTEX App Store](https://apps.vtex.com/vtexventures-livestreaming/p).
2. Click on the `Get app` button to install the app in your VTEX account.

> ⚠️ Notice that this is a paid app whose subscription costs will depend on the plan that you have chosen: **Lite**, **Standard**, or **Pro**. All payment details are provided at the moment of installation. Plan pricing refers to the total monthly minutes available for you to make as many transmissions as you like within the plan's available minutes. Each plan includes a set number of minutes for a month. For more details on the plans and pricing check out the [Live Shopping App Store page](https://apps.vtex.com/liveshopping/p).

3. Once the app is successfully installed, open your account's Store Theme app using the code editor of your preference.
4. In the `manifest.json` file, add the app to the theme's peer dependencies list:

```
"peerDependencies": {
    "vtexventures.livestreaming": "0.x"
  }
```

5. Declare the Live Shopping app in the desired template. For example:

```
"store.home": {
    "blocks": [
      "livestreaming",
      "rich-text#shelf-title",
      "flex-layout.row#shelf",
      "rich-text#question",
      "rich-text#link",
      "newsletter"
    ]
  },
```

6. [Deploy your changes](https://developers.vtex.com/docs/guides/vtex-io-documentation-making-your-new-app-version-publicly-available#step-6---deploying-the-app-stable-version).

Once you have deployed your changes, check out the [app's overview on VTEX Admin](#apps-overview-on-vtex-admin) and set up the app on your store's by following the instructions on the [Configuration section below.](#configuration)

## App's overview on VTEX Admin

Once you have [installed the VTEX Live Shopping app](#installation), access your store's **Admin** > **Store Setup** > **Live Shopping** > **Events** and you will see an interface as the following:

![app-overview](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-2.png)

- **Events**: section responsible for creating new events, managing them, and tracking events' data. Check out the [Configuration section below.](#configuration) set up the app on your store's.

- **Usage**: helps you track how many Live events minutes are available and were used by your account.

> ⚠️ The total amount of minutes available will depend on your chosen plan: **Lite**, **Standard**, or **Pro**. All payment details are provided at the moment of installation.

## Configuration

### Creating new events

1. Open your account Admin using your browser.
2. In the Store Setup section, access `Live Shopping`.
3. Click on `Events`.
4. Click on the `New` button to schedule a new live shopping on your website.

![creating-events](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-3.png)

5. Fill out the fields according to the instructions below:

- `Event Name` - The desired name for the event being created.
- `UTM Source` - The urchin tracking parameters, i.e., identification data for your URL. It enables you to track accesses and check where different traffic comes from.
- `Collection ID` - Optional field. The ID of the desired product collection to be attached to the live stream event. This feature encourages customers to add more products to the store cart.

6. Save your changes.

### Live Shopping events

![admin-events](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-4.png)

1. In the events list, click on the desired event's arrow button (in the `Action` column).
2. Copy the event's ID in the `Details` section.
3. Change its status to `Live` by toggling the `Status` button.

![details](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-5.png)

> ⚠️ The event will take approximately 3 minutes to turn on, i.e., be live.

4. Using the admin sidebar, access `CMS` and then `Site Editor`.
5. Locate the Live Shopping block in your store, according to the template you have declared it, and click on it.

![site-editor-configs](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-6.png)

6. Toggle the `Show component` button to display the Live Shopping component on your store.
7. Click in **Item** and in **Events (In live)** choose the desired event. Then click on `APPLY`.
8. If desired, set a start and end date for the component display.

> ℹ️ Use the Site Editor module to configure not only the live event but also texts, images, and banners to be displayed alongside it.

9. Save your changes.

#### Choosing the transmission’s Layout type

1. In the events list, click on the desired live event's arrow button (in the `Action` column).
2. In the section, **Layout Type**, choose the type of layout do you want for the Live event:

- Horizontal transmission: Recommended for desktop resolutions.
- Vertical transmission: Recommended for mobile resolutions.

### Accessing the studio to be on the live stream

1. In the events list, click on the desired live event's arrow button (in the `Action` column).
2. In the section, **Streaming Studio**, you have two buttons:

- `COPY INVITATION`: click on it and send the live event’s link to a co-host, for example, and they can enter live with you.
- `ACCESS`: Access the live event studio as the host of it.

When you click on `ACCESS`, a new window will appear redirecting you to the live studio.
![access](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-7.png)

In the `Complete my profile` field, type your name and click on `CONTINUE`.
Then, the page will redirect you to the live event studios.

### Managing events' live chat

The Live Shopping app counts with a live chat, enabling your users to engage with the event and share their questions in real-time.

1. In the events list, click on the desired live event's arrow button (in the `Action` column).
2. In the `Live Chat` section, keep up with real-time comments, as well as the number of viewers and likes.

![live-chat](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-8.png)

3. In the `Questions` section, create questions to be displayed to the audience through the `New question` button. You can choose between quizzes and polls and define the time frame in which they will be displayed. The fetched answers will be stored in the same section.

![new-question](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-9.png)

4. In the admin sidebar, access the `Block list of words` section.
5. Click on the `New` button to define which words will be forbidden to be displayed on the real-time chat.

![block-words](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-10.png)

> ℹ️ This feature is helpful to block rude, politician, or non-related comments from your live stream. Notice that the added words will be applied to all events, with no exceptions.

6. Do not forget to save all of your changes during the steps.

### Showing products during the Live event

When you [create a new event](#creating-new-events), you have the option to add the ID of the desired product collection to be attached to the live stream event, and in the section **Products within collection**, you can manage which products will show during the event.

1. In the events list, click on the desired live event's arrow button (in the `Action` column).
2. In the `Products within collection` section, choose the desired products to show during the Live stream and toggle the `Actions` button.

![live-shopping-products](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-11.png)

### Finalising live-streamed events

1. In the events list, click on the desired live event's arrow button (in the `Action` column).
2. Change its status to `Finalized` by toggling the `Status` button.

> ⚠️ The live shopping completion process may take a while. Do not close the page until the `Finalized` status is green, as shown in the image below.

![finalized-status](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-12.png)

Once finished, you can request the recording of your event in **Recording the event** section and click on the button `REQUEST VIDEO`.

### Tracking events' data

1. In the events list, click on the desired event's graphic button in the `Action` column.
2. Check out the events' analytics data, as shown below:

![analytics-event](https://cdn.jsdelivr.net/gh/vtexdocs/dev-portal-content@main/docs/vtex-io/Store-Framework-Apps/advanced-components/vtexventures-livestreaming-13.png)

## Customization

To apply CSS customizations in this and other blocks is done through the customization module.

Enter the details of the event and when the event is in live a button will be activated called "Customize look and feel" by clicking in it, you will enter the customization module.

Now, you will be able to customize the elements of the application according to the brand image in a simple and fast way.
We recommend that ideally the configuration and customization be done before selecting the event in the site editor, starting the live and making it visible on the website; well, to visualize the changes on the user's side the page where the transmission is being shown must be refreshed.

![1](https://user-images.githubusercontent.com/34868336/236523154-256f1c99-7cd5-44e5-b371-198c3285b173.png)

When entering the customization module you will find two visuals: Mobile and Desktop; by selecting each of them you will be able to configure and customize the components of said views. In each of these visuals you can customize the product and chat sections.

![2](https://user-images.githubusercontent.com/34868336/236523186-9aacc6e4-b74a-456e-80e4-b8339f5e366b.png)
