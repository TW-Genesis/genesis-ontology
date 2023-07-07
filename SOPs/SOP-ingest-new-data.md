# SOP: Ingesting new data into Genesis-DB

## Purpose

This standard operating procedure (SOP) details how to ingest a new dataset to Genesis-DB. The dataset is not assumed to be structured or of a particular form. As such, the scope of this SOP does not extend to describing specific mapping procedures between datasets and ontology terms. Implementing these methods in Apache Jena is also beyond the scope of this SOP.

## How to ingest a new static dataset

1. Identify data that are desired to ingest.
2. Map these data fields to ontology terms. See Case A if unable to map all fields.
3. Extract data from source and either:
    1. parse to `.ttl`, then load into Genesis-DB; or
    2. use SPARQL to write directly to Genesis-DB.
4. Write and run some test queries to verify the data is ingested as expected.

## How to setup a new data stream for ingestion

1. Using a static representative sample of, or a specification for the stream:
   1. identify data that are desired to ingest; then
   2. map these data fields to ontology terms. See Case A if unable to map all fields.
2. Run a test ingestion, using the static sample or a test stream.
3. Write and run test queries to verify the stream is ingesting as expected.

## Case A: unable to map fields to ontology terms

1. Follow the SOP for updating and creating new ontology terms.
2. Return to step 2. above.