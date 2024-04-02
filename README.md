# Ultimate Data Processing Actor: Merge, Dedup & Transform

This refined and optimized actor is designed for large-scale merging, deduplication, and transformation of datasets.

## Why Use This Actor
- **Speed:** Experience extremely fast data processing, thanks to parallelized workloads—up to 20x faster than standard methods.
- **Efficiency:** Read from multiple datasets simultaneously, making it ideal for merging post-scraping.
- **Reliability:** Actor migration proof with persisted steps, ensuring no repeated work or duplicated data.
- **Memory Management:** 'Dedup as loading' mode allows for efficient memory usage, even with huge datasets (10M+).
- **Flexibility:** Deduplicate using multiple fields and nested objects/arrays, with deep equality checks.
- **Storage Options:** Store results in key-value store records.
- **Fast Blank Runs:** Quickly identify duplicates without processing data.

## Merging
Merge items from multiple datasets into a single dataset or key-value store output. In 'Dedup after load' mode, the order of items retains the order of the provided datasets.

## Deduplication
Specify fields for deduplication to remove duplicate items based on field values. Combine multiple fields for more precise deduplication. Deep comparison is used for objects and arrays.

## Transformation
Perform arbitrary data transformations before and after deduplication with `preDedupTransformFunction` and `postDedupTransformFunction`. These functions take an array of items and return a modified array.

Access helper variables and the Apify SDK reference within transformation functions. Customize transformations to suit your needs, whether filtering, adding, or modifying items.

