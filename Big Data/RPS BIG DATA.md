# EPOCH DIGITAL


# RENCANA PEMBELAJARAN SEMESTER

**Mata Kuliah**: Praktikum Pengantar Big Data  
**Pembina**: Adam Setiadi, S.Kom  
**Prasyarat**: Basis Data, Pemrograman Lanjut

---

## CAPAIAN PEMBELAJARAN

Setelah mengikuti Pembelajaran ini, mahasiswa diharapkan mampu:

### Sikap:
Mampu menunjukkan sikap bertanggung jawab atas pekerjaan di bidang keahliannya secara mandiri dan dapat diberi tanggung jawab atas pencapaian hasil kerja tim dalam proyek analisis dan pemrosesan Big Data.

### Pengetahuan:
Menguasai pengetahuan teoretis dan faktual mengenai ekosistem Big Data, mencakup konsep arsitektur sistem terdistribusi, prinsip-prinsip pemrosesan data dalam skala besar, teknologi Hadoop dan Spark, serta metodologi analisis data untuk merancang dan membangun solusi Big Data yang fungsional pada lingkungan Linux.

### Keterampilan:
Mampu menerapkan pemikiran logis, kritis, sistematis, dan inovatif dalam konteks pengembangan atau implementasi ilmu pengetahuan dan teknologi yang memperhatikan dan menerapkan nilai humaniora yang sesuai dengan bidang keahliannya untuk memecahkan masalah pemrosesan dan analisis data dalam skala besar.

### Keterampilan Khusus:
Mampu mengaplikasikan konsep, prinsip, dan teknik-teknik Big Data untuk merancang, membangun, dan menguji sistem pemrosesan data terdistribusi menggunakan teknologi Hadoop, Spark, dan tools Big Data lainnya pada sistem operasi Ubuntu Linux melalui Virtual Machine.

---

## RENCANA PERTEMUAN

