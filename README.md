# HackerEarth — Bojack's Restaurant Total Earnings

HackerEarth ML challenge: given images of restaurant bills, extract the total amount from each one.

## Approach

**Step 1 — PDF to image** (`Convert PDFToImage.ipynb`)
Used the `wand` library to convert PDFs from the test set into JPEG images. Google Vision API requires image input, not PDFs.

**Step 2 — OCR** (`ExtractText.ipynb`)
Passed each image through Google Vision API and dumped the extracted text to `.txt` files.

**Step 3 — Find the total** (`FindTotalAmount.ipynb`)
Totals are always floating-point numbers. Initial approach: list all floats in the text and take the maximum → **99.8% accuracy**.

Error analysis revealed the edge case: some bills had a "change" line, which sometimes held a higher value than the actual total. Fix: check if the sum of line amounts was also present in the text and use that for secondary validation → **99.92% accuracy**.

## Files

| File | Purpose |
|---|---|
| `Convert PDFToImage.ipynb` | PDF → JPEG conversion |
| `ExtractText.ipynb` | Google Vision API OCR |
| `FindTotalAmount.ipynb` | Total extraction logic |
| `Extracted text.rar` | Pre-extracted text output from the test set |

## Dependencies

- `wand` (ImageMagick Python binding)
- Google Cloud Vision API (needs a service account key)
- Standard Python: `re`, `os`
