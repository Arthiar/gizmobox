# Gizmobox Project

This project builds a simple data pipeline for Gizmobox.

It starts with raw data in the landing area, moves it to bronze tables and views, cleans it into silver tables, and then joins key data into gold tables.

## Project flow

* Landing: raw files are stored in volumes and cloud storage
* Bronze: raw customer, order, address, payment, refund, and membership data is loaded
* Silver: raw data is cleaned and shaped into better tables
* Gold: final business-ready tables are created for reporting and analysis

## Main folders

* `dea_01_unity_catalog` - sets up catalog, schemas, volumes, and storage access
* `dea_02_etl_with_spark_to_bronze` - loads raw source data into bronze views and tables
* `dea_03_etl_with_spark_to_silver` - cleans and transforms bronze data into silver tables
* `dea_03_etl_with_spark_to_gold` - joins silver data into final gold tables

## Data used so far

* Customers
* Orders
* Membership files
* Addresses
* Payments
* Refunds

## Current output

So far, the project creates bronze, silver, and gold objects in the `gizmobox` catalog.

Examples include:

* `gizmobox.bronze.v_customer`
* `gizmobox.bronze.v_orders`
* `gizmobox.bronze.v_membership`
* `gizmobox.silver.customer`
* `gizmobox.silver.payments`
* `gizmobox.silver.refunds`
* `gizmobox.silver.membership`
* `gizmobox.silver.address`
* `gizmobox.silver.orders_json`
* `gizmobox.silver.orders`
* `gizmobox.gold.customer_address`

## Notes

This README is a simple project summary for the work completed so far.
