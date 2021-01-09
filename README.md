# spec

`UniversalNotification` is a data format represented by JSON, inspired by [Chrome NotificationOptions](https://developer.chrome.com/docs/extensions/reference/notifications/#type-NotificationOptions).

## Motivation

For cross-platform applications, the existence of multiple notification systems requires developers to consider the notifications API for each platform independently.

Defining notifications as an intermediate form with a uniform format will help reduce friction when developing cross-platform notification applications.

## Definition

`UniversalNotification` is defined by [JSON Schema](https://json-schema.org/), see [schema.json](./schema.json).

### Properties

Each root property of `UniversalNotification` is optional.
For applications that receive `UniversalNotification`,
they do not need to support all properties,
only need to support the properties they can.

#### title

The header of the notification, it is usually emphasized visually.

#### message

The main notification content.

#### iconUrl

The URI to the sender's avatar, app icon.

#### imageUrl

The URI to the image for the notifications with image.

#### url

The URI to the main action when the user interacts with the notification.
Defined by the URI schemes of each platform.
