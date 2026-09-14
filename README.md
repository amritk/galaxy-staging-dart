# DemoApiScalarGalaxy Dart API Library

This package provides convenient access to the DemoApiScalarGalaxy REST API from Dart applications.
It is generated from your OpenAPI document with typed models, resource clients, pagination helpers, and Dart 3 support.

The full generated API reference is available in `api.md` and the operation inventory is available in `reference.md`.

## Installation

```sh
dart pub add <published-package-name>
```

## Usage

Instantiate the generated client and call async methods from resource clients.

```dart
import 'package:demo_api_scalar_galaxy/demo_api_scalar_galaxy.dart';

Future<void> main() async {
  final client = DemoApiScalarGalaxy();
  // await client.planets;
}
```

## Request and Response Types

Request params and response bodies are generated as null-safe Dart classes with explicit JSON conversion helpers.
Resource methods return `Future<T>`, `Page<T>`, stream wrappers, or bytes depending on the OpenAPI response.

## Handling Errors

Non-success responses throw `ApiException` subclasses that expose status code, headers, raw body, and request id metadata when available.
Transport failures are represented by `APIConnectionError`.

## Retries and Timeouts

Per-request `RequestOptions` can configure timeout, retry, headers, query params, and base URL overrides.
Retryable responses honor `Retry-After` before exponential backoff.

## Pagination

Paginated operations return `Page<T>` values with `hasNextPage()` and `getNextPage()` helpers when pagination metadata is available.

## Raw Responses and Custom Requests

Each resource exposes `withRawResponse` helpers for callers that need status, headers, or unparsed response bodies.
Per-request headers and query params provide an escape hatch for undocumented API fields.

## Requirements

Requires Dart 3.
