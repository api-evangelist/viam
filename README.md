# Viam (viam)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Viam is a robotics and edge AI platform founded in 2020 by Eliot Horowitz (MongoDB co-founder and former CTO). It pairs viam-server — a gRPC-based runtime that runs on Linux single-board computers (RDK) and ESP32-class microcontrollers (micro-rdk) — with viam.app, a multi-tenant cloud for fleet management, data capture, ML training, and remote operations. Every hardware component (motors, cameras, sensors, arms) and every machine-level service (motion, vision, SLAM, ML inference, navigation) is exposed through a uniform gRPC contract defined in viamrobotics/api with first-class SDKs for Python, Go, Rust, TypeScript, C++, Java, .NET, and Flutter. A modular registry lets vendors and community contributors publish new hardware drivers, vision models, and services as OCI images or packages that any Viam machine can pull at config time, making physical-world control feel like building a microservice.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/viam/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/viam/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Robotics
- Edge AI
- Fleet Management
- Computer Vision
- Machine Learning
- IoT
- Embedded
- gRPC

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Viam Fleet Management API

Create and manage organizations, locations, machines, machine parts, fragments, OAuth apps, API keys, and team memberships in the viam.app cloud. Backed by the AppService gRPC service in viamrobotics/api with REST/JSON transcoding over app.viam.com:443.

