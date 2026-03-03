# Spotify System Design — Diagram Checklist

These diagrams should be created in Figma using the step-by-step progressive reveal approach.
Each diagram builds on the previous one, adding new components.

## High Level Design Diagrams (Step-by-Step)

| # | Filename | Description | Components to Show |
|---|----------|-------------|--------------------|
| 1 | `Intro_1.png` | Simple illustration showing music streaming challenges | User with phone, multiple backend services, latency/scale icons |
| 2 | `Intro_2.png` | High-level overview of the full system | Simple block diagram showing major subsystems |
| 3 | `Audio_Upload_And_Ingestion.png` | Upload → S3 → Transcode → CDN pipeline | Artist, Upload Service, S3, Transcoding Queue, Transcoding Service, CDN |
| 4 | `Music_Streaming_And_Playback.png` | User → Streaming Service → CDN → Client buffering | Client App, Streaming Service, Metadata Service, CDN Edge, Buffer diagram |
| 5 | `Search_System.png` | Search query flow through Elasticsearch | Client, Search Service, Elasticsearch cluster, result types |
| 6 | `Recommendation_Engine.png` | Full recommendation pipeline | Event Ingestion, Kafka, Flink, Spark, Data Warehouse, Feature Store/Redis, Home Feed Service |
| 7 | `Playlist_Service.png` | Playlist CRUD and caching | Client, Playlist Service, PostgreSQL, Redis cache, Kafka events |
| 8 | `User_Interaction_And_Social.png` | Social features and friend activity | User Service, Activity DB, Redis presence, WebSocket, Kafka |
| 9 | `Final_Design.png` | Complete system with all components and numbered steps | Everything combined |

## Deep Dive Diagrams

| # | Filename | Description |
|---|----------|-------------|
| 10 | `Adaptive_Bitrate_Streaming.png` | Show chunk manifest, bitrate switching logic, buffer monitoring |
| 11 | `CDN_Caching_Strategy.png` | Three-tier caching: Edge → Regional → Origin (S3) |
| 12 | `Discover_Weekly_Pipeline.png` | 5-step pipeline: Collect → Taste Profile → Candidates → Rank → Assemble |

## Figma Layer Naming Convention

For the step-by-step video animation approach, name layers as:
- `step-1-client` — Client/User icon
- `step-2-upload-service` — Upload Service box
- `step-3-s3-storage` — S3 storage
- `step-4-transcoding` — Transcoding queue + service
- `step-5-cdn` — CDN edge servers
- etc.

This allows progressive reveal in Figma prototyping for video production.
