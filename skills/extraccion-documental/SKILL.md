---
name: extraccion-documental
description: Conversion of legal documentation in PDF or scanned form into structured data for due diligence and mass review. Use it when a volume of documents must be analysed and findings extracted systematically.
---

# Document Extraction

## Process
1. **Inventory**: list every file with type, date, parties and status (signed / draft / illegible).
2. **Classification** by area: corporate · contracts · employment · real estate · financing · IP · litigation · licensing · data protection · tax.
3. **Extraction** per document:
   - Parties and signatories
   - Signature date and effective date
   - Subject matter
   - Term, renewal and notice period
   - Amounts and payment terms
   - Guarantees and security
   - Change of control
   - Exclusivity and non-compete
   - Limitation of liability
   - Governing law and forum
   - Referenced annexes and whether they are present

4. **Cross-check**: compare the extracted data against the inventory to detect what is missing.

## Output
Structured table, one document per row, with a link to the exact location (file and page).

## Rules
- Always cite the file and page. A finding without a location is useless.
- Explicitly mark **[ILLEGIBLE]** and **[NOT FOUND]**. Never fill gaps with what seems reasonable.
- Flag referenced annexes that are not in the data room: this is the most common gap.