- **Human URL:** [https://docs.viam.com/dev/reference/apis/fleet/](https://docs.viam.com/dev/reference/apis/fleet/)

#### Tags

- Robotics
- Fleet Management
- Organizations
- Locations
- Machines

#### Properties

- [Documentation](https://docs.viam.com/dev/reference/apis/fleet/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/v1/app.proto)
- [OpenAPI](openapi/viam-fleet-management-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-fleet-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-fleet-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/viam-organization-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/viam-location-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/viam-machine-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/viam-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Viam Machine Management API

Connect directly to a viam-server instance running on a device to inspect resources, run operations, manage sessions, retrieve machine status and version, transform poses, and tunnel TCP traffic. The Robot Service is the entry point for every machine-side gRPC call.

- **Human URL:** [https://docs.viam.com/dev/reference/apis/robot/](https://docs.viam.com/dev/reference/apis/robot/)

#### Tags

- Robotics
- Machines
- Sessions
- Operations

#### Properties

- [Documentation](https://docs.viam.com/dev/reference/apis/robot/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/robot/v1/robot.proto)
- [OpenAPI](openapi/viam-machine-management-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-machine-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-machine-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam Data Client API

Upload, download, query (SQL/MQL), tag, and delete tabular and binary data captured from machines. Manage datasets, saved queries, bounding boxes, sequences, and the cloud-hosted MongoDB connection used for analytics workloads.

- **Human URL:** [https://docs.viam.com/dev/reference/apis/data-client/](https://docs.viam.com/dev/reference/apis/data-client/)

#### Tags

- Robotics
- Data
- Tabular Data
- Binary Data
- Datasets

#### Properties

- [Documentation](https://docs.viam.com/dev/reference/apis/data-client/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/data/v1/data.proto)
- [OpenAPI](openapi/viam-data-client-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-data-client-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-data-client-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/viam-tabular-data-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/viam-binary-data-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Viam Data Sync API

Upload captured data from viam-server to the cloud via DataCaptureUpload, FileUpload, and StreamingDataCaptureUpload. This is the ingest plane that backs the Data Management Service running on every machine.

- **Human URL:** [https://docs.viam.com/data-ai/capture-data/capture-sync/](https://docs.viam.com/data-ai/capture-data/capture-sync/)

#### Tags

- Robotics
- Data
- Sync
- Capture

#### Properties

- [Documentation](https://docs.viam.com/data-ai/capture-data/capture-sync/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/datasync/v1/data_sync.proto)
- [OpenAPI](openapi/viam-data-sync-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-data-sync-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-data-sync-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam ML Training API

Submit and manage cloud-hosted ML training jobs that produce models deployable to viam-server. Supports built-in TFLite trainers and custom containerized trainers via SubmitTrainingJob and SubmitCustomTrainingJob.

- **Human URL:** [https://docs.viam.com/data-ai/train/train-tflite/](https://docs.viam.com/data-ai/train/train-tflite/)

#### Tags

- Robotics
- Machine Learning
- Training
- Edge AI

#### Properties

- [Documentation](https://docs.viam.com/data-ai/train/train-tflite/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/mltraining/v1/ml_training.proto)
- [OpenAPI](openapi/viam-ml-training-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-ml-training-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-ml-training-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam ML Inference API

Run cloud-hosted inference against models registered in the Viam ML registry via GetInference. Complements the device-side ML Model Service for cases where compute must live in the cloud.

- **Human URL:** [https://docs.viam.com/services/ml/deploy/](https://docs.viam.com/services/ml/deploy/)

#### Tags

- Robotics
- Machine Learning
- Inference
- Edge AI

#### Properties

- [Documentation](https://docs.viam.com/services/ml/deploy/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/mlinference/v1/ml_inference.proto)
- [OpenAPI](openapi/viam-ml-inference-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-ml-inference-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-ml-inference-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam Billing API

Retrieve current-month usage, billing tier metadata, invoice summaries, invoice PDFs, and organization billing information. Supports custom billing tiers and the location-level billing organization assignment used by Viam's "build a robotics business" features.

- **Human URL:** [https://docs.viam.com/manage/manage/billing/](https://docs.viam.com/manage/manage/billing/)

#### Tags

- Robotics
- Billing
- FinOps
- Invoices

#### Properties

- [Documentation](https://docs.viam.com/manage/manage/billing/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/v1/billing.proto)
- [OpenAPI](openapi/viam-billing-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-billing-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-billing-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam Motion Service API

Plan and execute motion for a machine's components — Move, MoveOnMap, MoveOnGlobe, GetPose, StopPlan, ListPlanStatuses, GetPlan. Runs on viam-server as a machine-level service combining kinematic chains, frame system, and obstacle avoidance.

- **Human URL:** [https://docs.viam.com/services/motion/](https://docs.viam.com/services/motion/)

#### Tags

- Robotics
- Motion Planning
- Services

#### Properties

- [Documentation](https://docs.viam.com/services/motion/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/service/motion/v1/motion.proto)
- [OpenAPI](openapi/viam-motion-service-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-motion-service-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-motion-service-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam Vision Service API

Run object detection, image classification, and 3D segmentation against a configured camera component. Supports GetDetectionsFromCamera, GetClassificationsFromCamera, GetObjectPointClouds, and CaptureAllFromCamera.

- **Human URL:** [https://docs.viam.com/services/vision/](https://docs.viam.com/services/vision/)

#### Tags

- Robotics
- Vision
- Computer Vision
- Services

#### Properties

- [Documentation](https://docs.viam.com/services/vision/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/service/vision/v1/vision.proto)
- [OpenAPI](openapi/viam-vision-service-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-vision-service-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-vision-service-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam SLAM Service API

Simultaneous Localization And Mapping. GetPosition returns the machine's pose within the map; GetPointCloudMap and GetInternalState stream the live map. Backed by Viam's ORB-SLAM3 and Cartographer integrations and the Cloud SLAM service.

- **Human URL:** [https://docs.viam.com/services/slam/](https://docs.viam.com/services/slam/)

#### Tags

- Robotics
- SLAM
- Mapping
- Services

#### Properties

- [Documentation](https://docs.viam.com/services/slam/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/service/slam/v1/slam.proto)
- [OpenAPI](openapi/viam-slam-service-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-slam-service-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-slam-service-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam ML Model Service API

Device-side inference. Infer runs a deployed model against tensors; Metadata returns model input and output schemas. Pairs with TFLite, ONNX, and Triton ML model implementations.

- **Human URL:** [https://docs.viam.com/services/ml/deploy/](https://docs.viam.com/services/ml/deploy/)

#### Tags

- Robotics
- Machine Learning
- Inference
- Edge AI
- Services

#### Properties

- [Documentation](https://docs.viam.com/services/ml/deploy/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/service/mlmodel/v1/mlmodel.proto)
- [OpenAPI](openapi/viam-ml-model-service-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-ml-model-service-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-ml-model-service-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam Component APIs

Hardware abstraction for every supported component class — arm, audio in/out, base, board, button, camera, encoder, gantry, generic, gripper, input controller, motor, movement sensor, pose tracker, power sensor, sensor, servo, switch. Each component class exposes a uniform gRPC contract.

- **Human URL:** [https://docs.viam.com/dev/reference/apis/](https://docs.viam.com/dev/reference/apis/)

#### Tags

- Robotics
- Components
- Hardware
- Sensors
- Actuators

#### Properties

- [Documentation](https://docs.viam.com/dev/reference/apis/)
- [Protobuf](https://github.com/viamrobotics/api/tree/main/proto/viam/component)
- [OpenAPI](openapi/viam-component-apis-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-component-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-component-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam Data Pipelines API

Create, list, rename, enable, disable, and delete scheduled MQL data pipelines that aggregate captured machine data into the Viam hot data store. Backed by ListDataPipelineRuns for execution history.

- **Human URL:** [https://docs.viam.com/data-ai/data/data-pipelines/](https://docs.viam.com/data-ai/data/data-pipelines/)

#### Tags

- Robotics
- Data
- Pipelines
- Analytics

#### Properties

- [Documentation](https://docs.viam.com/data-ai/data/data-pipelines/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/app/datapipelines/v1/data_pipelines.proto)
- [OpenAPI](openapi/viam-data-pipelines-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-data-pipelines-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-data-pipelines-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Viam Provisioning API

Bootstrap a smart machine onto Wi-Fi and into the viam.app cloud over Bluetooth or hotspot. SetNetworkCredentials, SetSmartMachineCredentials, GetNetworkList, GetSmartMachineStatus, and ExitProvisioning are used by the Flutter provisioning widgets and viam-agent.

- **Human URL:** [https://docs.viam.com/manage/configure/provisioning/](https://docs.viam.com/manage/configure/provisioning/)

#### Tags

- Robotics
- Provisioning
- Onboarding
- Bluetooth

#### Properties

- [Documentation](https://docs.viam.com/manage/configure/provisioning/)
- [Protobuf](https://github.com/viamrobotics/api/blob/main/proto/viam/provisioning/v1/provisioning.proto)
- [OpenAPI](openapi/viam-provisioning-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/viam-provisioning-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/viam-provisioning-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://www.viam.com)
- [Documentation](https://docs.viam.com)
- [Documentation](https://docs.viam.com/dev/reference/apis/)
- [Documentation](https://docs.viam.com/sdks/)
- [Sign Up](https://app.viam.com)
- [Sandbox](https://app.viam.com)
- [Pricing](https://www.viam.com/pricing)
- [Changelog](https://docs.viam.com/dev/reference/changelog/)
- [Status Page](https://status.viam.com)
- [Documentation](https://docs.viam.com/manage/cli/)
- [GitHub Organization](https://github.com/viamrobotics)
- [Protobuf](https://github.com/viamrobotics/api)
- [SDK](https://github.com/viamrobotics/rdk)
- [SDK](https://github.com/viamrobotics/micro-rdk)
- [SDK](https://github.com/viamrobotics/viam-python-sdk)
- [SDK](https://github.com/viamrobotics/viam-typescript-sdk)
- [SDK](https://github.com/viamrobotics/viam-rust-sdk)
- [SDK](https://github.com/viamrobotics/viam-cpp-sdk)
- [SDK](https://github.com/viamrobotics/viam-flutter-sdk)
- [SDK](https://github.com/viamrobotics/viam-java-sdk)
- [SDK](https://github.com/viamrobotics/viam-dotnet-sdk)
- [SDK](https://github.com/viamrobotics/viam-svelte-sdk)
- [Tool](https://github.com/viamrobotics/agent)
- [Tool](https://github.com/viamrobotics/build-action)
- [Tool](https://github.com/viamrobotics/upload-module)
- [Tool](https://github.com/viamrobotics/visualization)
- [Code Examples](https://github.com/viamrobotics/samples)
- [Code Examples](https://github.com/viamrobotics/can-inspection-simulation)
- [Code Examples](https://github.com/viamrobotics/inspection-module-starter)
- [Documentation](https://github.com/viamrobotics/docs)
- [Tool](https://github.com/viamrobotics/prime)
- [Tool](https://github.com/viamrobotics/three)
- [Portal](https://app.viam.com/registry)
- [Forum](https://discord.gg/viam)
- [Blog](https://www.viam.com/blog)
- [Blog](https://www.viam.com/post)
- [Case Studies](https://www.viam.com/customers)
- [Terms of Service](https://www.viam.com/legal/terms)
- [Privacy Policy](https://www.viam.com/legal/privacy)
- [Trust Center](https://www.viam.com/security)
- [Support](https://www.viam.com/contact)
- [LinkedIn](https://www.linkedin.com/company/viamrobotics)
- [Twitter](https://twitter.com/viamrobotics)
- [YouTube](https://www.youtube.com/@ViamRobotics)
- [Plans](plans/viam-plans-pricing.yml)
- [Rate Limits](rate-limits/viam-rate-limits.yml)
- [Fin Ops](finops/viam-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
