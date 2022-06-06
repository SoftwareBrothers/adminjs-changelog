# AdminJS Changelog – May 2022

Hey everyone, and welcome to our monthly recap of what has changed in AdminJS in May 2022.

## adminjs
- fixed issues in bulk action type;
- added an option in `AdminJSOption`s to set a default 'perPage' setting;
- fixed an issue where an empty record was being returned on error.

## @adminjs/mongoose
- now uses `estimatedDocumentCount` instead of `count` ([@rseibane](https://github.com/rseibane)).

## @adminjs/express
- fixed a bug where you could access UI of protected routes while being signed out.

## Coming soon
We're preparing for a beta roll out for v6 of AdminJS core and v3 of Design System in the nearest future. Here's what you can expect, amongst other things:
- React version will be updated to the most recent React 18 across all AdminJS repositories;
- `@adminjs/themes` - a repository with predefined AdminJS themes will be added;
- ThemeGenerator - a tool that allows you to customize or build your custom themes will be added;
- `Select` input field will be moved to Design System - you'll be able to use it in your custom components;
- `Phone` input field will be added to Design System and AdminJS core via `phone` property type;
- `Currency` input field will be added to Design System and AdminJS core via `currency` property type;
- `DatePicker` input field will be rewritten to allow you to type in the date/datetime using text input;
- `RichText` input field will no longer be using Quill, it will be using TipTap instead.

🔮 And as a little sneak peek: we already started working on the next major release – v7 – in which we'll be focusing on rewriting AdminJS architecture to make admin panel customization even easier. So stay tuned!
