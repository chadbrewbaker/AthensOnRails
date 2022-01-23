# AthensOnRails
Generator for Cloud object store query infrastructure

## Components
* Translates SQL schema to Athena cloudformation.
* Generates ingestion infra cloudformation - via S3/Kinesis/MSK.  Maps CSV/JSON -> Parqet then writes to the Athena S3 store. Think I upstreamed all blockers so these work https://github.com/domoritz/csv2parquet https://github.com/domoritz/json2parquet
* A cost monitoring script.
* Automation for re-compilation of high cost queries to AWS batch or cached Parquet views.

## Future Enhancements
* Port to GCP infra

--Research--

[POC data tables](https://try.zeek.org/#/tryzeek/saved/556026)

[PrestoSQL Data Types](https://prestodb.io/docs/current/language/types.html)

Athena [EXPLAIN ANALYZE](https://aws.amazon.com/about-aws/whats-new/2021/11/amazon-athena-cost-details-query-execution-plans/)

[Pakt Athena CloudFormation](https://github.com/PacktPublishing/Serverless-Analytics-with-Amazon-Athena)

[AWS Athena workshop CloudFormation](https://athena-in-action.workshop.aws)
