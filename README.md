# Wren:AM Documentation

This repository hosts the documentation source for Wren:AM.
The documentation follows the [Wren Security documentation conventions](https://github.com/WrenSecurity/wrensec-docs/wiki/Documentation-Conventions); this file describes only the conventions specific to this project.

## Building

```sh
npm ci
npm run build
```

The site is generated into `build/site`.
The build reads the checked-out working tree, so uncommitted changes are included.

## Structure

Each type of documentation is an Antora module under `modules/`:

* `ROOT` – introduction, getting started and community pages.
* `components` – the Reference Guide.

Modules for other types of documentation are added when there is content for them.

### Reference Guide

Pages of the Reference Guide are placed by feature area:

* `authentication/index.adoc` – the authentication service, modules and chains.
* `authentication/modules/<module>.adoc` – one page per authentication module, named after the module.
* `<area>/<feature>.adoc` or `<component>.adoc` – other features and components, e.g. `oauth2/token-introspection.adoc` or `radius-server.adoc`.

Every new page is added to `modules/components/nav.adoc`.
