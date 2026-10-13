### tugas B

## objektif

# membangun prototipe awal sistem yang jawaban FAQ yng relevan thdp pertanyaan user, dengan semantic search, lalu llm memberikan respons jawban natural

## sumber dan struktur data

# mengubah entri FAQ jadi embedding lalu simpan ke vector database FAISS

## batasan dan asumsi

# kalo ada jawaban faq pake faq, kalo ada diluar jawab langsung kecuali pertanyaan masih seputar produk/jasa maka sbnrnya harus kembalikan kendali ke manusia(belum utk tugas kali ini)


### tugas j analisis relevansi

## uji query
# ada di faq - jawaban aman(2 nomor atas)
# parafrase kata - jawaban mirip 1 dan 2 karena emg parafrase dr kedua soal itu(no 3 dan 4)
# luar soal - diarahkan tny org real
# kesimpulan semantic bekerja dengan baaik

## deskripsi proyek
# proyek ini menggunakan sistem semantic search dan integrasi LLM utk toko e commrce dengan data faq di file ecommerce_faq_knowledge_base.csv

## alur sistem
# ingest -- pake pandas read ecommerce_faq_knowledge_base,csv lalu ngelist masing" faq
# embed -- embed masing" list faq pake gen ai dengan gemini-embedding-2
# store -- store ke faiss
# retrieve -- agar bisa nemukan pertanyaan yang mirip dari query yang ada
# generate -- dengan gemini kasih response

## keterbatasan
# harus di prompt agar ga kemana"
# jawaban terbatas dr faq aja
# api gemini ga selalu works

## cara pakai
# saya ga isi requirements.txt, kurang paham cara pakainya