# ✋ Pelacakan Gestur Tangan dengan OpenCV & MediaPipe

Sebuah prototipe computer vision sederhana yang mampu melacak pergerakan tangan dan mengenali gestur dasar secara langsung dari feed webcam. Proyek ini dibangun untuk mengeksplorasi sistem interaksi manusia-komputer (Human-Computer Interaction) yang intuitif.

<p align="center">
  <img src="https://github.com/KMoex-HZ/Hand-Tracking/blob/main/demo.gif?raw=true" alt="Demo Pelacakan Tangan" width="700">
</p>

---

### ✨ Fitur Utama

- **Pelacakan Tangan Langsung:** Menggunakan feed webcam untuk mendeteksi dan melacak posisi tangan secara *real-time*.
- **Deteksi Landmark Tangan:** Mengimplementasikan library MediaPipe untuk mendapatkan 21 titik landmark pada tangan dengan presisi tinggi.
- **Pengenalan Gestur Sederhana:** Dilengkapi dengan logika kustom untuk mengenali gestur spesifik, seperti "Thumbs-Up" (Jempol ke Atas).
- **Visualisasi Hasil:** Menampilkan hasil deteksi (landmark dan nama gestur) secara langsung pada jendela video output menggunakan OpenCV.

---

### 🛠️ Tumpukan Teknologi (Tech Stack)

- **Bahasa:** Python
- **Library Utama:**
  - **OpenCV:** Untuk pemrosesan gambar dan video, serta menampilkan output.
  - **MediaPipe:** Untuk model deteksi tangan dan landmark yang sudah terlatih.
  - **NumPy:** Untuk manipulasi numerik pada koordinat landmark.

---

### 🚀 Instalasi & Cara Menjalankan

Untuk menjalankan proyek ini di komputermu, ikuti langkah-langkah berikut:

**Langkah 1: Clone Repository**
```bash
git clone [https://github.com/KMoex-HZ/Hand-Tracking.git](https://github.com/KMoex-HZ/Hand-Tracking.git)
cd Hand-Tracking
```
**Langkah 2: Buat Virtual Environment & Instal Dependensi**
```
# Pastikan kamu sudah punya file requirements.txt
pip install -r requirements.txt
```
```
# belum punya requirements.txt, instal manual:
pip install opencv-python mediapipe numpy
```
**Langkah 3: Jalankan Aplikasi**
```
python main.py 
# Atau nama file utama Python-mu
```

### ⚙️ Cara Kerja
- Inisialisasi: OpenCV diinisialisasi untuk menangkap frame video dari webcam. Model deteksi tangan dari MediaPipe juga disiapkan.
- Deteksi Landmark: Setiap frame dari video diproses oleh MediaPipe. Jika tangan terdeteksi, model akan mengembalikan 21 titik koordinat (landmark) untuk tangan tersebut.
- Logika Gestur: Sebuah fungsi kustom menganalisis posisi vertikal dari landmark ujung ibu jari terhadap landmark pangkal jari telunjuk untuk menentukan apakah gestur "Thumbs-Up" sedang dilakukan.
- Tampilan Output: OpenCV digunakan untuk menggambar titik-titik landmark dan garis penghubung di atas gambar tangan, serta menampilkan teks hasil deteksi gestur ("Thumbs Up!") pada layar.
