# ⚙️ Machine Learning Operation

**Developer, Operations DevOps, MLOps, apa itu?**
Dulu, software development dan IT operations berjalan terpisah. Developer fokus membuat kode dan fitur baru, sementara Operations bertanggung jawab atas deployment dan pemeliharaan. Pendekatan ini menciptakan GAP pengetahuan antar tim, yang memicu berbagai masalah. Siklus rilis menjadi lambat karena deployment manual dan birokrasi. Kurangnya komunikasi menyebabkan misinterpretasi dan kesalahan. Perubahan kode yang tidak terintegrasi dengan baik menimbulkan masalah stabilitas. Kurangnya visibilitas antar tim, karena perbedaan tools dan akses, membuat proses pengembangan menjadi terhambat.

Secara umum, proses pengembangan aplikasi melibatkan dua tim utama: Developer (merancang, menulis, mengemas, dan menguji kode) dan IT Operations (merilis, men-deploy, mengoperasikan, dan memantau infrastruktur). Kedua tim ini memiliki tujuan yang sama: menyajikan aplikasi yang stabil kepada pengguna. Namun, perbedaan prioritas, tools, dan pola kerja seringkali menimbulkan konflik. Developer dituntut cepat, yang terkadang mengorbankan kualitas. IT Operations fokus pada stabilitas, yang sering terganggu oleh perubahan dari aplikasi. Konflik ini berujung pada kurangnya pemahaman dan komunikasi, yang seringkali berujung pada saling menyalahkan.

Kondisi ini menciptakan bottleneck yang menghambat kolaborasi dan efisiensi, yang pada akhirnya dapat merugikan perusahaan. Pengguna kecewa, feedback negatif, dan perusahaan berisiko kehilangan pasar.

Untuk mengatasi masalah ini, dan seiring dengan meningkatnya tuntutan pasar akan rilis software yang lebih cepat, muncullah konsep DevOps. DevOps adalah gabungan dari filosofi budaya, praktik, dan tools untuk meningkatkan kemampuan perusahaan dalam menyajikan aplikasi secara cepat. 

DevOps menekankan kolaborasi, menghilangkan hambatan, dan otomatisasi. Filosofi DevOps melibatkan berbagi tanggung jawab. Praktiknya merampingkan prosedur kerja tim. Tools DevOps mengotomatiskan tugas-tugas berulang. 

Dengan DevOps, Developer dan IT Operations dapat bersatu, berkolaborasi, dan berkomunikasi dengan lebih efektif, sehingga dapat meningkatkan inovasi, feedback pengguna, dan nilai bisnis.

Kesuksesan DevOps dalam mempercepat pengembangan perangkat lunak menginspirasi penerapan prinsip serupa pada Machine Learning, yang kemudian dikenal sebagai MLOps. MLOps bertujuan untuk menghilangkan GAP antara Machine Learning Engineer dan tim Operations, demi pelayanan terbaik kepada pengguna dan peningkatan revenue bisnis. Machine Learning Operations adalah proses untuk menerapkan dan memelihara model ML di produksi secara andal dan efisien. Analoginya, seorang chef tidak hanya membuat resep (model ML), tetapi juga memastikan hidangan tersaji konsisten (produksi model). 
<div align="center">
<img src="https://assets.cdn.dicoding.com/original/academy/dos-a10ab3b55e97e7b2810c27353a1a463c20250326150424.jpeg">
</div>

## Machine Learning Lifecycle
Dalam skala industri, pengembangan sistem machine learning biasanya melibatkan berbagai tim dengan keahlian, peran, dan kepentingan yang berbeda. Idealnya, tim-tim ini berkolaborasi dan menerapkan prinsip MLOps untuk menciptakan sistem yang reliable, scalable, adaptable, dan maintainable.

Dalam perusahaan yang mapan, data scientist biasanya membuat model machine learning, yang kemudian diserahkan kepada ML engineer dan software engineer untuk diintegrasikan ke dalam sistem produksi. Proses ini melibatkan beberapa tim yang saling "melempar" tugas dan menunggu, yang dapat memakan waktu dan menimbulkan masalah karena perbedaan beban kerja. 

<div align="center">
  <img src="https://github.com/user-attachments/assets/17d3b636-c781-44b7-82f1-5b9255109c65">
</div>

