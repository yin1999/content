---
title: "USBConnectionEvent: USBConnectionEvent() constructor"
short-title: USBConnectionEvent()
slug: Web/API/USBConnectionEvent/USBConnectionEvent
page-type: web-api-constructor
status:
  - experimental
browser-compat: api.USBConnectionEvent.USBConnectionEvent
---

{{APIRef("WebUSB API")}}{{SeeCompatTable}}{{SecureContext_Header}}{{AvailableInWorkers}}

The **`USBConnectionEvent()`** constructor creates a new {{domxref("USBConnectionEvent")}} object.
This constructor is not typically used,
it is created by the browser in response to the connection and disconnection of a USB device.

## Syntax

```js-nolint
new USBConnectionEvent(type, options)
```

### Parameters

- `type`
  - : A string with the name of the event.
    It is case-sensitive and browsers set it to `connect` or `disconnect`.
- `options`
  - : An object that, _in addition of the properties defined in {{domxref("Event/Event", "Event()")}}_, can have the following properties:
    - `device`
      - : A {{domxref("USBDevice")}} representing the USB device being connected or disconnected.

### Return value

A new {{domxref("USBConnectionEvent")}} object.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
