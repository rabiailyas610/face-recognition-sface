## Serverless Face Recognition Engine (CLIP & Neon DB)
A production-ready, cloud-native face verification pipeline built using Python, Advanced Computer Vision, and Serverless Cloud Vector infrastructure.

## Project Evolution: Before vs. After (Upgrades)
This repository has been refactored and modernized to align with industry-standard cloud engineering architectures. Below is the technical breakdown of the system upgrades:
## Database Storage

* Legacy Architecture (2 Years Ago): Local system directory files or standard relational layout.
* Modernized Architecture (Current): Neon Serverless PostgreSQL Cloud Engine.

## Indexing & Search

* Legacy Architecture (2 Years Ago): Manual file comparison looping which caused high latency and was highly inefficient.
* Modernized Architecture (Current): Deep pgvector Vector Indexing for instant querying.

## Mathematical Distance

* Legacy Architecture (2 Years Ago): Basic pixel arrays and Euclidean mapping.
* Modernized Architecture (Current): L2 Vector Distance Space Operator (<->).

## Feature Extraction

* Legacy Architecture (2 Years Ago): Traditional pixel-based representations using the older imgbeddings library.
* Modernized Architecture (Current): OpenAI CLIP Vision Transformer via Hugging Face.

## Pipeline Reliability

* Legacy Architecture (2 Years Ago): High third-party package version conflicts.
* Modernized Architecture (Current): Completely stable, dependency-isolated backend.

## Key Features

* Serverless Cloud Architecture: Powered by Neon DB, enabling automated computing and database storage scaling on demand.
* Sub-Millisecond Vector Scans: Utilizes the cloud-native pgvector indexing plugin to run quick similarity matches over high-dimensional arrays.
* Deep Biometric Embeddings: Formulates stable 512-dimensional vector arrays using OpenAI's pre-trained Vision Transformers (clip-vit-base-patch32).
* Clean Execution Flow: A unified, production-ready script framework optimized for quick pipeline deployments.

## System Workflow

   1. Face Localization: Input source graphics are captured, and structural visual bounds are extracted natively via OpenCV.
   2. Transformer Processing: Isolated face crop matrices are tokenized through the Hugging Face CLIPProcessor.
   3. High-Dimensional Extraction: The CLIPVisionModel computes a standardized 512-point numeric representation array.
   4. Cloud Index Match: The generated query list executes an L2 distance lookup (<->) directly inside Neon DB to instantly retrieve the closest person match profile records.

## Technology Stack

* Languages & Frameworks: Python 3.x, PyTorch
* Computer Vision: OpenCV (Open Source Computer Vision Library)
* Deep Learning Model: OpenAI CLIP (Vision Transformer Model)
* Database Engine: Neon PostgreSQL Serverless Instance
* Vector Plugin: pgvector extension (vector(512))
