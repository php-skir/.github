<p align="center">
    <a href="https://github.com/php-skir">
        <img src="https://raw.githubusercontent.com/php-skir/.github/main/art/branding/skir-rides-php-elephant.svg" alt="Skir riding the PHP elephant" width="600">
    </a>
</p>

<h1 align="center">Bring Skir's type-safe workflow to PHP.</h1>

<p align="center">
    Generate PHP contracts from <code>.skir</code> schemas, expose them from Laravel, and consume them with typed PHP or TypeScript clients.
</p>

<p align="center">
    <a href="https://github.com/php-skir/server#quick-start">Get started with Laravel</a>
    ·
    <a href="https://skir.build/">Explore Skir</a>
</p>

## What is Skir?

[Skir](https://skir.build/) is a schema language for defining data models and APIs once, then generating idiomatic, type-safe code across your stack. php-skir brings that workflow to PHP with code generators, Laravel server and client integrations, and a TypeScript runtime for generated clients and services.

## How it fits together

1. **Define** models and RPC methods in `.skir` files.
2. **Generate** typed PHP data objects and contracts.
3. **Serve** procedures through ordinary Laravel controllers.
4. **Consume** them from typed PHP or TypeScript clients.

## Laravel integrations

| Repository | Use it to |
| --- | --- |
| [`php-skir/server`](https://github.com/php-skir/server) | Expose generated SkirRPC methods from Laravel controllers. |
| [`php-skir/client`](https://github.com/php-skir/client) | Consume SkirRPC services through a typed Laravel client powered by [Saloon](https://docs.saloon.dev/). |

## PHP generators

| Repository | Generates |
| --- | --- |
| [`skir-laravel-data-generator`](https://github.com/php-skir/skir-laravel-data-generator) | [Spatie Laravel Data](https://spatie.be/docs/laravel-data) objects, typed RPC clients, and server contracts. |
| [`skir-php-generator`](https://github.com/php-skir/skir-php-generator) | Framework-agnostic PHP objects, typed RPC clients, and server contracts. |
| [`skir-simple-data-objects-generator`](https://github.com/php-skir/skir-simple-data-objects-generator) | Immutable DTOs built on [`std-out/simple-data-objects`](https://github.com/std-out/simple-data-objects), typed RPC clients, and server contracts. |

## TypeScript

[`@php-skir/skir-client`](https://github.com/php-skir/typescript-client) is the runtime used by generated TypeScript clients and services. It supports Skir's default transport as well as opt-in CBOR request and response bodies.

> [!NOTE]
> CBOR is a php-skir ecosystem extension and is not part of upstream Skir's standard RPC transport. Enable it on both sides of a connection; otherwise, keep the default transport for upstream compatibility.
