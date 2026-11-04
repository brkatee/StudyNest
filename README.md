# StudyNest

Aplicație web/mobilă pentru studiu activ: încarci un PDF sau DOCX și obții automat concepte cheie, întrebări, quiz, flashcards și hartă mentală. Datele rămân salvate local (IndexedDB).

## Funcții
- Upload PDF/DOCX (drag-and-drop), extragere text cu [pdf.js](https://mozilla.github.io/pdf.js/) și [mammoth.js](https://github.com/mwilliamson/mammoth.js)
- Generare locală (euristică) de concepte, idei principale, întrebări
- Editare manuală a textului și a întrebărilor
- Quiz cu alegere unică, alegere multiplă și răspuns scurt, cu scor și istoric
- Flashcards, hartă mentală, note
- Spațiu personal cu documente încărcate, volum, progres, ultima activitate și greșeli
- Persistență locală în IndexedDB (fișier original, text, carduri, scoruri și greșeli); datele nu se sincronizează între dispozitive

## Rulare
Fișier static, fără build. Deschide `index.html` printr-un server local:

```bash
python3 -m http.server 8000
```

Apoi accesează http://localhost:8000. Necesită internet pentru bibliotecile de pe cdnjs.

## Publicare pe GitHub Pages
Repository → Settings → Pages → Source: **GitHub Actions**. Workflow-ul din `.github/workflows/pages.yml` publică la fiecare push pe `main`.

## Note
Butonul „Generează cu AI” folosește serviciul Claude când aplicația rulează într-un mediu care îl oferă. Într-un site static obișnuit, generează automat întrebări local și indică explicit fallback-ul; aceasta nu este generare AI. Tipul întrebării și răspunsurile corecte/greșite sunt completate automat. Citatele AI sunt verificate când sunt furnizate, dar nu garantează corectitudinea; verifică manual întrebările și răspunsurile.

## Idei următoare
Export carduri (CSV/Anki), OCR pentru PDF-uri scanate (Tesseract.js).
