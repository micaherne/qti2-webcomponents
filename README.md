qti2-webcomponents
==================

*NB This project is under heavy development and does not work as described in this document*

Overview
--------

This is a set of Web Components Custom Elements for QTI 2.1 interactions and other related
content. The idea is to be able to copy an `itemBody` from a QTI item and for it to work
as-is in the browser. (Unfortunately, due to how the custom elements spec defines valid
tag names, all QTI element names must be prefixed with "qti2-".)

Demo Quick Start
----------------

1. Import all components: `<link rel="import" href="qti2-webcomponents/qti2-webcomponents.html">`
2. Add a QTI2 `itemBody` to your page (with all QTI element names rewritten to have
   the "qti2-" prefix
3. View the page in the browser

Interactions will be displayed as custom user interface components and can be used, although
in this demo configuration they will manage their own variables, so some features may not
work as expected.

Item Session Variables
----------------------

For full functionality, many of the components require access to either the item's variable
declarations, or the actual value of variables from the "item session" as described in the
QTI spec.

These can be provided by adding a qti2-controller component to your page. This can be 
configured to either:

a. manage a previously-defined Javascript object, or
b. use a well-defined REST interface to get the current value of the variables from a 
   web service
   
(only the first is currently implemented)
