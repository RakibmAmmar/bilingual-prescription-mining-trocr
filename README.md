# Bilingual Handwritten Prescription Mining in Low-Resource Settings Using Fine-Tuned TrOCR

## Overview

This project presents an end-to-end AI pipeline for bilingual handwritten prescription understanding in low-resource healthcare settings such as Bangladesh. The system recognizes handwritten medicine names from prescription crops using a fine-tuned TrOCR model, corrects OCR errors using lexicon-guided Levenshtein post-processing, enriches medicine information using a structured medicine knowledge base, and generates patient-centric summaries in both English and Bangla.

## Motivation

Handwritten prescriptions in Bangladesh often contain mixed Bangla-English text, poor handwriting, irregular medicine spellings, and non-standard layouts. Misreading medicine names or dosage instructions can create serious patient-safety risks. This project aims to reduce ambiguity by combining OCR, domain-specific correction, and patient-friendly summarization.

## Key Results

| Method | CER ↓ | WER ↓ | Exact Match Accuracy ↑ |
|---|---:|---:|---:|
| Raw Fine-Tuned TrOCR | 8.86% | 27.96% | 73.13% |
| TrOCR + Lexicon-Guided Post-Processing | 5.87% | 13.42% | 88.06% |
| Absolute Improvement | 2.99% | 14.54% | 14.93% |

Lexicon-guided post-processing reduced CER by approximately 33.7%, reduced WER by approximately 52.0%, and improved exact medicine-name accuracy by 14.93 percentage points.

## Main Contributions

- Converted annotated prescription regions into OCR-ready medicine-name crops.
- Fine-tuned `microsoft/trocr-base-handwritten` for handwritten medicine-name recognition.
- Compared OCR approaches including TrOCR, DocTR, EasyOCR, and Tesseract.
- Designed lexicon-guided post-processing using Levenshtein edit distance.
- Built a medicine knowledge enrichment pipeline for strength, disease class, indication, frequency, and timing.
- Generated bilingual Bangla-English patient-centric prescription summaries.

## Future Research Direction: HCI and XR Extension

My future research goal is to extend this AI-based prescription understanding system into Human-Computer Interaction and XR. A possible direction is an AI-assisted gaze-guided AR interface that helps patients, pharmacists, or healthcare workers verify handwritten medicine names, understand dosage instructions, and reduce interpretation errors.

Possible evaluation metrics:

- Medicine identification accuracy
- Error correction rate
- Task completion time
- User confidence
- SUS usability score
- NASA-TLX cognitive load
- User trust in AI recommendations

## Privacy and Ethical Note

This repository does not include identifiable patient data. Any prescription images used for demonstration are cropped, anonymized, blurred, or recreated for research presentation purposes.

## Technologies

- Python
- PyTorch
- Hugging Face Transformers
- TrOCR
- PIL / OpenCV
- pandas / NumPy
- Levenshtein distance
- OCR evaluation using CER and WER

## Author

Rakib Mohammad Ammar  
BSc in Computer Science and Engineering  
Port City International University, Bangladesh  

Research interests: AI, OCR, HCI, XR, low-resource healthcare, document understanding
