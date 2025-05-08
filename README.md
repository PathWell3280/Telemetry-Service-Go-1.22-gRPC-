# Telemetry Service (Go 1.22 / gRPC)

## Overview
This microservice ingests telemetry events via gRPC streaming at **50 000 events/sec**, pseudonymizes user IDs using **SHA-256** (ISO 27701 §7), and exposes **Prometheus** metrics for SRE monitoring.

## Features
- **gRPC** `StreamEvents` RPC for high-throughput ingestion
- **SHA-256** pseudonymization of user identifiers
- **ISO 27701 §7** compliant pseudonymization
- **Prometheus** metrics endpoint (`/metrics`)
- **SRE-ready**: health checks, metrics, configurable concurrency

## Prerequisites
- Go **1.22**
- Protocol Buffers **v3** with `protoc-gen-go`, `protoc-gen-go-grpc`
- `protoc` compiler

## Setup

1. **Clone** the repo:
   ```bash
   git clone https://github.com/yourorg/telemetry_service.git
   cd telemetry_service
