<div align="center">
  <img alt="AdminJS Changelog - April 2022" src="https://adminjs.co/img/a.svg">
</div>

# AdminJS Changelog – April 2022

Hey everyone and welcome to our monthly recap of what has changed in AdminJS in April 2022.

## adminjs – v5.10.0
- You can now translate 'Dashboard' in breadcrumbs. The translation key is `dashboard` under global `messages`;
- Added support for assets versioning. This is optional, but is something you might want to do if you are hosting and caching JavaScript browser bundles behind a CDN. The versioning can be done manually or with the help of @adminjs/bundler. In order to use this feature you have to add `coreScripts` under `assets` in your AdminJS options;
- Added `showResourceActions` to resource action's config. This is set to `true` by default. Disabling this will cause resource actions (top right corner of an action view) to be hidden under a specific action. You might want to hide resource actions in record action context to avoid confusion.
- Added 'Filter' button to custom resource actions in case you need to access filters. The filter button is displayed if there is `showFilter: true` set in action's config;
- Updated localization implementation, meaning AdminJS can now come with many standard translations included. Language selector has not been included yet but will be coming in the future;
- Added Ukrainian (ua) locale;
- Added simplified Chinese (ch-ZN) locale (thanks to [@panda2134](https://github.com/panda2134));
- Modified the implementation of resource's back button. When you navigate, `from` and `to` paths are now stored in Redux store and can be accessed globally;
- When you submit or reset your filters, the filter drawer will be closed. Additionally, when you navigate to a URL with filters in search params, the filter drawer will no longer open automatically;
- Fixed how `new` and `edit` actions are differentiated on the frontend. This solved a rare problem where a resource with manually-inputted primary key would trigger an `edit` action instead of `new`;
- Added new AdminJS environment variable: `ADMIN_JS_TMP_DIR` – in case you want to change the default `.adminjs` directory to a different path;
- Resource's name in breadcrumbs will no longer navigate to `list` action if it is disabled. Instead, it will be just text;
- You can now change a tooltip's position for property's description. You can do this by specifying `custom.tooltipDirection` in your property's options.

## @adminjs/typeorm – v3.0.0
- You can now filter records by UUID columns;
- Version 3.0.0 has been released thanks to [@asheliahut](https://github.com/asheliahut). The new version adds support for TypeORM ~v0.3.0. Because of this, new releases of @adminjs/typeorm will no longer support older versions.

## @adminjs/design-system – v2.2.4
- Added a new input component: [CurrencyInput](https://github.com/SoftwareBrothers/adminjs-design-system/pull/35);
- Carbon Icons updated to the latest version;
- Fixed a bug when a tooltip position was always relative to the initial position on the screen which caused its misplacenebt while scrolling;
- Updated record actions buttons `(DropDownItemWithButtons, SingleButtonInGroup)` to show a spinner ("Fade" icon) when you press the button. It should help to display that an action is in progress when you use a non-instant action that has no action component in AdminJS.

## @adminjs/import-export – v1.3.2
- Cleaned up the build, the Example App is now excluded from the library after its built, and pathing is correct again;
- Added a default `sortBy` param which is used when fetching records. The results are now always sorted by either primary key or title property. The cause of this change is that some adapters, eg @adminjs/typeorm required `sortBy` to be present.

## @adminjs/passwords – v2.0.2
- Added translations to the package. You can now rename the buttons.

## @adminjs/bundler – v1.2.0
- Added support for automatic assets versioning. If you specify `versioning.manifestPath`, the script will create an assets manifest file at a given path. The file will contain the mappings of AdminJS JavaScript bundles to their versioned counterparts, eg `global.bundle.js` vs `global.bundle.1650890848033.js`.

## @adminjs/logger - v2.2.0
- Added support for logging `new` and `bulkDelete` actions.

## @adminjs/koa – v2.1.0
- You can now specify `Session Options` when creating an authenticated router.
