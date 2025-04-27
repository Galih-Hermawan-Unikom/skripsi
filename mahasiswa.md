---
layout: default
title: "Daftar Mahasiswa Aktif"
permalink: /skripsi/mahasiswa/
---

# Mahasiswa Aktif – Semester Genap 2024/2025

Halaman ini menampilkan semua mahasiswa yang **belum selesai** (status bukan “Selesai”) dalam bimbingan skripsi.

| NIM     | Nama Mahasiswa     | Judul Skripsi Singkat         | Status     | Semester Mulai        | Jumlah Sesi | Tanggal Sesi Terakhir | Aksi                       |
|---------|--------------------|-------------------------------|------------|-----------------------|-------------|-----------------------|----------------------------|
{% for mhs in site.data.mahasiswa %}
  {% unless mhs.status == "Selesai" %}
| {{ mhs.nim }} | {{ mhs.nama }} | {{ mhs.judul }} | {{ mhs.status }} | {{ mhs.semester_mulai }} | {{ mhs.jumlah_sesi }} | {{ mhs.tanggal_sesi_terakhir }} | [Detail](/skripsi/mahasiswa/{{ mhs.nim }}/) |
  {% endunless %}
{% endfor %}
