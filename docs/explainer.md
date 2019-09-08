# Device Discovery API

NOTE: THIS IS WORK IN PROGRESS (draft)

## Authors:

- Lars Knudsen (@larsgk)
- [Author 2]
- [etc.]

## Table of Contents [if the explainer is longer than one printed page]

[You can generate a Table of Contents for markdown documents using a tool like [doctoc](https://github.com/thlorenz/doctoc).]

## Introduction

The Generic Sensor API spec (https://w3c.github.io/sensors/) and
derivaties (e.g. https://www.w3.org/TR/orientation-sensor/) provide
a great foundation for unified interaction with device sensors.
In addition, Web USB, Web Bluetooth and Serial API enables communication
with external devices attached to the host system, relying on user
interaction and custom driver code embedded in the application.

However, there is a need for a generic solution for actuator support,
device discovery, pre-provisioning and driver registration for this
domain of features to be valuable - in particular - for
enterprise solutions.

## Motivating Use Cases

### Engineer/field worker running diagnostics

Inspection of factory floors, engine rooms, etc. will benefit from
field workers to be able to quickly obtain readings from sensors in the
vicinity. Connection can be wired or wireless depending on the setup.
Assuming the diagnostics SW is a PWA (being offline will be a common case),
the engineer should be able to discover and interact with trusted
devices without the need to go through the current flow of provisioning
for every single sensor.

TBD areas to explore: Enterprise Chrome or Extensions (pre-provision),
(trusted) driver registration, NFC

### Vehicle monitoring
When connecting a phone to a vehicle (most common: car) via BLE or USB, I'd like for
any web app utilizing sensor data (geolocation, ambient light, temperature, etc.)
to be able to tap into the extra sensors available.

It should be possible to register and prioritize (e.g. 'new default')
these sensors to be discoverable as first class Generic Sensors for the app.

TBD areas to explore: NFC (tap to provision on/off)

### Home automation
Given that BLE Mesh implementations for home automation is moving now it would
only be natural if a web app connecting to a node in the house would be able to
discover and interact with the sensors and actuators available.  Allowing
dynamic registration/deregistration in the Generic Sensor (and Actuator) context
will provide app developers a generalized and portable approach to interacting
with home automation units (thermostats, lights, environmental readings, etc.).

## API: Driver Registration

## API: Device Discovery

## [API 1]

[For each related element of the proposed solution - be it an additional JS method, a new object, a new element, a new concept etc., create a section which briefly describes it.]

```js
// Provide example code - not IDL - demonstrating the design of the feature.

// If this API can be used on its own to address a user need,
// link it back to one of the scenarios in the goals section.

// If you need to show how to get the feature set up
// (initialized, or using permissions, etc.), include that too.
```

[Where necessary, provide links to longer explanations of the relevant pre-existing concepts and API.
If there is no suitable external documentation, you might like to provide supplementary information as an appendix in this document, and provide an internal link where appropriate.]

[If this is already specced, link to the relevant section of the spec.]

[If spec work is in progress, link to the PR or draft of the spec.]

## [API 2]

[etc.]

## Key scenarios

[If there are a suite of interacting APIs, show how they work together to solve the key scenarios described.]

### Scenario 1

[Description of the end-user scenario]

```js
// Sample code demonstrating how to use these APIs to address that scenario.
```

### Scenario 2

[etc.]

## Detailed design discussion

### [Tricky design choice #1]

[Talk through the tradeoffs in coming to the specific design point you want to make.]

```js
// Illustrated with example code.
```

[This may be an open question,
in which case you should link to any active discussion threads.]

### [Tricky design choice 2]

[etc.]

## Considered alternatives

[This should include as many alternatives as you can,
from high level architectural decisions down to alternative naming choices.]

### [Alternative 1]

[Describe an alternative which was considered,
and why you decided against it.]

### [Alternative 2]

[etc.]

## Stakeholder Feedback / Opposition

[Implementors and other stakeholders may already have publicly stated positions on this work. If you can, list them here with links to evidence as appropriate.]

- [Implementor A] : Positive
- [Stakeholder B] : No signals
- [Implementor C] : Negative

[If appropriate, explain the reasons given by other implementors for their concerns.]

## References & acknowledgements

[Your design will change and be informed by many people; acknowledge them in an ongoing way! It helps build community and, as we only get by through the contributions of many, is only fair.]

[Unless you have a specific reason not to, these should be in alphabetical order.]

Many thanks for valuable feedback and advice from:

- [Person 1]
- [Person 2]
- [etc.]