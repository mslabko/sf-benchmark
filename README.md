## Test Protocol

**Cluster Resources**

- name: ethos61devva7
- CPU: 16
- RAM: 32 GiB

**Resources Distributions**

- Elastic: 4CPU, 1 GiB memory
- CatalogStorefront service: 4CPU, 4 workers
- Swoole service: 4CPU, X workers, dynamically set by swoole

**Scenarios**

30 seconds load with X concurrent requests, first 10 responses skipped (warmup),
where X - 4 8 16 24 32 which represents 1, 2, 4, 6 8  requests per CPU correspondingly 

Measured 2 different scenarios:
- read from memory, 20 & 100 products in response
- read from Elasticsearch, 20 & 100 products in response

10k products pre-generated  


