# Analisis Audio & Noise Statis

## Deskripsi

Tugas ini merupakan analisis sinyal audio dengan menggunakan Python. Audio direkam dengan adanya sumber noise statis, kemudian dianalisis menggunakan beberapa bentuk visualisasi sinyal dan dilakukan proses resampling untuk melihat pengaruh aliasing.

## Analisis Audio

Analisis audio yang dilakukan meliputi:

1. **Waveform**
   - Menampilkan perubahan amplitudo sinyal terhadap waktu.
   - Digunakan untuk melihat bagian ketika terdapat suara dan noise pada rekaman.

2. **FFT Spectrum**
   - Menampilkan komponen frekuensi yang terdapat pada audio.
   - Digunakan untuk melihat frekuensi yang dominan pada rekaman.

3. **STFT Spectrogram**
   - Menampilkan perubahan frekuensi terhadap waktu.
   - Digunakan untuk melihat karakteristik suara dan noise statis selama rekaman.

4. **Mel Spectrogram**
   - Menampilkan karakteristik audio menggunakan skala frekuensi Mel.
   - Skala ini lebih sesuai dengan persepsi pendengaran manusia.

## Resampling dan Aliasing

Audio asli memiliki sampling rate sebesar **48.000 Hz** dan kemudian dilakukan downsampling menjadi **8.000 Hz**.

Terdapat dua metode yang dibandingkan:

- **Naive Downsampling**: mengambil setiap sampel ke-6 tanpa filter anti-aliasing.
- **Filtered Resampling**: melakukan resampling dengan filter anti-aliasing untuk mengurangi komponen frekuensi yang dapat menyebabkan aliasing.

Hasil kedua metode dibandingkan menggunakan spectrogram.

## File

- `tugas_audio_noise_statis.ipynb` — Notebook analisis audio.
- `tugas_audio_noise_statis.pdf` — Hasil notebook dalam bentuk PDF.
- `audio_original.wav` — Audio hasil rekaman asli.
- `audio_downsampled_naive.wav` — Hasil naive downsampling.
- `audio_downsampled_clean.wav` — Hasil filtered resampling.
- `waveform_recording.png` — Visualisasi waveform.
- `fft_dbfs.png` — Visualisasi FFT spectrum.
- `stft_spectrogram.png` — Visualisasi STFT spectrogram.
- `mel_spectrogram.png` — Visualisasi Mel spectrogram.
- `spectrogram_naive.png` — Spectrogram hasil naive downsampling.
- `spectrogram_clean.png` — Spectrogram hasil filtered resampling.
- `perbandingan_aliasing.png` — Perbandingan hasil naive dan filtered resampling.
