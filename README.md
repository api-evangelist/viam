# Viam (viam)
Viam is a robotics and edge AI platform founded in 2020 by Eliot Horowitz (MongoDB co-founder and former CTO). It pairs viam-server — a gRPC-based runtime that runs on Linux single-board computers (RDK) and ESP32-class microcontrollers (micro-rdk) — with viam.app, a multi-tenant cloud for fleet management, data capture, ML training, and remote operations. Every hardware component (motors, cameras, sensors, arms) and every machine-level service (motion, vision, SLAM, ML inference, navigation) is exposed through a uniform gRPC contract defined in viamrobotics/api with first-class SDKs for Python, Go, Rust, TypeScript, C++, Java, .NET, and Flutter.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/viam/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Robotics, Edge AI, Fleet Management, Computer Vision, Machine Learning, IoT, Embedded, gRPC

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Architecture

| Component | Repo | Language | Role |
|---|---|---|---|
| viam-server (RDK) | [viamrobotics/rdk](https://github.com/viamrobotics/rdk) | Go | Per-machine runtime for Linux SBCs and servers |
| micro-rdk | [viamrobotics/micro-rdk](https://github.com/viamrobotics/micro-rdk) | Rust | Microcontroller variant (ESP32) |
| viam-agent | [viamrobotics/agent](https://github.com/viamrobotics/agent) | Go | System service installing, configuring, updating viam-server |
| API Protobuf | [viamrobotics/api](https://github.com/viamrobotics/api) | Protobuf | Canonical gRPC contract for every Viam API |
| viam.app | https://app.viam.com | Web | Multi-tenant cloud for fleet management |

## SDKs

| Language | Repository |
|---|---|
| Python | [viamrobotics/viam-python-sdk](https://github.com/viamrobotics/viam-python-sdk) |
| Go | [viamrobotics/rdk](https://github.com/viamrobotics/rdk) |
| Rust | [viamrobotics/viam-rust-sdk](https://github.com/viamrobotics/viam-rust-sdk) |
| TypeScript | [viamrobotics/viam-typescript-sdk](https://github.com/viamrobotics/viam-typescript-sdk) |
| C++ | [viamrobotics/viam-cpp-sdk](https://github.com/viamrobotics/viam-cpp-sdk) |
| Java | [viamrobotics/viam-java-sdk](https://github.com/viamrobotics/viam-java-sdk) |
| .NET | [viamrobotics/viam-dotnet-sdk](https://github.com/viamrobotics/viam-dotnet-sdk) |
| Flutter | [viamrobotics/viam-flutter-sdk](https://github.com/viamrobotics/viam-flutter-sdk) |
| Svelte | [viamrobotics/viam-svelte-sdk](https://github.com/viamrobotics/viam-svelte-sdk) |

## APIs

### Viam Fleet Management API
Create and manage organizations, locations, machines, machine parts, fragments, OAuth apps, API keys, and team memberships in the viam.app cloud.

**Human URL:** [https://docs.viam.com/dev/reference/apis/fleet/](https://docs.viam.com/dev/reference/apis/fleet/)

- [Documentation](https://docs.viam.com/dev/reference/apis/fleet/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/v1/app.proto)
- [OpenAPI](openapi/viam-fleet-management-api-openapi.yml)
- [JSON Schema — Organization](json-schema/viam-organization-schema.json)
- [JSON Schema — Location](json-schema/viam-location-schema.json)
- [JSON Schema — Machine](json-schema/viam-machine-schema.json)
- [JSON-LD Context](json-ld/viam-context.jsonld)
- [Naftiko Capability — Organizations](capabilities/fleet-organizations.yaml)
- [Naftiko Capability — Locations](capabilities/fleet-locations.yaml)
- [Naftiko Capability — Machines](capabilities/fleet-machines.yaml)
- [Naftiko Capability — Fragments](capabilities/fleet-fragments.yaml)

### Viam Machine Management API
Connect directly to a viam-server instance to inspect resources, run operations, manage sessions, retrieve machine status, transform poses, and tunnel TCP traffic.

**Human URL:** [https://docs.viam.com/dev/reference/apis/robot/](https://docs.viam.com/dev/reference/apis/robot/)

- [Documentation](https://docs.viam.com/dev/reference/apis/robot/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/robot/v1/robot.proto)
- [OpenAPI](openapi/viam-machine-management-api-openapi.yml)
- [Naftiko Capability — Status](capabilities/machine-status.yaml)
- [Naftiko Capability — Sessions](capabilities/machine-sessions.yaml)
- [Naftiko Capability — Frame System](capabilities/machine-frame-system.yaml)

### Viam Data Client API
Upload, download, query (SQL/MQL), tag, and delete tabular and binary data captured from machines. Manage datasets, saved queries, bounding boxes, sequences, and the cloud-hosted MongoDB connection.

**Human URL:** [https://docs.viam.com/dev/reference/apis/data-client/](https://docs.viam.com/dev/reference/apis/data-client/)

- [Documentation](https://docs.viam.com/dev/reference/apis/data-client/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/data/v1/data.proto)
- [OpenAPI](openapi/viam-data-client-api-openapi.yml)
- [JSON Schema — Tabular Data](json-schema/viam-tabular-data-schema.json)
- [JSON Schema — Binary Data](json-schema/viam-binary-data-schema.json)
- [Naftiko Capability — Tabular Data](capabilities/data-tabular.yaml)
- [Naftiko Capability — Binary Data](capabilities/data-binary.yaml)
- [Naftiko Capability — Datasets](capabilities/data-datasets.yaml)

### Viam Data Sync API
Upload captured data from viam-server to the cloud via DataCaptureUpload, FileUpload, and StreamingDataCaptureUpload.

**Human URL:** [https://docs.viam.com/data-ai/capture-data/capture-sync/](https://docs.viam.com/data-ai/capture-data/capture-sync/)

- [OpenAPI](openapi/viam-data-sync-api-openapi.yml)
- [Naftiko Capability — Sync](capabilities/data-sync.yaml)

### Viam ML Training API
Submit and manage cloud-hosted ML training jobs (built-in TFLite + custom containerized trainers).

**Human URL:** [https://docs.viam.com/data-ai/train/train-tflite/](https://docs.viam.com/data-ai/train/train-tflite/)

- [OpenAPI](openapi/viam-ml-training-api-openapi.yml)
- [Naftiko Capability — Training Jobs](capabilities/ml-training-jobs.yaml)

### Viam ML Inference API
Run cloud-hosted inference against models registered in the Viam ML registry via GetInference.

- [OpenAPI](openapi/viam-ml-inference-api-openapi.yml)
- [Naftiko Capability — Cloud Inference](capabilities/ml-inference.yaml)

### Viam Billing API
Retrieve current-month usage, billing tier metadata, invoice summaries, invoice PDFs, and organization billing information. Supports custom per-machine, per-data, per-API-call invoicing.

**Human URL:** [https://docs.viam.com/manage/manage/billing/](https://docs.viam.com/manage/manage/billing/)

- [OpenAPI](openapi/viam-billing-api-openapi.yml)
- [Naftiko Capability — Usage](capabilities/billing-usage.yaml)
- [Naftiko Capability — Invoices](capabilities/billing-invoices.yaml)

### Viam Motion Service API
Plan and execute motion — Move, MoveOnMap, MoveOnGlobe, GetPose, StopPlan, ListPlanStatuses, GetPlan.

- [OpenAPI](openapi/viam-motion-service-api-openapi.yml)
- [Naftiko Capability — Motion Planning](capabilities/motion-planning.yaml)

### Viam Vision Service API
Object detection, image classification, and 3D segmentation against camera components.

- [OpenAPI](openapi/viam-vision-service-api-openapi.yml)
- [Naftiko Capability — Detections](capabilities/vision-detections.yaml)
- [Naftiko Capability — Classifications](capabilities/vision-classifications.yaml)

### Viam SLAM Service API
Simultaneous Localization And Mapping. GetPosition, GetPointCloudMap, GetInternalState.

- [OpenAPI](openapi/viam-slam-service-api-openapi.yml)
- [Naftiko Capability — Mapping](capabilities/slam-mapping.yaml)

### Viam ML Model Service API
Device-side inference (TFLite, ONNX, Triton). Infer + Metadata.

- [OpenAPI](openapi/viam-ml-model-service-api-openapi.yml)
- [Naftiko Capability — Edge Inference](capabilities/ml-model-infer.yaml)

### Viam Component APIs
Hardware abstraction for every supported component class — arm, audio in/out, base, board, button, camera, encoder, gantry, generic, gripper, input controller, motor, movement sensor, pose tracker, power sensor, sensor, servo, switch.

- [OpenAPI](openapi/viam-component-apis-openapi.yml)
- [Naftiko Capability — Camera](capabilities/component-camera.yaml)
- [Naftiko Capability — Motor](capabilities/component-motor.yaml)
- [Naftiko Capability — Arm](capabilities/component-arm.yaml)
- [Naftiko Capability — Base](capabilities/component-base.yaml)
- [Naftiko Capability — Sensor](capabilities/component-sensor.yaml)

### Viam Data Pipelines API
Scheduled MQL pipelines that aggregate captured data into the Viam hot data store.

- [OpenAPI](openapi/viam-data-pipelines-api-openapi.yml)
- [Naftiko Capability — Pipelines](capabilities/data-pipelines.yaml)

### Viam Provisioning API
Bootstrap a smart machine onto Wi-Fi and the Viam cloud over Bluetooth or hotspot.

- [OpenAPI](openapi/viam-provisioning-api-openapi.yml)
- [Naftiko Capability — Provisioning](capabilities/provisioning.yaml)

## Artifacts

| Artifact | Path |
|---|---|
| Plans & Pricing | [plans/viam-plans-pricing.yml](plans/viam-plans-pricing.yml) |
| Rate Limits | [rate-limits/viam-rate-limits.yml](rate-limits/viam-rate-limits.yml) |
| FinOps | [finops/viam-finops.yml](finops/viam-finops.yml) |
| Vocabulary | [vocabulary/viam-vocabulary.yml](vocabulary/viam-vocabulary.yml) |
| JSON-LD Context | [json-ld/viam-context.jsonld](json-ld/viam-context.jsonld) |
| Spectral Ruleset | [rules/viam-rules.yml](rules/viam-rules.yml) |
| Review | [review.yml](review.yml) |

## Description

Viam is a robotics and edge AI platform founded in 2020 by Eliot Horowitz (MongoDB co-founder and former CTO). It pairs **viam-server** — a gRPC-based runtime that runs on Linux single-board computers (RDK, Go) and ESP32-class microcontrollers (micro-rdk, Rust) — with **viam.app**, a multi-tenant cloud for fleet management, data capture, ML training, and remote operations. Every hardware component and every machine-level service is exposed through a uniform gRPC contract defined in [viamrobotics/api](https://github.com/viamrobotics/api), with first-class SDKs for nine languages.

A modular registry lets vendors and community contributors publish new hardware drivers, vision models, and services as OCI images or packages that any Viam machine can pull at config time, making physical-world control feel like building a microservice. The Billing API is unusual: it lets a Viam customer become a billing provider for its own end-customers, with custom per-machine, per-data, or per-API-call invoicing — a natural fit for OEMs embedding robotics into a product sold as a service.

## Maintainers

- **Kin Lane** — [API Evangelist](https://apievangelist.com) — info@apievangelist.com
