# LayoutLMv3 Notebooks and Training Tips

Explore **LayoutLMv3** through our notebooks for fine-tuning and inference, achieving exceptional performance on the FUNSD dataset, surpassing 90% F1. Key to this success is the use of segment position embeddings, offering improved performance over word-level embeddings.

OCR engines, including Tesseract, identify segments, enhancing LayoutLMv3's capabilities. For FUNSD, segment creation is based on labels ([details](https://huggingface.co/datasets/nielsr/funsd-layoutlmv3/blob/main/funsd-layoutlmv3.py#L140)). Always opt for segment position embeddings for superior performance.

## Training Tips

LayoutLMv3 training parallels LayoutLMv2, with a few distinctions:

- **Image Preprocessing**: Resize and normalize images to `pixel_values` of shape `(batch_size, num_channels, height, width)`, with RGB format. This differs from LayoutLMv2, which used BGR format.

- **Text Tokenization**: LayoutLMv3 relies on RoBERTa-based byte-level Byte-Pair-Encoding. Unlike LayoutLMv2, which used BERT-like WordPiece tokenization.

Introducing the `LayoutLMv3Processor` that seamlessly combines image and text processing. It mirrors the usage of its predecessor, [`LayoutLMv2Processor`](https://huggingface.co/docs/transformers/model_doc/layoutlmv2#usage-layoutlmv2processor).

