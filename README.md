# Project Nura

**See information. Hear understanding.**

Nura is an AI-powered visual accessibility system designed for people who are blind or visually impaired. It transforms visual information that would otherwise be inaccessible into contextual, spoken information.

The initial product is designed as a web/mobile experience and browser extension, with the long-term goal of integrating the same intelligence into a flexible, foldable hardware screen reader.

## Problem

Most digital accessibility tools are optimized for structured digital interfaces. However, visually impaired people encounter large amounts of important information in the physical world that is inherently visual:

- Books and printed documents
- Street and building signage
- Currency
- Product labels
- Receipts
- Posters and notices
- Forms
- Screens and digital displays
- Maps, charts and diagrams

Nura focuses on making this information accessible through vision-to-voice interaction.

## Core Concept

The user points a camera at visual information and Nura:

1. Captures the visual input
2. Detects and extracts relevant information
3. Uses AI to understand the content and context
4. Converts the result into natural spoken output
5. Allows the user to ask follow-up questions about what was captured

### Example

**User points at a street sign**

> "The sign reads Kenyatta Avenue."

**User points at a Kenyan banknote**

> "This is a one thousand Kenyan shilling note."

**User points at a textbook**

> "The heading reads Cellular Respiration."

The goal is not to describe every object in the environment. Nura prioritizes **information-bearing visual content**.

## Core MVP Features

### 1. Text Reading

- OCR-based text extraction
- Books
- Documents
- Receipts
- Forms
- Posters
- Printed notices
- Small or difficult-to-read text

### 2. Signage Reading

Recognition and spoken interpretation of:

- Street signs
- Building names
- Room numbers
- Directional signs
- Public notices
- Shop signs
- Institutional signage

### 3. Currency Recognition

Initial focus:

- Kenyan currency

The architecture should support expansion to other currencies.

### 4. Contextual Understanding

Instead of only extracting raw OCR text, Nura can explain what the captured information means.

For example:

> "This appears to be a university admission letter. The important information is your admission status, reporting date and program."

### 5. Ask About What You See

Users can ask natural-language questions about the current visual context:

- "What does this say?"
- "Read the heading."
- "What is the important information?"
- "What denomination is this?"
- "What does this document mean?"
- "Repeat that."
- "Read the next paragraph."

### 6. Voice Output

ElevenLabs provides the spoken interaction layer, allowing visual information to become accessible through natural audio.

## Product Interfaces

Nura is designed as one intelligence engine with multiple interfaces.

```text
                         Nura
                  Visual Intelligence
                         Engine
                           |
          +----------------+----------------+
          |                |                |
       Mobile             Web          Browser Extension
          |                |                |
          +----------------+----------------+
                           |
                     Future Hardware
                           |
                    Camera + Controls
                           |
                      Audio Output
                           |
                        Earbuds
```

### Web

A browser-based interface for rapid access and demonstrations.

### Mobile

A camera-first interface designed around accessibility and voice interaction.

### Browser Extension

Designed to make web pages, images, buttons, forms and other digital content easier to access.

### Hardware

The long-term vision is a small, flexible and foldable visual reader that can be attached or positioned over:

- Books
- Laptops
- Mobile phones
- Desks
- Other surfaces

The hardware would provide the camera and physical controls while Nura provides the intelligence.

## Hardware Vision

The eventual device should be portable, flexible and simple to operate.

Possible interaction model:

```text
              +-------------------+
              |      CAMERA       |
              +---------+---------+
                        |
                   Visual Input
                        |
                        v
                 NURA ENGINE
                        |
                        v
                 Voice Response
                        |
                        v
                   Bluetooth
                        |
                        v
                     Earbuds
```

Potential physical controls:

- Capture / Read
- Ask
- Repeat / Stop

The hardware should not require a complicated interface.

## Technology Stack

### Required Hackathon Products

**ElevenLabs**
- Voice output
- Natural speech
- Speech interaction where applicable

**Cursor**
- AI-assisted development
- Agentic coding
- Rapid implementation
- Testing and debugging

**Render**
- Backend/API deployment
- Cloud infrastructure
- Future background processing and persistence

### Supporting Technologies

The implementation can use technologies such as:

- Python
- FastAPI
- Computer vision
- OCR
- Multimodal AI
- JavaScript
- HTML/CSS
- PostgreSQL

The exact implementation can evolve as the MVP is developed.

## High-Level Architecture

```text
Camera / Browser
       |
       v
Visual Input
       |
       v
Vision + OCR Layer
       |
       +---------> Text
       |
       +---------> Currency
       |
       +---------> Signage
       |
       +---------> Document
       |
       +---------> Image / Visual Context
                       |
                       v
                Context Engine
                       |
                       v
                AI Response
                       |
                       v
                  ElevenLabs
                       |
                       v
                   Audio Output
```

## MVP Priority

Because the initial implementation is being developed under a short hackathon timeline, development is prioritized as follows.

### P0 — Essential

- Camera/image capture
- Text reading
- Signage recognition
- Kenyan currency recognition
- Contextual visual understanding
- Voice output
- Ask questions about captured content

### P1 — Important

- Reading history
- Follow-up questions
- Voice commands
- Reading speed controls
- Browser extension
- Improved document structure detection

### P2 — Future

- Native mobile applications
- Foldable hardware prototype
- Offline/edge inference
- Additional currencies
- Multilingual support
- Advanced document understanding
- Specialized accessibility deployments
- Device management

## Design Principles

### Voice-first

The primary output should be accessible without requiring visual interaction.

### Information-first

The system should prioritize text, signage, currency, documents and other meaningful visual information rather than narrating every object in the environment.

### Context-aware

Nura should move beyond raw OCR and help users understand what the information means.

### Confidence-aware

The system should communicate uncertainty rather than confidently presenting potentially incorrect information.

Example:

> "I believe this is a 500 shilling note, but I'm not completely certain."

### Minimal interaction

The user should be able to accomplish common tasks with a small number of commands.

### Portable

The eventual hardware should work across books, phones, laptops and other everyday surfaces.

### Privacy-conscious

Images and audio should be processed transiently by default wherever practical. Persistent storage should be minimized and explicit when needed.

## Example User Journey

```text
User points camera at a document
            |
            v
       Capture image
            |
            v
      Detect document
            |
            v
       Extract text
            |
            v
      Understand context
            |
            v
  Generate concise response
            |
            v
      ElevenLabs voice
            |
            v
          User
            |
            v
     "What is the date?"
            |
            v
      Context-aware answer
```

## Long-Term Vision

Nura aims to become an **intelligent visual access layer** that can sit between the physical/digital world and a person's preferred method of interaction.

The long-term platform can power:

- Mobile accessibility
- Web accessibility
- Browser accessibility
- Assistive hardware
- Educational environments
- Public institutions
- Workplaces
- Libraries
- Transportation environments
- Other accessibility-focused deployments

The fundamental idea remains simple:

> **Visual information should not be inaccessible simply because it cannot be seen.**

## Hackathon Demonstration

The recommended demonstration flow is:

1. Read a printed page
2. Read a street/building sign
3. Identify Kenyan currency
4. Understand a document or poster
5. Ask a follow-up question
6. Demonstrate spoken output through ElevenLabs
7. Show the future foldable hardware concept

The presentation should emphasize that the prototype is the first interface to a broader **visual intelligence engine**, rather than the final hardware product.

## Status

**Hackathon MVP — In Development**

The current focus is proving the core experience:

**Capture → Understand → Speak → Ask**

---

## License

To be determined.
