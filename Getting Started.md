---
order: 100
icon: rocket
tags: [guide]
---

## Getting Started with your first event

### prepare guest list

You can download a sample guest list:
[!file sample](assets/sample-list.xlsx)

Besides texts columns, when a column has repeated values, it will be imported as a selection list. Later you can filter using it. For example:

| Group   | Level  |
| ------- | ------ |
| VIP     | 💎     |
| media   | 💎💎   |
| on-site | 💎💎💎 |

!!!warning
Only the first sheet will be imported.
!!!
!!!info
The excel file to be imported needed to be on the same ios device with the app. We suggest using iCloud or OneDrive to sync the file (which serves the benefit of a backup location). Or you can airdrop to the files app on your device.
!!!

:bulb: OneDrive has the additional benefit of being able to save history versions of your excel files.

---

### import the list

click create event

if files App (local or from cloud provider), find and select your excel file

:bulb: headers in the first column is required. if you leave following rows empty, you are creating a blank guest list for the event.

---

### manage the list

create new guest on site

filter the list

view live statistics

:bulb: you may edit your list without paid plan, with the exception that check-in status are not editable.

---

### pay to activate the event

after paying, you can checkin your guests. You may choose to pay and activate just one day before your event.

---

### at the event

checkin your guests in the list

checkin your guests by scanning QR code

multiple checkin is logged in the history section in the guest detail view

from guest menu, you can reset checkin status of the guest

---

### post event

export the list

additional columns will be exported:

| gift  | arrived_at                                                  |
| ----- | ----------------------------------------------------------- |
| TRUE  | 2021-09-26T19:05:37.451+00:00,2021-09-26T19:06:02.784+00:00 |
| FALSE |                                                             |
|       | 2021-09-26T19:05:37.451+00:00                               |

```
gift - whether guest has received a gift
arrived_at - timestamps of multiple checkins, seperated by comma
```

:bulb: you can export anytime during the event, as means of backup, or import the up to date list using another device. (note: data are not synced in multiple devices)


