# Al-Bader Model Question Papers (SKIMVB)

Official repository for hosting Samastha Kerala Islam Matha Vidyabhyasa Board model question papers for the Al-Bader Application.

## Structure

```text
papers/
  └── <classId>/                # class-1 to class-10, class-plus-1, class-plus-2
      └── <examTerm>/           # quarterly, half_yearly, annual, class_test
          └── <subjectKey>.pdf  # e.g., fiqh.pdf, thafheem-1.pdf, aqeeda.pdf
```

## Adding a New Question Paper

1. Place the PDF in the appropriate folder:
   `papers/<classId>/<examTerm>/<subjectKey>.pdf`

2. Add an entry to `manifest.json`:
   ```json
   {
     "id": "class-5_half_yearly_fiqh",
     "classId": "class-5",
     "examTerm": "half_yearly",
     "subject": {
       "malayalam": "ഫിഖ്ഹ്",
       "english": "Fiqh",
       "arabic": "الفقه"
     },
     "fileSize": "173 KB",
     "pdfUrl": "https://cdn.jsdelivr.net/gh/salahudheen9847/al-bader-model-questions@main/papers/class-5/half_yearly/fiqh.pdf"
   }
   ```

3. Commit & push:
   ```bash
   git add .
   git commit -m "Add question paper"
   git push origin main
   ```
