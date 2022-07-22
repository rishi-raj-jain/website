---
slug: "Capgo-API"
title: "Capgo API"
description: "Documentation for Capgo API"

---
# Intro 
This is the documentation of the backend API of Capgo cloud

You can access to the API you need to add in the headers your API key as `authorization`
you get it [there](https://web.capgo.app/app/apikeys)

# Channels
This endpoint allows you to check and modify all available Channels of your app

POST `https://capgo.app/api/channels`

Send this
```typescript
interface ChannelSet {
  appid: string
  channel: string
  version?: string
  public?: boolean
}
```

receive this:
```javascript
{ status: 'ok' }
```


GET  `https://capgo.app/api/channels`

Send `appid` as URL parameter and receive array of channel:
```javascript
{
    id: number;
    created_at: string;
    name: string;
    app_id: string;
    version: number;
    created_by: string;
    updated_at: string;
    public: boolean;
    disableAutoUpdateUnderNative: boolean;
    disableAutoUpdateToMajor: boolean;
}[]
```
and optionally `channel` name as URL parameter to receive one:
```javascript
{
    id: number;
    created_at: string;
    name: string;
    app_id: string;
    version: number;
    created_by: string;
    updated_at: string;
    public: boolean;
    disableAutoUpdateUnderNative: boolean;
    disableAutoUpdateToMajor: boolean;
}
```

# Devices
This endpoint allows you to check and modify all devices link to your app

POST `https://capgo.app/api/device`

Send this
```typescript
interface DeviceLink {
  app_id: string
  device_id: string
  version_id?: string
  channel_id?: string
}
```

receive this:
```javascript
{ status: 'ok' }
```
GET  `https://capgo.app/api/device`

Send `appid` as URL parameter and receive array of channel:
```javascript
{
    created_at?: string | undefined;
    updated_at?: string | undefined;
    device_id: string;
    version: number;
    app_id: string;
    platform?: "ios" | "android" | undefined;
    plugin_version: string;
    os_version?: string | undefined;
}[]
```
and optionally `channel` name as URL parameter to receive one:
```javascript
{
    created_at?: string | undefined;
    updated_at?: string | undefined;
    device_id: string;
    version: number;
    app_id: string;
    platform?: "ios" | "android" | undefined;
    plugin_version: string;
    os_version?: string | undefined;
}
```