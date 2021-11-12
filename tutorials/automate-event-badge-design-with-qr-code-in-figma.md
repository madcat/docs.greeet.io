# How to automate event badge design (with QR code)

![](./event-badge-examples.png)

Now you have your guest list organized, and want to create badges for them. I've found one way to automate this process without having to manually copy and paste each names.

### Prepare: Install Figma & Plugin

[Figma](https://www.figma.com/downloads/)

[Plugin : Google Sheets Sync](https://www.figma.com/community/plugin/735770583268406934/Google-Sheets-Sync)

### Step 1: Copy your guest list to Google sheets

Think about what information is unique to each guests that will be included in the badge design. At minimum it should be their name.

![](./event-badge-sheet-1.png)

!!!info
When your badge deisgn has First Name and Surname on two rows or even in two colors. You can simply use two columns for first name and surname and reference them in two text elements in Figma.
!!!

![](./event-badge-sheet-2.png)

### Step 2: Re-Create badge layout in Figma

Use dummy text layers to reference data column in your guest list.

For example, select the text layer for name. Change the layer name to #name where 'name' should be exactly the same as the column name in your Google sheet.

![](./event-badge-figma-layer-name.png)

### Step 3: Sync guests to badges

1. Open guest list file in Google sheets.
2. Click 'Share' in the top right of Google Sheets
3. Click 'Change to anone with the link'
4. Now click 'Copy link'

![](./event-badge-sheet-share.png)

5. From Figma menu, click Plugins > Google Sheets Sync
6. Paste the share link
7. Click 'Fetch & Sync'

![](./event-badge-figma-sync.png)

### Finish: Email or Print

You can choose to download each badge as PNG file to send Email, or group into printable size frames and download PDF files to print out.

:tada: **Now you have automatically generated badges for all your guests!**

==- Get in touch

# <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScF_aJQG1QWhQkGlnHBLUOlcT3K5MM-egeceAntukPDRGq8uA/viewform?embedded=true" width="512" height="512" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

===

---

### Advanced Tip 1: Automatically populate a unique QR code for each guest.

Add a column in google sheet for the content of QR code. Depends on which platform you want to later scan the QR code, this value should come from the platform.

Add another column(e.g. qr) for the QR code image, which we will use a online API to generate. Enter the following formula in the cell of second row:

```
= CONCATENATE("https://api.qrserver.com/v1/create-qr-code/?size=150x150&format=svg&data=",E3)
```

![](./event-badge-sheet-3.png)

Double click on the bottom right square, to copy down the formula to all rows.

In your figma file, add a reactangle layer (r key), and change the layer name to #qr.

Sync guests to badges.

The plugin will try to call the QR code api and download all the QR code images.

### Advanced Tip 2: Automatically populate multiple badge styles.

Consider you want diffrent groups of guests (VIP/Media/etc.) to have different badge designs.

Here is how you can do it:

1. Besides name, add another column in your guest list to indicate the grouping.

![](./event-badge-sheet-4.png)

2. In your figma file, create additional designs for each group. Name them as group=vip, group=media etc. where second part after the slash should be exact values in the group column in your guest list.

3. Now make each design frame a component.

4. Select all components, click Combine as Varaiants in the Design panel at right side of figma screen.

5. Sync guests to badges.
