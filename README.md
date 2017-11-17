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

FAQ
--------

**I can code. Why would I use TinyFlow**

TinyFlow does not aim to replace programming. Instead, it proposes a high level representation of the application you are building. You can create the states and reprogram them and use them as a flow.

For example, if you have to deal with dynamic behaviour or error handling; if/else are not a pretty solution.

Credits
----------

* AlexisTM
