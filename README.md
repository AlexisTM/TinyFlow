# TinyFlow
Tiny Flow is a visual programming language based on states and flow.

It consists of the following:
* Web based UI to design the flow (On the web or Electron)
* Flow to a generic JSON(?) representation
* Client  libraries in each language that can handle the JSON (or other) at different levels
* Flow validity check

Minimal capabilities to be called client library:
* Flow import
* Base state (to be extended)
* Base extensions (to be extended)
* Going through the states based on the flow
* Examples

Optional features:
* Flow export
* Flow status update (Which protocol?)
* Standard states/extension as a reference
* Event implementation


It first aims autonomous behaviour; yet could be used with any language on any platform.

Design
--------

### Starting points (+ events)

It marks the start of the states to be executed. The main starting point is started by default. The non-main starting points are events triggered by internal or external call; with priorities. (Low Battery; Communication lost; ...)

### States

Each state have the following functions;
* **void before(...):** Called before the loop
* **void loop(...):** Main loop
* **void after(...):** Called after the loop
* **... next(...):** Called just before switching to the next state
* **void constructor(...):** Called on creation of the state
* **bool isDone(...):** Called once after the after function to check if the state logic is finished

Each state have the following parameters;
* **float timeout:** Maximum time for the state to be executed before being set to Done
* **float duration:** Time to wait after the logic of the state is finished to end the state.
* **... &global:** A global complex object available for every states. (Like self for an object; it is the current UAV state for example) *Should it be const&?*

### Ending points

Just a state. What should we do here? Isn't a state enough? Do we notify that we need another state starting point to run?

FAQ
--------

**Why did you make TinyFlow?**

The TinyFlow library comes from the urge to have an easier way to define some autonomous behaviour and events; It also allows more complex behaviour like: "While x available; do y()".

**I can code. Why would I use TinyFlow**

TinyFlow does not aim to replace programming. Instead, it proposes a high level representation of the application you are building. You can create the states and reprogram them and use them as a flow.

For example, if you have to deal with dynamic behaviour or error handling; if/else are not a pretty solution.

Other libraries used
----------

* [PaperJS](http://paperjs.org) v0.11.5 full

Credits
----------

* AlexisTM
