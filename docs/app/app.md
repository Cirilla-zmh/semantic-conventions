<!--- Hugo front matter used to generate the website version of this page:
linkTitle: App
--->

# App

**Status**: [Development][DocumentStatus]

This document defines events related to client-side applications
(e.g. web apps or mobile apps).

<!-- toc -->

- [Click Events](#click-events)
  - [Event: `app.screen.click`](#event-appscreenclick)
  - [Event: `app.widget.click`](#event-appwidgetclick)
- [Attributes](#attributes)

<!-- tocstop -->

## Click Events

### Event: `app.screen.click`

<!-- semconv event.app.screen.click -->
<!-- NOTE: THIS TEXT IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/snippet.md.j2 -->
<!-- prettier-ignore-start -->
<!-- markdownlint-capture -->
<!-- markdownlint-disable -->

**Status:** ![Development](https://img.shields.io/badge/-development-blue)

The event name MUST be `app.screen.click`.

This event represents an instantaneous click on the screen of an application.

The `app.screen.click` event can be used to indicate that a user has clicked or tapped on the screen portion of an application. Clicks outside of an application's active area SHOULD NOT generate this event. This event does not differentiate between touch/mouse down and touch/mouse up. Implementations SHOULD give preference to generating this event at the time the click is complete, typically on touch release or mouse up. The location of the click event MUST be provided in absolute screen pixels.

| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`app.screen.coordinate.x`](/docs/registry/attributes/app.md) | int | The x (horizontal) coordinate of a screen coordinate, in screen pixels. | `0`; `131` | `Required` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`app.screen.coordinate.y`](/docs/registry/attributes/app.md) | int | The y (vertical) component of a screen coordinate, in screen pixels. | `12`; `99` | `Required` | ![Development](https://img.shields.io/badge/-development-blue) |

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- END AUTOGENERATED TEXT -->
<!-- endsemconv -->

### Event: `app.widget.click`

<!-- semconv event.app.widget.click -->
<!-- NOTE: THIS TEXT IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/snippet.md.j2 -->
<!-- prettier-ignore-start -->
<!-- markdownlint-capture -->
<!-- markdownlint-disable -->

**Status:** ![Development](https://img.shields.io/badge/-development-blue)

The event name MUST be `app.widget.click`.

This event indicates that an application widget has been clicked.

Use this event to indicate that visual application component has been clicked, typically through a user's manual interaction.

| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`app.widget.id`](/docs/registry/attributes/app.md) | string | An identifier that uniquely differentiates this widget from other widgets in the same application. [1] | `f9bc787d-ff05-48ad-90e1-fca1d46130b3`; `submit_order_1829` | `Required` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`app.screen.coordinate.x`](/docs/registry/attributes/app.md) | int | The x (horizontal) coordinate of a screen coordinate, in screen pixels. | `0`; `131` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`app.screen.coordinate.y`](/docs/registry/attributes/app.md) | int | The y (vertical) component of a screen coordinate, in screen pixels. | `12`; `99` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`app.widget.name`](/docs/registry/attributes/app.md) | string | The name of an application widget. [2] | `submit`; `attack`; `Clear Cart` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |

**[1] `app.widget.id`:** A widget is an application component, typically an on-screen visual GUI element.

**[2] `app.widget.name`:** A widget is an application component, typically an on-screen visual GUI element.

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- END AUTOGENERATED TEXT -->
<!-- endsemconv -->

## Attributes

See the [app attributes](/docs/registry/attributes/app.md) registry for all
application-related attributes that may appear on telemetry items.

[DocumentStatus]: https://opentelemetry.io/docs/specs/otel/document-status
