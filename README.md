# DistributedKV — Java Distributed Key-Value Store

A Java implementation exploring replicated key-value storage, Multi-Raft consensus, configurable storage engines, and distributed read paths.

## Core Components

- **Consensus**: Raft nodes/groups, logs, snapshots, and replicated state machines
- **Data placement**: consistent hashing and cluster management
- **Storage**: RocksDB, in-memory engines, and MVCC-related components
- **Networking**: Netty-based server and client protocol
- **Read paths**: ReadIndex and follower-read implementations
- **Tests**: unit/integration and benchmark source code under `src/test`

## Project Layout

- `src/main/java/com/distributedkv/raft/`: Raft consensus
- `src/main/java/com/distributedkv/storage/`: storage engines
- `src/main/java/com/distributedkv/network/`: networking
- `src/main/java/com/distributedkv/server/`: server orchestration
- `docs/`: design, API, deployment, and performance notes

## Build

Requires Java 11+ and Gradle 7+. Run `gradle build` from the repository root.

> **Verification needed:** The supplied project has an empty `src/main/java/com/distributedkv/Main.java` despite an `application.mainClass` setting, and no Gradle wrapper was included. Build/run behavior has not been verified.

## Performance

The project includes benchmark and performance-test sources; any throughput, availability, or latency numbers should be published only alongside reproducible commands, environment details, and measured output. The original README's performance claims have been intentionally omitted pending validation.

## Security

Default keystore/truststore password strings in the supplied configuration were replaced with placeholders. Configure real credentials securely before deployment.

## Validation status

This source snapshot is a work in progress. No build, unit tests, distributed correctness tests, or benchmark runs passed as part of this publication review. The Java entry point is empty and no Gradle wrapper is included. The documentation describes design intentions and requires reconciliation with runtime behavior.
