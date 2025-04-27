---
layout: default
title: "Daftar Mahasiswa Aktif"
permalink: /mahasiswa/
---

# Mahasiswa Aktif – Semester Genap 2024/2025

<table>
  <thead>
    <tr>
      <th>NIM</th>
      <th>Nama Mahasiswa</th>
      <th>Judul Skripsi</th>
      <th>Aksi</th>
    </tr>
  </thead>
  <tbody>
    {% for mhs in site.data.mahasiswa %}
      {% unless mhs.status == "Selesai" %}
    <tr>
      <td>{{ mhs.nim }}</td>
      <td>{{ mhs.nama }}</td>
      <td>{{ mhs.judul | strip_html | truncate: 50 }}</td>
      <td>
        <a class="button" href="{{ site.baseurl }}/mahasiswa/{{ mhs.nim }}/">
          Lihat Catatan
        </a>
      </td>
    </tr>
      {% endunless %}
    {% endfor %}
  </tbody>
</table>