| Pertemuan | Kemampuan Akhir yang Diharapkan | Bahan Kajian (Materi Ajar) | Bentuk Pembelajaran | Pengalaman Belajar | Kriteria Penilaian (Indikator) | Indikator | Bobot |
|-----------|----------------------------------|----------------------------|---------------------|-------------------|-------------------------------|-----------|-------|
| **1** | Mampu menginstal dan mengonfigurasi Virtual Machine dengan Ubuntu Linux untuk environment Big Data. | Setup Environment Big Data: Instalasi VirtualBox/VMware, Download Ubuntu 22.04/24.04 LTS, Konfigurasi VM (RAM, Storage, Network), Instalasi Ubuntu Desktop, Update sistem (apt update & upgrade). | Praktikum, Demonstrasi | Mahasiswa menginstal VirtualBox di Windows, membuat VM baru, menginstal Ubuntu Linux, dan melakukan konfigurasi dasar sistem operasi. | Keberhasilan instalasi VM dan OS Ubuntu. | 1. VirtualBox dan Ubuntu ter-install dengan benar. 2. VM dapat dijalankan dan diakses. 3. Sistem Ubuntu ter-update dan siap digunakan. | 2.5 |
| **2** | Mampu menguasai operasi dasar Linux command line dan menginstal Java Development Kit. | Linux Fundamentals & Java Setup: Terminal Linux, Navigation (cd, ls, pwd), File operations (cp, mv, rm, mkdir), Permissions (chmod, chown), Text editors (nano/vim), Package management (apt), Instalasi OpenJDK, Environment variables (JAVA_HOME, PATH). | Praktikum, Latihan Terbimbing | Mahasiswa mempraktikkan command-line Linux, mengelola file dan direktori, mengatur permissions, dan menginstal serta mengonfigurasi Java JDK untuk Big Data tools. | Kemampuan operasi Linux dan konfigurasi Java. | 1. Mampu navigasi dan manipulasi file via terminal. 2. Java JDK ter-install (java -version). 3. JAVA_HOME terkonfigurasi dengan benar. | 2.5 |
| **3** | Mampu menginstal dan mengonfigurasi Hadoop Single Node Cluster di Ubuntu. | Instalasi Hadoop: Download Hadoop 3.x, Ekstraksi dan setup direktori, Konfigurasi SSH passwordless, Edit file core-site.xml, hdfs-site.xml, mapred-site.xml, yarn-site.xml, Format NameNode, Start Hadoop daemons (start-dfs.sh, start-yarn.sh). | Praktikum, Demonstrasi | Mahasiswa mengunduh Hadoop, melakukan konfigurasi file XML untuk single node, setup SSH, memformat HDFS, dan menjalankan Hadoop services. | Keberhasilan instalasi dan operasi Hadoop. | 1. Hadoop services berjalan (jps menampilkan NameNode, DataNode, ResourceManager, NodeManager). 2. Web UI Hadoop dapat diakses (localhost:9870). 3. HDFS ter-format tanpa error. | 2.5 |
| **4** | Mampu melakukan operasi HDFS dan memahami arsitektur distributed file system. | HDFS Operations & Architecture: Konsep Block, Replication, NameNode, DataNode, Command hdfs dfs (-ls, -mkdir, -put, -get, -cat, -rm, -cp, -mv, -tail), Monitoring HDFS via Web UI, Safe mode, fsck untuk health check. | Praktikum, Latihan Terbimbing | Mahasiswa mempraktikkan upload/download file ke HDFS, membuat struktur direktori, monitoring storage usage, dan memahami konsep replikasi data. | Ketepatan operasi HDFS dan pemahaman arsitektur. | 1. Mampu upload/download file ke/dari HDFS. 2. Memahami konsep block dan replication. 3. Dapat monitoring HDFS via command line dan Web UI. | 2.5 |
| **5** | Mampu memahami paradigma MapReduce dan mengimplementasikan program MapReduce dengan Java. | MapReduce Programming: Konsep Map phase dan Reduce phase, WordCount example, Implementasi Mapper class, Reducer class, Driver program, Kompilasi Java code, Packaging ke JAR file, Submit job ke Hadoop, Monitoring job execution. | Praktikum, Studi Kasus | Mahasiswa menulis kode Java untuk MapReduce (Mapper, Reducer, Driver), mengompilasi menjadi JAR file, menjalankannya di Hadoop cluster, dan monitoring eksekusi job. | Fungsionalitas program MapReduce. | 1. Program MapReduce ter-compile tanpa error. 2. Job berhasil disubmit dan dieksekusi. 3. Output hasil reduce tersimpan di HDFS dengan benar. | 2.5 |
| **6** | Mampu menginstal Apache Hive dan melakukan query data warehouse dengan HiveQL. | Apache Hive Setup & Querying: Instalasi Hive, Konfigurasi Metastore (Derby/MySQL), hive-site.xml configuration, Start HiveServer2, Akses via Beeline, CREATE DATABASE, CREATE TABLE (managed/external), LOAD DATA, Partitioning, Bucketing. | Praktikum, Demonstrasi | Mahasiswa menginstal Hive di Ubuntu, mengonfigurasi metastore, menjalankan HiveServer2, dan mengakses Hive melalui Beeline untuk membuat database dan tabel. | Keberhasilan setup Hive dan eksekusi query. | 1. Hive services berjalan tanpa error. 2. Dapat connect ke Hive via Beeline. 3. Database dan tabel berhasil dibuat. | 2.5 |
| **7** | Mampu melakukan analisis data dengan HiveQL (SELECT, JOIN, aggregation) dan optimasi query. | Advanced HiveQL: SELECT statements, WHERE filtering, JOIN operations (INNER, LEFT, RIGHT), GROUP BY & aggregations, HAVING clause, Subqueries, Query optimization techniques, Explain plan, Partition pruning. | Praktikum, Latihan Terbimbing | Mahasiswa memuat dataset besar ke Hive, melakukan query kompleks dengan JOIN dan aggregation, dan mengoptimasi query menggunakan partitioning. | Ketepatan query dan hasil analisis. | 1. Data ter-load ke tabel Hive. 2. Query JOIN dan aggregation berjalan dengan benar. 3. Mampu menggunakan partitioning untuk optimasi. | 2.5 |
| **8** | Mampu menginstal Apache Spark dan memahami arsitektur serta komponen Spark. | Apache Spark Installation & Architecture: Download Spark 3.x, Ekstraksi dan setup, Konfigurasi environment variables (SPARK_HOME), Spark architecture (Driver, Executors, Cluster Manager), Spark Submit, Spark Shell (spark-shell, pyspark), Web UI (localhost:4040). | Praktikum, Demonstrasi | Mahasiswa menginstal Spark di Ubuntu, mengonfigurasi environment variables, menjalankan Spark shell, dan memahami arsitektur komponen Spark. | Keberhasilan instalasi dan pemahaman Spark. | 1. Spark ter-install dan dapat dijalankan. 2. Spark shell (pyspark) dapat diakses. 3. Mampu menjelaskan peran Driver dan Executor. | 2.5 |
| **9** | Mampu memprogram dengan Spark RDD (Resilient Distributed Dataset) dan operasi transformasi-action. | Spark RDD Programming: Konsep RDD (immutable, distributed), Cara membuat RDD (parallelize, textFile), Transformations (map, filter, flatMap, reduceByKey, groupByKey), Actions (collect, count, take, reduce, saveAsTextFile), Lazy evaluation. | Praktikum, Latihan Terbimbing | Mahasiswa membuat RDD dari file dan collection, melakukan transformasi data dengan map/filter, dan mengeksekusi action untuk mendapatkan hasil. | Kemampuan pemrograman RDD. | 1. RDD berhasil dibuat dari berbagai sumber. 2. Transformasi (map, filter) berjalan dengan benar. 3. Action menghasilkan output yang sesuai. | 2.5 |
| **10** | Mampu memproses data terstruktur dengan Spark DataFrame dan Spark SQL. | Spark DataFrame & SQL: Membuat DataFrame, Schema definition, read.csv/json/parquet, DataFrame operations (select, filter, where, groupBy, agg, orderBy), Spark SQL queries, createOrReplaceTempView, Join operations, Window functions. | Praktikum, Studi Kasus | Mahasiswa membaca data dari berbagai format file, membuat DataFrame, melakukan operasi DataFrame, dan menjalankan SQL query di Spark. | Kemampuan manipulasi data dengan DataFrame. | 1. DataFrame berhasil dibuat dari CSV/JSON. 2. Operasi DataFrame berjalan sesuai ekspektasi. 3. SQL query di Spark menghasilkan output yang benar. | 2.5 |
| **11** | Mampu melakukan data cleaning, transformation, dan preprocessing dengan PySpark. | Data Engineering with PySpark: Handling missing values (dropna, fillna), Data type casting, String manipulation (split, concat, regexp), Date/time processing, Duplicate removal, Feature engineering, User-Defined Functions (UDF), Data validation. | Praktikum, Latihan Terbimbing | Mahasiswa membersihkan dataset (handling null, duplikasi), melakukan transformasi tipe data, feature engineering, dan validasi data menggunakan PySpark. | Kualitas hasil data preprocessing. | 1. Missing values ter-handle dengan strategi yang tepat. 2. Data types terkonversi dengan benar. 3. Fitur baru berhasil dibuat dan data tervalidasi. | 2.5 |
| **12** | Mampu menginstal Apache Kafka dan memahami konsep message streaming. | Apache Kafka Setup & Concepts: Instalasi Kafka dan Zookeeper, Kafka architecture (Broker, Producer, Consumer, Topic, Partition), Start Zookeeper dan Kafka server, Membuat topic, Mengirim message dengan console producer, Membaca message dengan console consumer, Consumer groups. | Praktikum, Demonstrasi | Mahasiswa menginstal Kafka dan Zookeeper di Ubuntu, membuat topic, mengirim dan menerima message melalui command line producer/consumer. | Keberhasilan setup dan operasi Kafka. | 1. Kafka dan Zookeeper services berjalan. 2. Topic berhasil dibuat. 3. Message dapat dikirim dan diterima secara real-time. | 2.5 |
| **13** | Mampu mengintegrasikan Spark Structured Streaming dengan Kafka untuk real-time data processing. | Spark Structured Streaming: Konsep streaming, Membaca stream dari Kafka dengan PySpark, Streaming transformations, Windowing operations (tumbling, sliding), Watermarking, Output modes (append, complete, update), Write stream ke console/file/database, Checkpoint. | Praktikum, Studi Kasus | Mahasiswa membuat aplikasi Spark Streaming yang subscribe ke Kafka topic, melakukan agregasi real-time dengan windowing, dan menyimpan hasil streaming. | Fungsionalitas streaming pipeline. | 1. Spark Streaming terhubung ke Kafka topic. 2. Data stream ter-proses dengan transformasi yang benar. 3. Output streaming tersimpan sesuai requirement. | 2.5 |
| **14** | Mampu melakukan visualisasi dan exploratory data analysis dengan Jupyter Notebook dan Python libraries. | Data Visualization & EDA: Setup Jupyter Notebook di Ubuntu, Instalasi libraries (pandas, matplotlib, seaborn, plotly), Integrasi PySpark dengan Jupyter, Membaca data dari HDFS/Spark, Eksplorasi statistik deskriptif, Visualisasi (line plot, bar chart, histogram, scatter plot, heatmap), Dashboard sederhana. | Praktikum, Latihan Terbimbing | Mahasiswa setup Jupyter Notebook, connect ke Spark, melakukan exploratory data analysis, dan membuat visualisasi data dari Big Data processing results. | Kualitas analisis dan visualisasi. | 1. Jupyter Notebook terintegrasi dengan PySpark. 2. Visualisasi informatif dan mudah dipahami. 3. Insight dari data dijelaskan dengan baik. | 2.5 |
| **15** | Mampu mengoptimasi performa Spark application dan melakukan troubleshooting. | Spark Performance Tuning: Spark configuration tuning (executor memory, cores, partitions), Memory management (storage vs execution), Partition optimization (repartition, coalesce), Broadcast variables, Accumulators, Caching/Persisting, Monitoring dengan Spark UI (Stages, Tasks, Storage, Executors), Debugging common errors, Best practices. | Praktikum, Studi Kasus | Mahasiswa melakukan tuning konfigurasi Spark, menganalisis Spark UI untuk identifikasi bottleneck, mengoptimasi partitioning, dan troubleshooting performance issues. | Kemampuan optimasi dan problem solving. | 1. Mampu menganalisis Spark UI untuk bottleneck. 2. Konfigurasi Spark ter-optimasi untuk use case. 3. Performance aplikasi meningkat setelah tuning. | 2.5 |
| **16** | Mampu mempresentasikan dan mendemonstrasikan proyek akhir Big Data end-to-end pipeline. | **Proyek Akhir**: End-to-end Big Data pipeline dengan use case nyata (misal: analisis log, sentiment analysis, recommendation system). Pipeline mencakup: data ingestion (HDFS/Kafka), processing (Spark/Hive), storage, analysis, dan visualization. Presentasi & Demo hasil implementasi dengan dokumentasi lengkap. | Presentasi & Demo Proyek | Mahasiswa mendemonstrasikan sistem Big Data yang telah dibangun di Ubuntu VM, menjelaskan arsitektur sistem, proses ETL, analisis data, insight yang dihasilkan, dan tantangan yang dihadapi beserta solusinya. | Kelengkapan, fungsionalitas, dan kualitas proyek. | 1. Pipeline berjalan end-to-end dari ingestion hingga visualization. 2. Analisis menghasilkan insight yang valuable. 3. Presentasi teknis jelas dan komprehensif. 4. Dokumentasi proyek lengkap (README, setup guide, code comments). | 40 |