## MLOps Maturity
MLOps Maturity Level adalah kerangka kerja yang menunjukkan tingkat otomatisasi, struktur, dan integrasi proses operasional machine learning dalam sebuah organisasi. Tingkatan ini membantu perusahaan memahami posisi mereka dan memberikan arahan pengembangan. 

Tingkatan ini juga mencerminkan kemampuan perusahaan dalam mengelola siklus hidup machine learning, dari pengembangan hingga pengelolaan model di produksi.

Level kematangan ditentukan secara kualitatif berdasarkan aspek manusia/budaya, proses/struktur, dan objek/teknologi. Semakin tinggi levelnya, semakin tinggi tingkat kesulitannya, tetapi dampaknya juga semakin besar.

Berbeda dengan level perkembangan manusia yang pasti, MLOps maturity level tidak memiliki guideline yang baku. Setiap perusahaan dapat mengadopsi pendekatan yang berbeda. Namun, Google dan Microsoft menyediakan guideline dengan mengkategorikan maturity level menjadi tiga hingga lima level. Perbedaan jumlah level ini mencerminkan perbedaan tujuan, fokus, dan kebutuhan masing-masing organisasi.

# Rangkuman Membangun Model Machine Learning yang Andal
## Pengantar Model Machine Learning
Dalam pengembangan machine learning (ML), developer seringkali terlalu fokus pada pemodelan dan mengabaikan data pipeline. Membangun model tanpa data pipeline yang baik ibarat membangun rumah di atas pasir: model tampak mengesankan di awal, tetapi rentan kesalahan, bias, dan performa buruk. Banyak proyek ML gagal bukan karena algoritma yang buruk, tetapi karena kualitas dan integritas data yang diabaikan.

Kualitas data adalah salah satu "sayap" yang menunjang "terbangnya" model. Mengabaikan kualitas data atau pemilihan algoritma akan menghasilkan model yang buruk.

### Machine Learning Workflow
Machine learning workflow yang ideal (dikutip dari kelas Machine Learning untuk Pemula) meliputi beberapa tahapan seperti berikut.

1. Data Collecting
2. EDA (Exploratory Data Analysis)
3. Data Cleaning
4. Model Selection
5. Evaluation
6. Deployment
7. Monitoring
Proses di atas bersifat iteratif, artinya Anda bisa melakukan beberapa tahapan berulang kali hingga mencapai performa yang diinginkan.

### Pembagian Tugas dalam Tim
Dalam perusahaan, idealnya ada pembagian tugas untuk mencapai suatu tujuan. Pada sistem machine learning biasanya tugas akan dibagi seperti berikut ini.

- Data Engineers & Data Analysts: menangani hulu pengolahan data (ETL - Extract, Transform, Load), data store (data warehouse/data lake), dan feature store.
- Machine Learning Engineers: menerima data yang sudah "matang", bersih, dan terstruktur, sehingga dapat fokus pada pembangunan, pelatihan, dan evaluasi model.
Meskipun menerima data yang sudah bersih, machine learning engineer tetap perlu melakukan data wrangling (gathering, assessing, cleaning) agar data lebih sesuai dengan kebutuhan model.

Biasanya Anda melakukan proses tersebut secara manual satu per satu, hal tersebut dapat menimbulkan masalah sehingga Anda harus mencari solusinya.

- Masalah: menjalankan data loading dan preprocessing berulang kali dapat menghasilkan model yang tidak konsisten dan memakan waktu.
- Solusi: membungkus data loading dan preprocessing menjadi satu fungsi untuk menghindari duplikasi kode, memastikan konsistensi, mempermudah maintenance, dan memungkinkan otomatisasi alur kerja data.
Otomatisasi Data Pipeline
### Modul ini akan menyempurnakan alur kerja continuous training dengan GitHub Actions, dengan menambahkan otomatisasi untuk validasi dan pemrosesan data sebelum pelatihan model.

Kesimpulannya, membangun model ML yang andal membutuhkan konfigurasi yang seimbang antara kualitas data dan pemilihan algoritma. Data pipeline yang baik adalah fondasi penting. Modul ini akan mematangkan workflow dengan otomatisasi data pipeline, serta membahas basic manner pengumpulan data dan model statis vs. dinamis.

# MLFlow
MLflow adalah platform open-source yang dirancang untuk mengelola alur kerja machine learning (ML) secara end-to-end. MLflow membantu para data scientist, machine learning engineer, dan tim pengembang untuk mencatat, melacak, mengelola, dan mendistribusikan model ML dengan lebih mudah. Dengan MLflow, semua elemen penting dalam proyek ML, seperti eksperimen, parameter, metrik, artefak, dan model, dapat dikelola secara terpusat.

