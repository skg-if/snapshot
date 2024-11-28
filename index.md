---
title: Snapshot
layout: default
nav_order: 6
---

# Snapshot guidelines

For the sake of simplicity, JSON-LD has been chosen as a reference data format for the exchange as suggested by the examples described in the core model entities.

As a first step, adopters of the SKG-IF can expose their mapped data as a bulk `.zip` file (all-inclusive) where records are serialised in JSON and split across different `part` files.
Each part file contains 10,000 SKG-IF records in JSON lines format.
Part files are grouped into folder whose name indicates the range of the part files contained.
In this way, each folder will contain 10 million SKG-IF records in total.
The naming for part files and the subfolders is not binding.
To ease the consumption of such a file, the following structure has been agreed and should be followed when exposing data in this way.

```
./snapshot.zip
├── /products
│   ├── /00000-00999
│   │   ├── part_00000.jsonl
│   │   ├── part_00001.jsonl
│   │   ├── ...
│   │   └── part_00999.jsonl
│   ├── /01000-01999
│   │   ├── part_01000.jsonl
│   │   ├── part_01001.jsonl
│   │   ├── ...
│   │   └── part_01999.jsonl
│   └── /...
├── /agents
│   ├── /00000-00999
│   ├── /01000-01999
│   └── /...
└── /...
```
