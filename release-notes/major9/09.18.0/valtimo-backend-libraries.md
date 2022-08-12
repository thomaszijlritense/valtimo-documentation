# Backend libraries 9.18.0 RC

## New Features

The following features were added:

* **Custom FormFieldDataResolvers**

  Support was added for creating ExternalFormFieldResolvers that implement a new support(String name) method.
  Previously, an enum `ExternalFormFieldType` denoted the prefixes that were supported, which prevented
  implementations from making custom prefixes. Information on how to use form field data resolvers
  can be found [here](/using-valtimo/form-link/using-form-field-data-resolvers.md), and information on
  how to create custom form field data resolvers can be found [here](/extending-valtimo/form-link/custom-form-field-data-resolver.md).

* **Plugin categories**

  Plugins can now be categorized. This is done by annotating an interface, which plugins can then implement, e.g.
  `@PluginCategory(key = "category-key-here")`. A plugin that implements more than one interface with a category will
  belong to both categories.

  This allows for plugins to rely on other plugins. More information on this feature can be found
  [here](/extending-valtimo/plugin/custom-plugin-definition.md#plugin-categories).

* **Added new ZGW plugins**
  * openzaak
    * This plugin allows other plugins to authenticate with openzaak
  * documenten-api
    * This plugin can make a connection to the Documenten API. When a document was generated this plugin is used to 
    upload the document to the Documenten API
  * zaken-api
    * This plugin can make a connection to the Zaken API. This plugin supports the action to link documents that have been uploaded 
    to the Documenten API to the Zaak of the current case

## Bugfixes

The following bugs were fixed:

* **'No form linked' when a start form has been linked**

  For some cases, it was no longer possible to manually create a new case because of a popup saying that there was no
  start form configured even though it had been configured. The logs would show an 500 Internal Server Error.

## Breaking changes

No known breaking changes.

## Deprecations

The following was deprecated:

* **FormFieldDataResolver supports method**

  FormFieldDataResolver `supports(ExternalFormFieldType externalFormFieldType)` was deprecated and is replaced with 
  `supports(String externalFormFieldType)`.

## Known issues

No new known issues.