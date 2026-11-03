# Al-Mushajjir | المُشَجِّر 

### Transform educational materials into structured knowledge.

**Al-Mushajjir** is an open-source project that aims to transform educational materials into comprehensive, hierarchical, and interactive knowledge maps.

The project focuses on organizing complex learning materials into structured trees of interconnected concepts, topics, and subtopics, while preserving important information, explanations, examples, and relationships from the original sources.

The goal is not simply to summarize documents, but to make their knowledge easier to explore, understand, and study.

---

## Project Vision

Educational materials often contain large amounts of information presented in lengthy documents, books, and lecture notes. Understanding how their concepts relate to one another can be challenging.

Al-Mushajjir aims to address this problem by transforming educational content into structured knowledge maps that reveal its organization and relationships.

Users should be able to explore the generated maps interactively, understand individual concepts through explanations, trace information back to its original source, and export the results into professionally formatted PDF documents.

## Core Objectives

1. **Document Ingestion:** Accept educational materials in different formats, starting with PDF, DOCX, and TXT.
2. **Content Understanding:** Identify important topics, concepts, definitions, classifications, examples, and relationships.
3. **Hierarchical Organization:** Organize extracted knowledge into comprehensive, logically structured trees.
4. **Concept Explanations:** Provide explanations and additional context for individual nodes when needed.
5. **Content Coverage:** Preserve important information from the original material and identify missing or partially represented content.
6. **Source Traceability:** Associate knowledge-map nodes with their original document pages and sections.
7. **Interactive Exploration:** Allow users to navigate, expand, collapse, and explore different branches of a knowledge map.
8. **PDF Export:** Generate professionally formatted, readable, and multi-page PDF knowledge maps.
9. **Multilingual Support:** Support different interface, source-document, and output languages independently.

## Key Principles

### 1. Comprehensive Knowledge Representation

The application should preserve the important information contained in the original educational material.

Generated maps should represent more than a short summary. They should capture the document's main topics, subtopics, definitions, classifications, examples, and meaningful relationships.

Content coverage and completeness should be evaluated rather than assumed.

### 2. Source Traceability

Every relevant knowledge-map node should be traceable to its original source, such as a document page or section.

This allows users to verify information and return to the original material whenever necessary.

### 3. Separation of Responsibilities

Content extraction, knowledge generation, tree management, validation, visualization, and PDF rendering should remain separate components.

This makes the system easier to maintain, test, extend, and integrate with different AI models and rendering technologies.

### 4. Language Independence

The core knowledge representation should not depend on a specific language.

The system should support multilingual content without requiring changes to its fundamental data structures.

### 5. Extensibility

The architecture should allow new document formats, AI providers, visualization methods, output formats, and languages to be integrated without major changes to existing components.

---

## Multilingual Strategy

Al-Mushajjir is initially developed using English for its source code, technical documentation, and development workflow, with Arabic as the first target language for the application experience and generated educational content.

The architecture must support multilingual functionality from the beginning.

### Independent Language Settings

The following language settings must be independent:

- **Interface Language:** The language used for application labels, menus, and messages.
- **Source Language:** The language of the uploaded educational material.
- **Output Language:** The language used in the generated knowledge map and explanations.

For example, a user should be able to use an English interface, upload an Arabic document, and generate an Arabic knowledge map.

### Localization Requirements

- All interface text must be managed through centralized localization files.
- Language-specific strings must not be hardcoded throughout the application.
- Unicode must be supported throughout the system.
- Right-to-left (RTL) and left-to-right (LTR) layouts must be supported.
- Mixed Arabic and English text must be displayed correctly.
- PDF generation must support Arabic shaping, bidirectional text rendering, and appropriate embedded fonts.
- Content must not be automatically translated unless the user explicitly requests translation.

Arabic is the first priority for multilingual implementation, followed by additional languages such as Hebrew and other widely used languages.

---

## Planned Features

The following features represent the project's intended direction. They are not all implemented yet.

