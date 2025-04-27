---
layout: default
title: "Daftar Mahasiswa Aktif"
permalink: /skripsi/mahasiswa/
---

# Mahasiswa Aktif – Semester Genap 2024/2025

| NIM     | Nama Mahasiswa     | Judul Skripsi                     | Aksi                |
|---------|--------------------|-----------------------------------|---------------------|
{% for mhs in site.data.mahasiswa %}
  {% unless mhs.status == "Selesai" %}
| {{ mhs.nim }} | {{ mhs.nama }} | {{ mhs.judul | strip_html | truncate: 50 }} | [Lihat Catatan]({{ site.baseurl }}/skripsi/mahasiswa/{{ mhs.nim }}/) |
  {% endunless %}
{% endfor %}
