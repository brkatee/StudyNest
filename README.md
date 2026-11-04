# StudyNest

Aplicație web/mobilă pentru studiu activ: încarci un PDF sau DOCX și obții automat concepte cheie, întrebări, quiz, flashcards și hartă mentală. Datele rămân salvate local (IndexedDB).

## Funcții
- Upload PDF/DOCX (drag-and-drop), extragere text cu [pdf.js](https://mozilla.github.io/pdf.js/) și [mammoth.js](https://github.com/mwilliamson/mammoth.js)
- Generare locală (euristică) de concepte, idei principale, întrebări
- Editare manuală a textului și a întrebărilor
- Quiz (grilă / răspuns scurt) cu scor și istoric
- Flashcards, hartă mentală, note
- Persistență în IndexedDB (fișier original, text, carduri, scoruri)

## Rulare
Fișier static, fără build. Deschide `index.html` printr-un server local:

```bash
python3 -m http.server 8000
```

Apoi accesează http://localhost:8000. Necesită internet pentru bibliotecile de pe cdnjs.

## Publicare pe GitHub Pages
Repository → Settings → Pages → Source: **GitHub Actions**. Workflow-ul din `.github/workflows/pages.yml` publică la fiecare push pe `main`.

## Note
Butonul „Generează cu AI” funcționează doar în versiunea găzduită pe claude.ai; în rest se folosește generarea locală.

## Idei următoare
Export carduri (CSV/Anki), OCR pentru PDF-uri scanate (Tesseract.js).
