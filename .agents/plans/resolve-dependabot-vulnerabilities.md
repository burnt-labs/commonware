# Resolve Dependabot vulnerabilities

## Goal

Resolve every open Dependabot alert on the active Burnt Labs Commonware fork without changing runtime behavior outside dependency upgrades.

## Plan

1. Apply the complete MCP dependency upgrade and verify that the vulnerable AI SDK and lodash packages leave the lockfile.
2. Update both Dylint lockfiles to the patched `tar` release.
3. Validate a frozen MCP install, npm audit, MCP CI checks, Rust lockfile integrity, and the final diff.
4. Publish one security PR and verify its mergeability and hosted checks.

## Safety boundary

Do not suppress advisories or retain compatibility fallbacks. An alert is resolved only when the vulnerable package version is absent or replaced by a patched release.