<div align="center">
  <img src="https://assets.cdn.dicoding.com/original/academy/dos-03fdb97d263203c84a96e772408312bf20250318124211.png">
</div>

MLflow dapat digunakan bersama dengan berbagai library machine learning seperti TensorFlow, PyTorch, Scikit-learn, XGBoost, dan 20 library lainnya. 

<div align="center">
  <img src="https://assets.cdn.dicoding.com/original/academy/dos-617d1438bb19061a33e93933abb489f420250318123301.jpeg">
</div>

Platform ini juga mendukung integrasi dengan alat CI/CD seperti GitHub untuk mempermudah implementasi dan manajemen model di lingkungan produksi. Tidak berhenti di sini, sebagai tools yang sangat powerful tentunya MLflow memiliki berbagai macam fitur yang siap membantu Anda membangun sistem machine learning.

Tools ini memiliki beberapa fitur utama yang wajib Anda ketahui seperti berikut ini.

1. MLflow Tracking
MLflow Tracking adalah komponen yang memungkinkan pengguna untuk mencatat dan melacak eksperimen machine learning. Dengan fitur ini, semua informasi penting seperti parameter, metrik, kode sumber, dan artefak (seperti file model) dapat didokumentasikan secara otomatis.

2. MLflow Project
MLflow Projects membantu pengguna mendokumentasikan dan mengemas proyek machine learning dalam format yang terstandarisasi. Setiap proyek akan berisi file konfigurasi (MLproject) yang menjelaskan cara menjalankan proyek tersebut sehingga proyek dapat dipindahkan antar lingkungan dengan mudah.

3. MLflow Model
MLflow Models adalah salah satu komponen utama dari MLflow yang dirancang untuk menyimpan, mengelola, dan mendistribusikan model machine learning. MLflow Models memungkinkan pengguna untuk menyimpan model dalam format standar yang dapat digunakan ulang di berbagai platform dan mempermudah deployment model ke lingkungan produksi.

4. MLflow Model Registry
MLflow Model Registry adalah komponen dari MLflow yang dirancang untuk mengelola siklus hidup model machine learning secara terpusat. Model Registry memungkinkan pengguna untuk melacak versi model, memberikan anotasi, mengelola tahapan (staging, production, archived), dan mencatat metadata terkait model yang telah dicatat di MLflow Tracking.

5. MLflow Pipelines (Experimental)
MLflow Pipelines merupakan fitur eksperimental dari MLflow yang dirancang untuk menyediakan kerangka kerja modular, terstruktur, dan terotomatisasi untuk pengembangan machine learning. Fitur ini membantu kita untuk membangun pipeline pengembangan dan deployment model dengan lebih mudah dan efisien, sekaligus memastikan konsistensi alur kerja. Sayangnya, sesuai dengan namanya fitur ini masih berupa eksperimen yang berarti kita tidak dapat menggunakan fitur ini selain menggunakan MLflow versi 1.30.1 (setidaknya sampai 29 Desember 2024).

# Github Actions
<div align="center">
  <img src="https://images.ctfassets.net/8aevphvgewt8/KiQBgcnMQg6dALaS6erGk/f8d49c0cc5a461b903e52d08c3c3b8f6/actions-hero.webp?w=2496&fm=webp&q=90"> 
</div>
GitHub Actions adalah fitur dari GitHub yang digunakan untuk mengotomatisasi berbagai proses pengembangan perangkat lunak, terutama dalam konteks CI/CD (Continuous Integration dan Continuous Deployment). Dengan GitHub Actions, kamu dapat membuat workflow yang secara otomatis menjalankan tugas-tugas seperti membangun (build), menguji (test), dan mendistribusikan (deploy) aplikasi setiap kali terjadi perubahan dalam repositori, misalnya saat melakukan push ke branch tertentu atau membuat pull request. Selain itu, GitHub Actions juga dapat digunakan untuk menjalankan skrip otomatis seperti formatting kode, pengecekan keamanan, pengiriman notifikasi, dan publikasi artefak seperti Docker image atau paket Python. Workflow ini ditulis dalam file YAML di dalam direktori .github/workflows, dan dapat dikonfigurasi untuk berjalan di berbagai sistem operasi seperti Linux, Windows, atau macOS. Dengan demikian, GitHub Actions sangat membantu dalam mempercepat proses pengembangan, meningkatkan kualitas kode, dan mengurangi beban kerja manual melalui otomatisasi.

