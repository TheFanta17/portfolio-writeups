# Root-Me — Programmation — CAPTCHA me if you can
 
**Lien :** https://www.root-me.org/fr/Challenges/Programmation/CAPTCHA-me-if-you-can  
**Catégorie :** Programmation  
**Niveau :** Facile  
**Date :** 2025-09-20

---

## 🌍 Contexte
Automatiser la résolution d’un CAPTCHA simple (OCR / parsing) ou contourner une protection basique.

---

## 🔍 Approche
1. Tests manuels de la page web.
2. Prototype OCR local avec pytesseract et OpenCV.
3. Détection que le captcha est encodé en data URI (base64) dans le HTML.
4. Décodage Base64 -> OpenCV.
5. Prétraitement (grayscale, upscaling, morphological close, OTSU).
6. OCR avec whitelist et PSM adapté.
7. Maintien d'une session HTTP (requests.Session) pour POSTer le code rapidement.
8. Boucle automatique jusqu'à validation et affichage de la page de succès contenant le mot de passe.

---

## ✅ Résultat
Le script automatise GET -> OCR -> POST en conservant la session et affiche la page de validation contenant le mot de passe.