| Feature | Description |
|---|---|
| Document Upload | Upload educational materials in supported formats |
| Content Extraction | Extract document text and structure |
| AI-Powered Generation | Generate comprehensive hierarchical knowledge maps |
| Interactive Mind Maps | Explore and navigate knowledge trees |
| Node Explanations | View explanations for individual concepts |
| Source References | Trace nodes to original document sections and pages |
| Coverage Analysis | Identify missing or partially represented content |
| PDF Export | Export professionally formatted knowledge maps |
| Multilingual Interface | Use the application in different languages |
| RTL Support | Properly display Arabic and other RTL languages |

---

### Main Components

- **Core:** Defines the fundamental data models, hierarchical tree operations, and validation rules.
- **Ingestion:** Handles uploaded documents and input management.
- **Extraction:** Extracts text and structural information from documents.
- **Generation:** Converts extracted educational content into structured knowledge representations.
- **Localization:** Manages interface languages and language-related configuration.
- **Rendering:** Handles interactive knowledge-map visualization and PDF generation.
- **API:** Provides application interfaces for communication between components.

---

## Development Roadmap

Development will proceed incrementally, with an emphasis on correctness, maintainability, and testability.

### Phase 1 — Project Foundation
- Establish the project structure.
- Define the core data models.
- Implement hierarchical tree operations.
- Implement tree validation.
- Add JSON serialization and deserialization.

### Phase 2 — Basic Knowledge Maps
- Create manually structured knowledge-map examples.
- Implement basic tree visualization.
- Support node explanations and source references.
- Add unit and integration tests.

### Phase 3 — PDF Generation
- Implement structured PDF export.
- Support multi-page layouts.
- Establish consistent visual hierarchy and typography.
- Prepare the rendering architecture for Arabic and RTL text.

### Phase 4 — Document Processing
- Implement text extraction from supported document formats.
- Preserve document structure and source locations.
- Handle headings, paragraphs, lists, and tables.

### Phase 5 — AI-Powered Knowledge Generation
- Integrate an AI-powered generation engine.
- Generate comprehensive hierarchical structures.
- Validate generated content.
- Implement content coverage analysis.
- Support explanations and meaningful relationships between nodes.

### Phase 6 — Multilingual and RTL Support
- Complete the localization infrastructure.
- Implement Arabic interface support.
- Implement Arabic knowledge-map rendering.
- Validate Arabic PDF generation and mixed-language content.
- Extend support to additional languages.

### Phase 7 — Application Integration
- Integrate the main components.
- Build the interactive application interface.
- Improve usability and performance.
- Expand supported formats and export options.

---

## Technology Stack

The technology choices will be evaluated during development. The initial direction includes:

| Area | Planned Technologies |
|---|---|
| Programming Language | Python |
| Data Validation | Pydantic |
| Document Processing | PyMuPDF, python-docx |
| AI Integration | LLM APIs and open-source models |
| Data Processing | NumPy, Pandas when needed |
| Backend API | FastAPI |
| Testing | Pytest |
| Code Quality | Ruff, mypy |
| Version Control | Git and GitHub |
| PDF Generation | A library supporting structured layouts, Unicode, and Arabic RTL rendering |

Specific technologies may change as the project evolves.

---

## Contributing

Al-Mushajjir is intended to be an open-source project, and contributions are welcome.

Potential areas of contribution include:

- Python development and software architecture.
- Document extraction and processing.
- AI-powered knowledge generation.
- Hierarchical data structures and validation.
- Interactive visualization.
- PDF rendering and Arabic typography.
- Localization and multilingual support.
- Testing, documentation, and performance improvements.

Contribution guidelines will be added as the project develops.

---

## Current Development Status

**Status: Early Development**

The project is currently in its foundation and architectural design stage.

Initial development will prioritize the core hierarchical knowledge representation before introducing AI-powered generation.

---

## License

This project is distributed under the MIT License.

---

**Al-Mushajjir — From educational materials to structured knowledge.**