# Docker
<div align="center">
  <img src="https://www.docker.com/app/uploads/2025/04/pny-dbc-docker-desktop-home.png">
</div>
Docker adalah platform open-source yang memungkinkan developer untuk membuat, menjalankan, dan mendistribusikan aplikasi di dalam container. Container adalah unit ringan dan portabel yang mengemas semua hal yang dibutuhkan aplikasi—termasuk kode, runtime, sistem pustaka, dan dependensi lainnya—ke dalam satu paket. Dengan menggunakan Docker, aplikasi dapat dijalankan dengan cara yang konsisten di berbagai lingkungan, baik itu di laptop pengembang, server staging, maupun server produksi. Hal ini mengurangi masalah “works on my machine” dan mempercepat proses deployment secara signifikan.

# Prometheus
<div align="center">
  <img src="https://prometheus.io/_next/static/media/prometheus-logo.7aa022e5.svg">
</div>

Prometheus adalah sistem monitoring dan alerting open-source yang dirancang khusus untuk mengumpulkan dan menyimpan metrik secara time-series. Prometheus secara aktif men-scrape data metrik dari endpoint HTTP yang disebut /metrics, lalu menyimpannya dalam format yang bisa dikueri menggunakan bahasa bernama PromQL. Dengan fitur seperti alerting rules dan integrasi dengan berbagai sistem, Prometheus sangat ideal untuk memantau performa sistem dan aplikasi secara real-time, mendeteksi anomali, dan membantu dalam troubleshooting serta observability.

# Grafana
<div align="center">
  <img src="https://grafana.com/media/home/workflows/workflow_2.png?w=1920">
</div>
Grafana adalah platform visualisasi data open-source yang sering digunakan bersama Prometheus. Ia memungkinkan pengguna membuat dashboard interaktif yang menampilkan metrik, log, dan alert dalam bentuk grafik yang informatif dan real-time. Dengan Grafana, tim pengembang dapat dengan mudah memahami tren performa, penggunaan resource, atau pola kesalahan tanpa harus melihat data mentah. Grafana mendukung banyak sumber data, tidak hanya Prometheus, tapi juga Elasticsearch, InfluxDB, PostgreSQL, dan lainnya.

## Kenapa Penting ketika digabungkan?
Ketika Docker, Prometheus, dan Grafana digabungkan dalam sebuah alur kerja DevOps, mereka menciptakan ekosistem yang sangat efisien, portabel, dan dapat diobservasi. Docker menjamin konsistensi lingkungan pengembangan hingga produksi, Prometheus memungkinkan pemantauan performa aplikasi dan sistem secara detail, dan Grafana menyajikan visualisasi data yang mudah dicerna. Kombinasi ketiganya memberikan efisiensi dalam bentuk:
- Pengurangan waktu debugging dan downtime, karena sistem lebih mudah dipantau.
- Cepat dalam pengujian dan deployment dengan containerisasi Docker.
- Kemampuan membuat alert otomatis untuk memitigasi kegagalan sistem lebih dini.
- Observability menyeluruh, mulai dari performa model ML, API latency, hingga penggunaan CPU dan RAM, semuanya dalam satu dashboard.

Singkatnya, integrasi Docker + Prometheus + Grafana menjadikan proses pengembangan, deployment, dan pemantauan lebih otomatis, dapat dipercaya, dan skalabel.

# Dokumentasi Hasil Latihan
Saya berhasil membuat dashboard sederhana dengan melakukan monitoring performa CPU, RAM, Jumlah request endpoint, dan juga Latensi.
<div align="center">
  <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2016.25.13.png">
</div>
Dapat dilihat setiap matrik/visualisasi memiliki manfaatnya masing-masing dan dapat dilihat secara realtime. Kemudian Saya membuat sistem alerting dimana ketika model Machine Learning telah melakukan prediksi sebanyak 4000 kali, maka Grafana akan memberikan alert kepada saya melalui email dan menganjurkan untuk melatih kembali model Machine Learning agar menghindari Drifting atau pegeseran akurasi karena jumlah dataset atau trend yang berubah.
<div align="center">
  <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2016.25.53.png">
</div>
Sehingga ketika 
