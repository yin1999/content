---
title: "CookieStore: set() method"
short-title: set()
slug: Web/API/CookieStore/set
page-type: web-api-instance-method
browser-compat: api.CookieStore.set
---

{{securecontext_header}}{{APIRef("Cookie Store API")}}{{AvailableInWorkers("window_and_service")}}

The **`set()`** method of the {{domxref("CookieStore")}} interface sets a cookie with the given `name` and `value` or `options` object.

## Syntax

```js-nolint
set(name, value)
set(options)
```

### Parameters

This method requires one of the following:

- `name` {{optional_inline}}
  - : A string with the name of the cookie.
- `value` {{optional_inline}}
  - : A string with the value of the cookie.

Or

- `options` {{optional_inline}}

  - : An object containing:

    - `domain` {{Optional_Inline}}
      - : A string containing the domain of the cookie. Defaults to `null`.
    - `expires` {{Optional_Inline}}
      - : A timestamp, given as {{glossary("Unix time")}} in milliseconds, containing the expiration date of the cookie. Defaults to `null`.
    - `name`
      - : A string with the name of a cookie.
    - `partitioned` {{Optional_Inline}}
      - : A boolean value that defaults to `false`. If set to `true`, the set cookie will be a partitioned cookie. See [Cookies Having Independent Partitioned State (CHIPS)](/en-US/docs/Web/Privacy/Guides/Privacy_sandbox/Partitioned_cookies) for more information.
    - `path` {{Optional_Inline}}
      - : A string containing the path of the cookie. Defaults to `/`.
    - `sameSite` {{Optional_Inline}}

      - : One of the following [`SameSite`](/en-US/docs/Web/HTTP/Reference/Headers/Set-Cookie#samesitesamesite-value) values:

        - `"strict"`
          - : Cookies will only be sent in a first-party context and not be sent along with requests initiated by third party websites. This is the default.
        - `"lax"`
          - : Cookies are not sent on normal cross-site subrequests (for example to load images or frames into a third party site), but are sent when a user is navigating to the origin site (i.e. when following a link).
        - `"none"`
          - : Cookies will be sent in all contexts.

    - `value`
      - : A string with the value of the cookie.

### Return value

A {{jsxref("Promise")}} that resolves with {{jsxref("undefined")}} when setting the cookie completes.

### Exceptions

- `SecurityError` {{domxref("DOMException")}}
  - : Thrown if the origin can not be {{glossary("Serialization", "serialized")}} to a URL.
- {{jsxref("TypeError")}}
  - : Thrown if setting the cookie with the given `name` and `value` or `options` fails.

## Examples

The following example sets a cookie by passing an object with `name`, `value`, `expires`, and `domain`.

```js
const day = 24 * 60 * 60 * 1000;

cookieStore.set({
  name: "cookie1",
  value: "cookie1-value",
  expires: Date.now() + day,
  domain: "example.com",
});
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
