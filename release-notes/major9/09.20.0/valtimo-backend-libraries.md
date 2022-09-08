# Backend libraries 9.20.0 (RC)

## New Features

The following features were added:

* **Additional method for finding documents from within a process**

  The `search` method in the `JsonSchemaDocumentSearchService` does not work when retrieving a document if no
  authorization is found. A new method, `searchWithoutAuthorization` is now available. For classes that implement the 
  `DocumentSearchService`, this method has a default and only needs to be implemented if this use case is necessary.

## Bugfixes

No bugfixes.

## Breaking changes

No breaking changes.

## Deprecations

No new deprecations.

## Known issues

No new known issues.