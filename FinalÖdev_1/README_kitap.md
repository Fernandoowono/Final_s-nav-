# Final Ödev-1: Türkçe Kitap/Edebiyat Veri Seti – NLP Ön İşleme Pipeline

**Öğrenci:** Matias Fernando Ndong Owono Obiang
**Öğrenci No:** 2311081634  
**Ders:** Doğal Dil İşleme  
**Öğretim Üyesi:** Dr. Rabia Yaşa Koştaş  

---

## 📌 Projenin Amacı

Türk ve dünya edebiyatına ait 40 kitap özetini içeren Türkçe veri seti üzerinde temel NLP ön işleme adımları uygulanmış ve Zipf Yasası analizi gerçekleştirilmiştir.

---

## 📂 Veri Seti

| Özellik | Değer |
|---|---|
| Kaynak | Goodreads, Kitapyurdu, D&R |
| Toplam Kitap | 40 |
| Tür Sayısı | 4 (Roman, Şiir, Novella, Çocuk/Yetişkin) |
| Kategori | Türk Edebiyatı, Çeviri, Divan Edebiyatı |
| Dosya Boyutu | ~22 KB (0.022 MB) |
| Dosya Formatı | CSV (UTF-8-BOM) |

### Sütun Yapısı

| Sütun | Açıklama |
|---|---|
| `Kitap_ID` | Benzersiz kimlik (KIT001–KIT040) |
| `Baslik` | Kitap adı |
| `Yazar` | Yazarın adı |
| `Tur` | Edebi tür |
| `Kategori` | Türk Edebiyatı / Çeviri / Divan |
| `Kaynak` | Özet kaynağı |
| `Yayın_Yili` | İlk yayın yılı |
| `Ozet` | Ham Türkçe kitap özeti |

---

## ⚙️ Uygulanan Ön İşleme Adımları

| Adım | Kütüphane | Açıklama |
|---|---|---|
| Metin Temizleme | `re` | HTML, sayı, özel karakter kaldırıldı |
| Lowercasing | Python built-in | İ→i, I→ı Türkçe düzeltmesiyle |
| Tokenization | `nltk` | Kelime + cümle tokenization |
| Stop Word | `nltk` + özel liste | Türkçe stop words çıkarıldı |
| Stemming | `snowballstemmer` | Snowball Turkish algoritması |
| Lemmatization | Kural tabanlı | 30+ Türkçe ek kalıbı |

---

## 📁 Repo İçeriği

```
├── turk_kitap_nlp.ipynb           # Ana Jupyter Notebook
├── turk_kitap_ham.csv             # Ham veri seti
├── turk_kitap_stemmed.csv         # Stemming uygulanmış
├── turk_kitap_lemmatized.csv      # Lemmatization uygulanmış
└── README.md
```

---

## 🛠️ Kurulum

```bash
pip install nltk pandas matplotlib numpy snowballstemmer
```
