# Predictive Test Selection - post-merge strategy

This repository illustrates how [Develocity Predictive Selection feature](https://docs.gradle.com/enterprise/predictive-test-selection/) can be implemented with a post-merge strategy.

## Implementation

### Main Build

Builds of the main branch happen with PTS enabled and remaining tests selection.

See the [workflow file](./.github/workflows/main-build.yml) for more details.

### PR Build

PR builds happen with PTS enabled and [relevant tests](https://docs.gradle.com/enterprise/predictive-test-selection/#relevant-vs-remaining-tests) selection.

See the [workflow file](./.github/workflows/pr-build.yml) for more details.

## Characteristics

### Pros
- Maximize number of builds accelerated with PTS
- Easy to implement

### Cons
- Risk if main branch build failures are not monitored closely