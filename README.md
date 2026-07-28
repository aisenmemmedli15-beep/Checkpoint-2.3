# Vektor Saxlama və Oxşarlıq Axtarışı (Vector Storage & Similarity Search)

Bu layihə mətn məlumatlarının çoxölçülü **embedding vektorlarına** çevrilməsi, **ChromaDB** vektor bazasında saxlanılması və **Semantik Oxşarlıq Axtarışı (Similarity Search)** mexanizminin icrasını nümayiş etdirir.

# Layihə Haqqında

Axtarış sistemlərində klassik sözbəsöz (exact keyword match) axtarışlar əvəzinə, **semantik (məna baxımından) axtarış** istifadə olunur. Layihədə:
1. Mətnlər open-source `all-MiniLM-L6-v2` modeli ilə **384-ölçülü vektorlara** çevrilir.
2. Vektorlar və onlara aid metaməlumatlar **ChromaDB** lokal vektor bazasına yazılır.
3. Daxil edilən sorğu vektoru ilə bazadakı vektorlar arasında **Cosine Similarity (Kosinus Oxşarlığı)** hesablanaraq ən uyğun nəticələr (Top-K) tapılır.

# İstifadə Olunan Texnologiyalar

* **Dil:** Python 3.9+
* **Vektor Bazası (Vector Store):** ChromaDB (Free / Open-Source)
* **Embedding Modeli:** `sentence-transformers` (`all-MiniLM-L6-v2`)
* **Axtarış Metrikası:** Cosine Distance / Cosine Similarity

# Quraşdırma və İşə Salınma

 1. Tələb olunan kitabxanaları yükləyin:
```bash
pip install chromadb sentence-transformers
