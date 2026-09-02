# Hi, I'm Huiyu

Software engineer working on backend and distributed systems, with a background in large-scale geospatial data infrastructure and applied ML.

Recently I built an end-to-end asynchronous fraud-detection workflow for a credit-card scanning mobile SDK at a fintech startup — decoupling server-side ML inference from the synchronous scan path cut scan-to-response latency by over 75%. The interesting part was less the model than the lifecycle around it: API contracts and inference state transitions spanning a Java/Kotlin Android SDK and a Node.js backend, pending-result handling, and a server-to-server decision API that let merchants read results precomputed at scan time — all without breaking live partner integrations.

Before that I built a weather-risk data platform on AWS. Spark/Sedona pipelines aligned four heterogeneous raster and vector sources onto a common grid; the storage layer was split by access pattern across PostgreSQL/PostGIS, TimescaleDB, and S3, holding p95 query latency under 200 ms; and containerized services kept GPU downscaling inference isolated from the latency-sensitive APIs and alerting in front of it. Earlier, at TGS (an energy data analytics company), I moved 20 TB of simulation output and offshore sensor observations through parallel Python/Xarray/Dask pipelines on GCP, where rethinking Zarr and Parquet layouts and chunking cut processing time by 70%.

I came to software engineering from research. My Ph.D. was in climate science, where I spent six years writing distributed Python pipelines over 100+ TB of satellite and model data on multi-node Slurm HPC clusters — which is where I learned that most interesting problems are systems problems.

**Currently:** M.S. in Computer Science at Georgia Tech (Dec 2026), looking for software engineering/data engineering roles.

## Things I've built for fun

**[Synchronized Distributed File System](https://liuxhy.github.io/portfolio/1-distributed-file-system/)** · `C++` `gRPC` `Protobuf` `inotify` `pthreads`
An AFS-style DFS with whole-file client caching under single-writer semantics — CRC32 checksums paired with mtime comparison to skip redundant transfers, chunked streaming with gRPC deadlines for 100 MB+ files, and a persistent async callback stream that pushes updates instead of polling. Lock ownership is enforced on every write, with cleanup restoring server state after mid-write client crashes.

**[Multi-Agent Travel Planner](https://github.com/liuxhy/trip_planner_agent)** · `Python` `Google ADK` `Gemini 2.5` `Streamlit`
Eight agents composed into a sequential pipeline with hierarchical delegation, exposing flight, hotel, and activity agents as callable tools to a lead planner grounded on live weather and search APIs. A bounded critic-refiner loop validates itineraries against drive-time realism, transport consistency, and daily pacing before export.

## What I work with

**Languages**: `Python` `C++` `Java/Kotlin` `TypeScript` `SQL`

**Systems**: gRPC · Protobuf · concurrency · Dask · Spark/Sedona · Docker · Linux

**Web & mobile**: FastAPI · Node.js · React · Android SDK · REST

**Cloud**: AWS (EC2, S3, Lambda, RDS, Glue, CloudWatch) · GCP (Vertex AI, Cloud Run, GCS) · GitHub Actions

**Data & ML**: PostgreSQL/PostGIS · TimescaleDB · Xarray · Zarr · Parquet · PyTorch · scikit-learn

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/xinhuiyu-huiyu-liu) ·
[Website](https://liuxhy.github.io) ·
[Google Scholar](https://scholar.google.com/citations?user=0fies7oAAAAJ&hl=en)