---

## REFERENSI

1. White, T. (2015). *Hadoop: The Definitive Guide*, 4th Edition. O'Reilly Media.
2. Karau, H., Konwinski, A., Wendell, P., & Zaharia, M. (2015). *Learning Spark: Lightning-Fast Big Data Analysis*. O'Reilly Media.
3. Chambers, B., & Zaharia, M. (2018). *Spark: The Definitive Guide*. O'Reilly Media.
4. Narkhede, N., Shapira, G., & Palino, T. (2017). *Kafka: The Definitive Guide*. O'Reilly Media.
5. Dokumentasi resmi Apache Hadoop: https://hadoop.apache.org/docs/
6. Dokumentasi resmi Apache Spark: https://spark.apache.org/docs/latest/
7. Dokumentasi resmi Apache Hive: https://hive.apache.org/
8. Dokumentasi resmi Apache Kafka: https://kafka.apache.org/documentation/
9. Ubuntu Server Guide: https://ubuntu.com/server/docs
10. VirtualBox User Manual: https://www.virtualbox.org/manual/

---


## SPESIFIKASI MINIMUM SISTEM

### Host Machine (Windows):
- **Processor**: Intel Core i5/AMD Ryzen 5 atau lebih tinggi
- **RAM**: Minimum 8 GB (Recommended 16 GB)
- **Storage**: Minimum 50 GB free space (SSD recommended)
- **Software**: VirtualBox 7.x atau VMware Workstation Player

### Virtual Machine (Ubuntu):
- **OS**: Ubuntu 22.04 LTS atau 24.04 LTS Desktop
- **RAM Allocation**: 4-8 GB
- **Storage**: 30-40 GB (dynamically allocated)
- **CPU Cores**: 2-4 cores
- **Network**: NAT atau Bridged Adapter

---


Pada hari Sabtu 08 November 2025 telah dilakukan penyusunan Rencana Pembelajaran Semester (RPS) dan Deskripsi Tugas untuk mata kuliah Praktikum Pengantar Big Data.

**Dasar Pertimbangan penyusunan RPS adalah:**
1. Perubahan Kurikulum
2. Penyesuaian materi dengan topik-topik terkini dan kebutuhan industri Big Data
3. Implementasi Big Data tools pada Ubuntu Linux melalui Virtual Machine sesuai praktik industri
4. Pengembangan kompetensi praktis dalam ekosistem Big Data yang banyak digunakan di dunia profesional

Bandung, November 2025

**Tim Penyusun:**

| Nama Penyusun | Jabatan | Tanda Tangan |
|------------|---------|--------------|
| [Adam Setiadi], [S.Kom] | Pemateri | |


Bandung, November 2025
