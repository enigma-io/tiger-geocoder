# Ansible Role for the PostGIS TIGER Geocoder

An Ansible role to configure a PostgreSQL instance with the TIGER Geocoder extension for PostGIS.

## Requirements & Dependencies

* Tested on Ansible 1.7.2
* Ubuntu 14.04
* Postgres 9.3.6
* PostGIS 2.1
* postgis_tiger_geocoder extension for years 2013 and 2014

## Features

* Install `postgis_tiger_geocoder` extension
* Install nation-level geographies and specified state-level geographies

## Requirements

Provisioning tested on:
* Vagrant 1.6.5
* Ansible 1.7.2

Provisioned box tested with:
* Ubuntu 14.04
* Postgresql 9.3.6
* Postgis 2.1

## Install

To automate the build of a default TIGER Geocoder from scratch, see [our TIGER Geocoder Ansible playbook](https://github.com/enigma-io/ansible-tiger-geocoder-playbook).


## Variables

`tiger_mount_point`: Location for raw data download and Postgres data directory.

`tiger_data_directory`: Location for raw TIGER data directory.

`tiger_pg_data_directory`: Location for PostgreSQL data directory.

`tiger_pg_db_name`: The name of the geocoder database. Default is 'geocoder'.

`tiger_year`: Year of TIGER data to load. Tested on `2013` and `2014`.

`tiger_geos`: A list of all possible two-letter State/Territory abbreviations available for propagation into the geocoder.
