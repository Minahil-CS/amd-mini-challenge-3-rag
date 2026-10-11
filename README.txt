# NeuralForge AI - Containerized RAG System
> **AMD Mini Challenge 3 Submission** | High-Performance Document-Grounded QA Pipeline

NeuralForge AI is a containerized Retrieval-Augmented Generation (RAG) system built for AMD GPU infrastructure (ROCm/PyTorch). It extracts accurate, evidence-based answers with source citations across mixed-format documents (PDFs, DOCX, XLSX, CSV, Logs, and Images).

---

## 📽️ Project Deliverables
- 📄 **Presentation Slides:** [NeuralForgeAI-Presentation.pdf](./NeuralForgeAI-Presentation.pdf)
- 🎥 **Video Demo Link:** *[Yahan apna Unlisted YouTube / Google Drive Video Link Paste Karein]*

---

## ⚙️ Key Technical Features
- **AMD ROCm Acceleration:** Native integration on `rocm/pytorch` base image.
- **Multi-Format Ingestion:** Parsers for PDF, Word, Excel, CSV, Text logs, and Tesseract OCR for images.
- **Smart Refusal & Traps:** Prevents hallucinations on encrypted files and handles superseded documents.
- **Offline & Isolated:** Operates fully under strict zero-network constraints with optimized VRAM usage.

---

## 🚀 Quick Execution
```bash
# Build Docker Image
docker build -t mc3-rag:starter starter/

# Run Self-Check
python3 selfcheck.py mc3-rag:starter mc3-corpus
