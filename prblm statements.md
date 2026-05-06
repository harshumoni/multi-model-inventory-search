This project is a smart inventory system that uses AI to let customers find products by uploading a photo, solving the problem of not knowing the specific name or text description of an item.
        ┌────────────────────┐
        │      User Input     │
        │  (Image or Text)    │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │   Preprocessing     │
        │ (Resize / Clean)    │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │  CLIP Model         │
        │ (via Hugging Face   │
        │  Transformers)      │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │  Embedding Vector   │
        │ (512-D normalized) │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ OpenSearch k-NN     │
        │  Vector Search      │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Top-N Similar Items │
        │ (Scores + Metadata)│
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │   Frontend (React) │
        │   Results Gallery  │
        └────────────────────┘
