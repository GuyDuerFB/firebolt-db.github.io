---
layout: default
title: Release notes
description: Latest release notes for the Firebolt data warehouse.
parent: General reference
nav_order: 1
has_toc: false
has_children: false
---

# Release notes

Firebolt continuously releases updates so that you can benefit from the latest and most stable service. These updates might happen daily, but we aggregate release notes to cover a longer time period for easier reference. The most recent release notes from the latest version are below. 

- See the [Release notes archive](../release-notes/release-notes-archive.md) for earlier-version release notes.

{: .note}
Firebolt might roll out releases in phases. New features and changes may not yet be available to all accounts on the release date shown.

## DB version 3.31
**February 2024**

* [New features](#new-features)
* [Enhancements, changes, and new integrations](#enhancements-changes-and-new-integrations)
* [Resolved issues](#resolved-issues)

### New features

<!--- FIR-22307 ---> **PG compliant division**

LQP2 now has a new division operator that is PG compliant, by default.

<!--- FIR-29179 ---> **Prevents usage of new line delimeter for schema inference.**

An error will now occur if schema inference is used with the option “delimiter” set to something other than the default. 

### Enhancements, changes and new integrations

<!--- FIR-29747 ---> **Disabled Unix Time Functions**

The following functions will not be supported anymore:
- from_unixtime
- to_unix_timestamp
- to_unix_time

<!--- FIR-27548 ---> **Simplified table protobuf representation**



### Resolved issues

* Indirectly granted privileges have been removed from the `information_schema.object_privileges` view. 

* Fixed an issue where `ARRAY_FIRST` and `ARRAY_FIRST_INDEX` returned an error if the given input was nullable.