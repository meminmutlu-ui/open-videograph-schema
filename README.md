# Open VideoGraph Data Standard & Ontology Schema (v1.0.0)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21888981.svg)](https://doi.org/10.5281/zenodo.21888981)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Welcome to the official **Open VideoGraph Schema Registry**.

This repository contains the JSON Schema (Draft 2020-12) specifications for all 13 analytical data module specifications and root manifest container of the **VideoGraph** and **Video Intelligence Studio** narrative video analytics suite.

---

## 📌 Available Schemas (v1.0.0 - 14 Specifications)

| Schema Name | Description | JSON Schema Specification |
| :--- | :--- | :--- |
| **Manifest Root** | Root metadata & Character-Scene Bipartite Graph (`data.js`) | [`schemas/v1/manifest.json`](./schemas/v1/manifest.json) |
| **Scene Segmentation** | Scene boundaries, thumbnails, and 7 Golden Fields | [`schemas/v1/scene.json`](./schemas/v1/scene.json) |
| **Character Identity** | Character avatars and timestamped appearances | [`schemas/v1/character.json`](./schemas/v1/character.json) |
| **Transcript & Dialogue** | Timestamped spoken text and speaker diarization | [`schemas/v1/transcript.json`](./schemas/v1/transcript.json) |
| **Shot Boundaries** | Frame thumbnails, duration, Places365/CLIP tags | [`schemas/v1/shot.json`](./schemas/v1/shot.json) |
| **Sentiment & Mood** | Emotional tone curves, mood valence, polarity | [`schemas/v1/sentiment.json`](./schemas/v1/sentiment.json) |
| **Sequence & Acts** | Dramatic act segmentation and tension curves | [`schemas/v1/sequence.json`](./schemas/v1/sequence.json) |
| **Semantic Search** | 7 Golden Fields vector search indexing metadata | [`schemas/v1/semantic.json`](./schemas/v1/semantic.json) |
| **Narrative LightRAG** | Entity-Relationship Knowledge Graph & Global Summary | [`schemas/v1/narrative.json`](./schemas/v1/narrative.json) |
| **Topic Modeling** | Multi-granularity (3, 5, 7, 10) LDA/LLM topic distributions | [`schemas/v1/topic.json`](./schemas/v1/topic.json) |
| **Camera Movement** | Optical flow camera movement, framing scale & angles | [`schemas/v1/camera.json`](./schemas/v1/camera.json) |
| **Audio Spectrum** | Audio energy, music presence, silence mapping & motifs | [`schemas/v1/audio.json`](./schemas/v1/audio.json) |
| **Visual Tone** | Scene brightness, contrast, and HEX color palettes | [`schemas/v1/visual_tone.json`](./schemas/v1/visual_tone.json) |
| **Dialogue Flow** | Speaker turn transition graph and speaker nodes | [`schemas/v1/dialogue_flow.json`](./schemas/v1/dialogue_flow.json) |

---

## 🚀 Quick Start (JSON Schema Validation)

You can validate any VideoGraph export dataset against these schemas using any JSON Schema validator (Python `jsonschema`, JS `ajv`, C# `NJsonSchema`):

### Python Example:
```python
import json
import jsonschema

with open("data_scenes.js", "r") as f:
    # Read dataset
    data = json.load(f)

with open("schemas/v1/scene.json", "r") as f:
    schema = json.load(f)

# Validate
jsonschema.validate(instance=data[0], schema=schema)
print("Valid VideoGraph Scene Dataset!")
```

---

## 🔒 System Scope & Boundaries

- **Open VideoGraph Specification**: Covers public data schemas, 13 analytical data module specifications, and standalone viewer web application (Licensed under MIT & CC BY 4.0).
- **Video Intelligence Studio (Core & Admin Dashboard)**: The core backend processing engine, AI pipeline models, Admin Management Dashboard (`admin.html`), and server administration tools are **proprietary software (Copyright (c) 2026 Mehmet Emin Mutlu - All Rights Reserved)** and are strictly excluded from this public specification repository.

---

## 🛡️ License & Notice

> **Schema, Ontology & System Architecture Notice**:  
> The VideoGraph data structure, graph ontology (character-scene bipartite networks, character co-occurrence graphs, scene transition topologies), and 13 analytical data module specifications are designed and published by **Dr. Mehmet Emin Mutlu** (Anadolu University, Eskisehir, Turkey | Email: `memutlu@anadolu.edu.tr`) under the **Open VideoGraph Data Standard Specification**.

- **Author & Architecture Citation**: Dr. Mehmet Emin Mutlu (`meminmutlu-ui`)
- **Institution**: Anadolu University, Eskisehir, Turkey
- **Contact Email**: `memutlu@anadolu.edu.tr`
- **VideoGraph Standalone Export Player**: MIT License (Open Source)
- **Open VideoGraph Data Standard & Schemas**: Creative Commons Attribution 4.0 International (CC BY 4.0)
- **Video Intelligence Studio Core System**: Proprietary Suite (Copyright (c) 2026 Mehmet Emin Mutlu - All Rights Reserved)

---

## 🎓 How to Cite

If you use Open VideoGraph Schema in your research or software, please cite it as:

```bibtex
@dataset{mutlu2026videograph,
  author       = {Mutlu, Mehmet Emin},
  title        = {Open VideoGraph Schema v1.0.0},
  month        = aug,
  year         = 2026,
  publisher    = {Zenodo},
  version      = {v1.0.0},
  doi          = {10.5281/zenodo.21888981},
  url          = {https://doi.org/10.5281/zenodo.21888981}
}

---

APA 7th Edition:
Mutlu, M. E. (2026). Open VideoGraph Schema v1.0.0 [Standart]. Zenodo. https://doi.org/10.5281/zenodo.21888981
