# ARC Prize 2025: Neuro-Symbolic Solver for Abstraction and Reasoning Corpus

## Deskripsi Proyek

Repositori ini berisi solusi untuk kompetisi [ARC Prize 2025](https://www.kaggle.com/competitions/arc-prize-2025/overview), yang menantang peserta untuk membangun sistem AGI (Artificial General Intelligence) yang mampu menyelesaikan berbagai task visual berbasis grid, mirip dengan penalaran manusia. Solusi ini menggabungkan pendekatan **neuro-symbolic**: mengombinasikan encoder persepsi berbasis CNN (Convolutional Neural Network) dengan pencarian program simbolik (beam search) untuk mensintesis solusi task.

## Struktur Proyek

- `arc-prize-2025.ipynb` — Notebook utama berisi seluruh pipeline:
  - Eksplorasi data (EDA)
  - Baseline heuristik
  - Training perception encoder (CNN-Siamese)
  - Definisi DSL (Domain-Specific Language) untuk operasi grid
  - Beam search program synthesis
  - Evaluasi, tuning, dan profiling
  - Pembuatan file submission

## Fitur Utama

- **Data Loader**: Loader robust untuk format data ARC (JSON), baik training, evaluation, maupun test.
- **Perception Encoder**: CNN-Siamese yang memetakan grid ke embedding vektor.
- **Neuro-Symbolic Solver**: Kombinasi encoder neural dan pencarian program simbolik (beam search) dengan scoring gabungan pixel dan neural similarity.
- **Hyperparameter Tuning**: Grid search untuk beam width, depth, dan alpha (bobot scoring).
- **Profiling & Submission**: Analisis kecepatan, kompleksitas program, dan validasi format submission.

## Cara Menjalankan

1. **Lingkungan**: Notebook didesain untuk dijalankan di Kaggle Notebook (Python 3, GPU recommended). Semua dependensi utama (numpy, pandas, torch, tqdm, matplotlib, scikit-learn) sudah tersedia di image Kaggle.
2. **Data**: Data input tersedia otomatis di `/kaggle/input/arc-prize-2025/` saat dijalankan di lingkungan kompetisi.
3. **Training Encoder**: Jalankan sel training untuk melatih perception encoder. Model akan disimpan sebagai `perception_encoder_trained.pth`.
4. **Evaluasi & Submission**: Jalankan sel evaluasi dan submission untuk menghasilkan file `submission.json` sesuai format kompetisi.

## Dependensi

- Python 3.8+
- numpy
- pandas
- torch
- tqdm
- matplotlib
- scikit-learn

## Reproduksi & Adaptasi Lokal

Jika ingin menjalankan di luar Kaggle:
- Pastikan seluruh dependensi terinstal (`pip install -r requirements.txt`)
- Download dataset ARC Prize 2025 dari Kaggle dan letakkan di folder `input/arc-prize-2025/`
- Ubah path data di notebook dari `/kaggle/input/arc-prize-2025/` ke path lokal Anda.

## Referensi
- [ARC Prize 2025 - Kaggle](https://www.kaggle.com/competitions/arc-prize-2025/overview)
- [Original ARC Dataset](https://github.com/fchollet/ARC)

## Author
- [Pasha Akrilian](https://github.com/PashaAkrilian)

---

> Untuk pertanyaan, diskusi, atau kontribusi, silakan buka issue atau pull request di repositori ini. 