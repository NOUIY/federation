# CHANGELOG for `federation-integration-testsuite-js`

## 2.11.2

## 2.11.1

## 2.11.0

### Minor Changes

- Adds connect spec v0.2, available for use with Apollo Router 2.3.0 or greater. ([#3262](https://github.com/apollographql/federation/pull/3262))

## 2.11.0-preview.2

### Patch Changes

- Preparing preview.2 release ([#3255](https://github.com/apollographql/federation/pull/3255))

## 2.11.0-preview.1

## 2.11.0-preview.0

### Minor Changes

- Add connect spec v0.2 ([#3228](https://github.com/apollographql/federation/pull/3228))

## 2.10.0

### Minor Changes

- Adds the ability to compose and serialize directives for [Apollo Connectors](https://go.apollo.dev/connectors). To use Apollo Connectors, compose your supergraphs using [GraphOS](https://www.apollographql.com/docs/graphos/platform/schema-management) or [rover](https://www.apollographql.com/docs/rover/commands/dev), and run your supergraph in [Apollo Router](https://www.apollographql.com/docs/graphos/routing) 2.0.0 or higher. ([#3215](https://github.com/apollographql/federation/pull/3215))

## 2.9.3

## 2.9.2

## 2.9.1

## 2.9.0

## 2.8.5

## 2.8.4

## 2.8.3

## 2.8.3-beta.2

## 2.8.3-beta.1

## 2.8.3-beta.0

## 2.8.2

## 2.8.1

## 2.8.0

### Patch Changes

- Various set context bugfixes ([#3017](https://github.com/apollographql/federation/pull/3017))

## 2.8.0-alpha.1

## 2.8.0-alpha.0

## 2.7.8

### Patch Changes

- Triggering a clean 2.7.8 release now that harmonizer build has been fixed. ([#3010](https://github.com/apollographql/federation/pull/3010))

## 2.7.7

### Patch Changes

- No logical changes since 2.7.5 or 2.7.6, but we fixed a bug in the release process, so we need to publish a new patch version (2.7.7). ([#2999](https://github.com/apollographql/federation/pull/2999))

## 2.7.6

## 2.7.5

## 2.7.4

## 2.7.3

## 2.7.2

### Patch Changes

- Add new `generateQueryFragments` option to query planner config ([#2958](https://github.com/apollographql/federation/pull/2958))

  If enabled, the query planner will extract inline fragments into fragment definitions before sending queries to subgraphs. This can significantly reduce the size of the query sent to subgraphs, but may increase the time it takes to plan the query.

## 2.7.1

## 2.7.0

## 2.6.3

## 2.6.2

## 2.6.1

## 2.6.0

### Minor Changes

- Update `license` field in `package.json` to use `Elastic-2.0` SPDX identifier ([#2741](https://github.com/apollographql/federation/pull/2741))

- Introduce the new `@policy` scope for composition ([#2818](https://github.com/apollographql/federation/pull/2818))

  > Note that this directive will only be _fully_ supported by the Apollo Router as a GraphOS Enterprise feature at runtime. Also note that _composition_ of valid `@policy` directive applications will succeed, but the resulting supergraph will not be _executable_ by the Gateway or an Apollo Router which doesn't have the GraphOS Enterprise entitlement.

  Users may now compose `@policy` applications from their subgraphs into a supergraph.

  The directive is defined as follows:

  ```graphql
  scalar federation__Policy

  directive @policy(
    policies: [[federation__Policy!]!]!
  ) on FIELD_DEFINITION | OBJECT | INTERFACE | SCALAR | ENUM
  ```

  The `Policy` scalar is effectively a `String`, similar to the `FieldSet` type.

  In order to compose your `@policy` usages, you must update your subgraph's federation spec version to v2.6 and add the `@policy` import to your existing imports like so:

  ```graphql
  @link(url: "https://specs.apollo.dev/federation/v2.6", import: [..., "@policy"])
  ```

## 2.5.7

## 2.5.6

## 2.5.5

## 2.5.4

## 2.5.3

## 2.5.2

## 2.5.1

## 2.5.0

## 2.4.10

## 2.4.9

## 2.4.8

## 2.4.7

## 2.4.6

## 2.4.5

### Patch Changes

- Supersedes v2.4.4 due to a publishing error with no dist/ folder ([#2583](https://github.com/apollographql/federation/pull/2583))

## 2.4.4

## 2.4.3

## 2.4.2

## 2.4.1

### Patch Changes

- Start building packages with TS 5.x, which should have no effect on consumers ([#2480](https://github.com/apollographql/federation/pull/2480))

## 2.4.0

### Patch Changes

- Optimises query plan generation for parts of queries that can statically be known to not cross across subgraphs ([#2449](https://github.com/apollographql/federation/pull/2449))

## 2.4.0-alpha.1

## 2.4.0-alpha.0

## 2.3.5

## 2.3.4

## 2.3.3

## 2.3.2

## 2.3.1

# This is a private package, so this may be kept empty, but exists so that `changesets` will not complain
