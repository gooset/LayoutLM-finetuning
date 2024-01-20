# Invoice OCR & LayoutLM Classifier

This repository contains code for Optical Character Recognition (OCR) on invoices using Tesseract OCR and visualizing bounding boxes. Additionally, it preprocesses data with Hugging Face's datasets and fine-tunes a LayoutLM model for sequence classification.

## Usage

- **Installation**: Clone this repository and install dependencies with `pip install -r requirements.txt`.
- **OCR**: Use `invoice_ocr.ipynb` to perform OCR on invoice images.
- **Sequence Classification**: Utilize `layoutlm_sequence_classification.ipynb` to preprocess data and train the LayoutLM model.