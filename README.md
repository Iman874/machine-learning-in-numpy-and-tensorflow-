# machine-learning-in-numpy-and-tensorflow-
Tiny machine learning in numpy and machine learning

# Penjelasan Kode

## Import Library:

numpy (sebagai np): Digunakan untuk operasi numerik, terutama array (seperti data fitur dan label).
tensorflow (sebagai tf): Framework deep learning untuk membangun dan melatih model neural network.

## Data Latihan:

X_train: Array numpy berisi fitur karyawan (misalnya, pengalaman, skill, penilaian). Setiap baris mewakili satu karyawan, dan setiap kolom mewakili satu fitur.
y_train: Array numpy berisi label kinerja karyawan (1 untuk "bagus", 0 untuk "tidak bagus").

## Membuat Model:

tf.keras.Sequential: Mendefinisikan model neural network sederhana dengan lapisan-lapisan yang berurutan.
tf.keras.layers.Dense(1, input_shape=(3,), activation='sigmoid'):
Satu lapisan "Dense" (terhubung penuh) dengan 1 neuron (karena kita memprediksi biner "bagus"/"tidak bagus").
input_shape=(3,): Menunjukkan bahwa setiap sampel input memiliki 3 fitur.
activation='sigmoid': Fungsi aktivasi sigmoid untuk menghasilkan probabilitas (0 hingga 1) sebagai output.

## Kompilasi Model:

optimizer='adam': Algoritma optimasi Adam untuk menyesuaikan bobot model selama pelatihan.
loss='binary_crossentropy': Fungsi kerugian untuk masalah klasifikasi biner.
metrics=['accuracy': Metrik yang akan dipantau selama pelatihan (akurasi dalam hal ini).

## Pelatihan Model:

model.fit(X_train, y_train, epochs=1000, verbose=0):
Melatih model selama 1000 epochs (iterasi penuh pada data latihan).
verbose=0: Tidak menampilkan output selama pelatihan (untuk contoh ini).

## Data Karyawan Baru:

data_karyawan_baru: Array numpy berisi fitur karyawan baru yang akan diprediksi.

## Prediksi:

model.predict(data_karyawan_baru): Menghasilkan probabilitas karyawan baru berkinerja "bagus" atau "tidak bagus"

## Interpretasi Prediksi:

Jika probabilitas > 0.5, maka dianggap "bagus".
Jika tidak, dianggap "tidak bagus".
