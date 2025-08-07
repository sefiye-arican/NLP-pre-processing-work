# NLP Pre‑Processing Work

Bu çalışma, 2023 yazında gerçekleştirdiğim bir staj sürecinde yaptığım **başlangıç seviyesi bir doğal dil işleme (NLP) ön işleme projesidir**. Amaç, metin verileri üzerinde temel ön işleme adımlarını uygulayarak bu verileri analiz ve modelleme için hazır hâle getirmektir.

---

## İçindekiler

- [Genel Bakış](#genel-bakış)  
- [Kullanılan Teknolojiler](#kullanılan-teknolojiler)  
- [Ön İşleme Adımları](#ön-i̇şleme-adımları)  
  - Temizleme  
  - Tokenizasyon  
  - Stop-word çıkarımı  
  - Stemming ve Lemmatization  
- [Nasıl Kullanılır?](#nasıl-kullanılır)

---

## Genel Bakış

Bu proje, metin verilerini analiz ve modelleme adımlarına hazırlamak için gereken yaygın NLP ön işlem tekniklerini içerir. Hedeflenen temel işlemler:

- Ham metinleri temizlemek (HTML, URL, rakam, özel karakter vb.)
- Metni tokenize edip anlamlı parçalara bölmek
- Gereksiz kelimeleri çıkarmak (stop‑words)
- Kelimelerin temeldeki hâline dönüştürülmesi (stemming/lemmatization)

Bu adımlar sayesinde sentiment analizi, metin sınıflandırma veya konu modelleme gibi NLP görevleri için veri hazırlığı sağlanır.

---

## Kullanılan Teknolojiler

| Teknoloji            | Kullanım Alanı                      |
|----------------------|-------------------------------------|
| Python               | Temel programlama dili              |
| regex                | Metin temizleme (örneğin URL’ler)   |
| NLTK / SpaCy         | Tokenizasyon, stop‑word, lemmatizer |
| BeautifulSoup        | HTML etiket temizleme               |
| Gensim, Scikit‑Learn | Vektör dönüşümleri (örneğin TF‑IDF) |

---

## Ön İşleme Adımları

### 🧼 1. Temizleme (Cleaning)

- Küçük harfe dönüştürme (lowercase)
- HTML/XML etiketlerinin kaldırılması
- URL, e‑posta ve sayılar gibi özel desenlerin silinmesi
- Noktalama işaretleri ve gereksiz karakterlerin temizlenmesi

### ✂️ 2. Tokenizasyon

- Cümle ve kelime bazında bölme (örneğin `nltk.tokenize.word_tokenize`)
- Gerektiğinde özel tokenizasyon (örneğin tweet, chat dili)

### 🚫 3. Stop‑Word Çıkarımı

- Sık kullanılan anlamsız kelimelerin (örneğin “ve”, “the”, “is”) metinden çıkarılması

### 🌱 4. Kök ve Lemma İşlemleri

- **Stemming**: Kelimeleri kök hâline (stem) indirgeme
- **Lemmatization**: Bağlama göre anlamlı hâle lemmatize etme

---

## Nasıl Kullanılır?

1. Bu depoyu klonlayın:

   ```bash
   git clone https://github.com/sefiye-arican/NLP-pre-processing-work.git
   cd NLP-pre-processing-work

2. Gerekli kütüphaneleri kurun:
   ```bash
    pip install -r requirements.txt
   
3. Python ortamında örnek notebook'ları açarak takip edin:
    ```bash
    jupyter notebook

- `text_cleaning.ipynb` (veya diğer notebook dosyaları) üzerinde anlatımlı örnekler yer almaktadır.

4. Adım adım uygulama:

  - `clean_text()` fonksiyonu ile temizlik  
  - `tokenize_text()` ile tokenizasyon  
  - `remove_stopwords()` ile stop‑word çıkarımı  
  - `stem_or_lemmatize()` ile kelime köküne ya da lemma’ya dönüştürme


# NLP Pre‑Processing Work

This project is a **beginner-level natural language processing (NLP) pre-processing study** I developed during my internship in the summer of 2023. The goal is to apply fundamental pre-processing steps on text data to prepare it for analysis and modeling.

---

## Table of Contents

- [Overview](#overview)  
- [Technologies Used](#technologies-used)  
- [Pre-processing Steps](#pre-processing-steps)  
  - Cleaning  
  - Tokenization  
  - Stop-word Removal  
  - Stemming and Lemmatization  
- [How to Use](#how-to-use)

---

## Overview

This project includes common NLP pre-processing techniques to prepare text data for analysis and modeling. The main operations are:

- Cleaning raw text (HTML tags, URLs, numbers, special characters, etc.)
- Tokenizing text into meaningful components
- Removing unnecessary words (stop-words)
- Reducing words to their base form (stemming/lemmatization)

These steps help prepare datasets for tasks such as sentiment analysis, text classification, and topic modeling.

---

## Technologies Used

| Technology           | Purpose                            |
|----------------------|-------------------------------------|
| Python               | Main programming language           |
| regex                | Pattern-based text cleaning         |
| NLTK / SpaCy         | Tokenization, stop-word removal, lemmatization |
| BeautifulSoup        | HTML tag removal                    |
| Gensim, Scikit-Learn | Text vectorization (e.g. TF-IDF)    |

---

## Pre-processing Steps

### 🧼 1. Cleaning

- Convert text to lowercase
- Remove HTML/XML tags
- Remove patterns like URLs, emails, numbers
- Remove punctuation and unnecessary characters

### ✂️ 2. Tokenization

- Split text into sentences and words (e.g., `nltk.tokenize.word_tokenize`)
- Custom tokenization for tweets or chat-style texts if needed

### 🚫 3. Stop-word Removal

- Remove common words that add little meaning (e.g., “and”, “the”, “is”)

### 🌱 4. Stemming and Lemmatization

- **Stemming**: Reduce words to their stem forms
- **Lemmatization**: Reduce words to their lemma based on context

---

## How to Use

1. Clone this repository:

   ```bash
   git clone https://github.com/sefiye-arican/NLP-pre-processing-work.git
   cd NLP-pre-processing-work
