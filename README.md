# Etcd-Backup-Restore

## Warning about this fork

This fork existence is due to the project [reluctance](https://github.com/gardener/etcd-backup-restore/issues/544) to add metrics to the snapshotter endpoint.
Adding this feature meant breaking the server endpoint as the interop between two subcommands is messy.

/!\ Use this fork at your own risk /!\

[![CI Build status](https://concourse.ci.gardener.cloud/api/v1/teams/gardener/pipelines/etcd-backup-restore-master/jobs/master-head-update-job/badge)](https://concourse.ci.gardener.cloud/teams/gardener/pipelines/etcd-backup-restore-master/jobs/master-head-update-job)
[![Go Report Card](https://goreportcard.com/badge/github.com/gardener/etcd-backup-restore)](https://goreportcard.com/report/github.com/gardener/etcd-backup-restore)
[![GoDoc](https://godoc.org/github.com/gardener/etcd-backup-restore?status.svg)](https://godoc.org/github.com/gardener/etcd-backup-restore)

Etcd-backup-restore is collection of components to backup and restore the [etcd]. It also, provides the ability to validate the data directory, so that we could know the data directory is in good shape to bootstrap etcd successfully.

## Documentation Index

### Usage

* [Getting started](doc/usage/getting_started.md)
* [Manual restoration](doc/usage/manual_restoration.md)
* [Monitoring](doc/usage/metrics.md)
* [Generating SSL certificates](doc/usage/generating_ssl_certificates.md)

### Design and Proposals

* [Core design](doc/proposals/design.md)
* [Etcd data validation](doc/proposals/validation.md)
* [Data restoration](doc/proposals/restoration.md)
* [High watch events ingress rate issue](doc/proposals/high_watch_event_ingress_rate.md)

### Development

* [Setting up a local development environment](doc/development/local_setup.md)
* [Testing and Dependency Management](doc/development/testing_and_dependencies.md)
* [Tests](doc/development/tests.md)
* [Adding support for a new object store provider](doc/development/new_cp_support.md)

[etcd]: https://github.com/etcd-io/etcd
