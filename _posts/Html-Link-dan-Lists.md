<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>📝HTML Link dan Lists</title>
    <link rel="stylesheet" href="/assets/css/styles.css">
</head>
<body>
    <nav>
    
    <a href="/" >Home</a>
    
    <a href="/friends.html" >Friends</a>
    
    <a href="/blog.html" >Blog</a>
    
</nav>

    <h1>📝HTML Link dan Lists></page></h1>
<p>20 Mar 2025 - </p>

<hr />

<p><img src="/assets/image/html.png" alt="html link dan list" /></p>

<p>Dalam <strong>HTML</strong> (<em>HyperText Markup Language</em>), <strong>link</strong> dan <strong>lists</strong> adalah elemen dasar yang sangat penting dalam membangun struktur dan navigasi halaman web. Berikut adalah penjelasan lengkap mengenai kedua elemen ini:</p>

<hr />

<h2 id="1-link-tautan-pada-html"><strong>1. Link (Tautan) pada HTML</strong></h2>
<p>Link atau tautan dalam HTML digunakan untuk menghubungkan satu halaman ke halaman lainnya atau ke sumber eksternal seperti file, gambar, atau dokumen. Link juga dapat digunakan untuk menavigasi ke bagian tertentu dalam satu halaman web.</p>

<h3 id="a-sintaks-dasar-link"><strong>A. Sintaks Dasar Link</strong></h3>
<p>Tag yang digunakan untuk membuat link adalah <code class="language-plaintext highlighter-rouge">&lt;a&gt;</code> (<strong>anchor</strong>).</p>

<div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="nt">&lt;a</span> <span class="na">href=</span><span class="s">"#"</span><span class="nt">&gt;</span>Teks atau elemen yang bisa diklik<span class="nt">&lt;/a&gt;</span>
</code></pre></div></div>

<h3 id="b-atribut-pada-tag-a"><strong>B. Atribut pada Tag <code class="language-plaintext highlighter-rouge">&lt;a&gt;</code></strong></h3>
<p>Berikut adalah atribut-atribut yang sering digunakan pada elemen <code class="language-plaintext highlighter-rouge">&lt;a&gt;</code>:</p>

<ul>
  <li><strong><code class="language-plaintext highlighter-rouge">href</code></strong> – Menentukan URL tujuan link.<br />
  <strong>Contoh:</strong>
    <div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code>  <span class="nt">&lt;a</span> <span class="na">href=</span><span class="s">"https://www.example.com"</span><span class="nt">&gt;</span>Kunjungi Example<span class="nt">&lt;/a&gt;</span>
</code></pre></div>    </div>
  </li>
  <li><strong><code class="language-plaintext highlighter-rouge">target</code></strong> – Menentukan bagaimana link dibuka.<br />
  Nilai yang tersedia:
    <ul>
      <li><code class="language-plaintext highlighter-rouge">_self</code> – Membuka link di tab/jendela saat ini (default).</li>
      <li><code class="language-plaintext highlighter-rouge">_blank</code> – Membuka link di tab/jendela baru.</li>
      <li><code class="language-plaintext highlighter-rouge">_parent</code> – Membuka link di jendela induk (jika ada).</li>
      <li><code class="language-plaintext highlighter-rouge">_top</code> – Membuka link di jendela penuh (keluar dari frame).</li>
    </ul>

    <p><strong>Contoh:</strong></p>
    <div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code>  <span class="nt">&lt;a</span> <span class="na">href=</span><span class="s">"https://www.example.com"</span> <span class="na">target=</span><span class="s">"_blank"</span><span class="nt">&gt;</span>Buka di Tab Baru<span class="nt">&lt;/a&gt;</span>
</code></pre></div>    </div>
  </li>
  <li><strong><code class="language-plaintext highlighter-rouge">title</code></strong> – Menampilkan keterangan saat kursor diarahkan ke link.<br />
  <strong>Contoh:</strong>
    <div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code>  <span class="nt">&lt;a</span> <span class="na">href=</span><span class="s">"#"</span> <span class="na">title=</span><span class="s">"Keterangan"</span><span class="nt">&gt;</span>Link dengan Keterangan<span class="nt">&lt;/a&gt;</span>
</code></pre></div>    </div>
  </li>
  <li><strong><code class="language-plaintext highlighter-rouge">rel</code></strong> – Menentukan hubungan antara dokumen dengan link tujuan.<br />
  Nilai yang umum digunakan:
    <ul>
      <li><code class="language-plaintext highlighter-rouge">nofollow</code> – Memberitahu mesin pencari untuk tidak mengikuti link ini.</li>
      <li><code class="language-plaintext highlighter-rouge">noopener</code> – Mencegah halaman baru mengakses <code class="language-plaintext highlighter-rouge">window.opener</code>.</li>
      <li><code class="language-plaintext highlighter-rouge">noreferrer</code> – Mencegah pengiriman informasi referensi ke halaman tujuan.</li>
    </ul>

    <p><strong>Contoh:</strong></p>
    <div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code>  <span class="nt">&lt;a</span> <span class="na">href=</span><span class="s">"https://www.example.com"</span> <span class="na">target=</span><span class="s">"_blank"</span> <span class="na">rel=</span><span class="s">"nofollow noopener noreferrer"</span><span class="nt">&gt;</span>Kunjungi Example dengan Aman<span class="nt">&lt;/a&gt;</span>
</code></pre></div>    </div>
  </li>
  <li><strong><code class="language-plaintext highlighter-rouge">download</code></strong> – Menginstruksikan browser untuk mengunduh file daripada membukanya.<br />
  <strong>Contoh:</strong>
    <div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code>  <span class="nt">&lt;a</span> <span class="na">href=</span><span class="s">"file.pdf"</span> <span class="na">download</span><span class="nt">&gt;</span>Unduh File PDF<span class="nt">&lt;/a&gt;</span>
</code></pre></div>    </div>
  </li>
</ul>

<hr />

<h2 id="2-lists-daftar-pada-html"><strong>2. Lists (Daftar) pada HTML</strong></h2>
<p>Lists digunakan untuk menyusun konten secara terstruktur dalam format daftar. HTML menyediakan tiga jenis utama daftar:</p>

<h3 id="a-ordered-list-ol"><strong>A. Ordered List (<code class="language-plaintext highlighter-rouge">&lt;ol&gt;</code>)</strong></h3>
<p><code class="language-plaintext highlighter-rouge">Ordered List</code> digunakan untuk membuat daftar terurut (menggunakan angka, huruf, atau simbol).</p>

<h4 id="sintaks-dasar"><strong>Sintaks Dasar:</strong></h4>
<div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="nt">&lt;ol&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 1<span class="nt">&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 2<span class="nt">&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 3<span class="nt">&lt;/li&gt;</span>
<span class="nt">&lt;/ol&gt;</span>
</code></pre></div></div>

<h4 id="atribut-pada-ol"><strong>Atribut pada <code class="language-plaintext highlighter-rouge">&lt;ol&gt;</code></strong></h4>
<ul>
  <li><strong><code class="language-plaintext highlighter-rouge">type</code></strong> – Menentukan tipe penomoran dalam daftar.<br />
  Nilai yang tersedia:
    <ul>
      <li><code class="language-plaintext highlighter-rouge">"1"</code> → Angka (default)</li>
      <li><code class="language-plaintext highlighter-rouge">"A"</code> → Huruf kapital</li>
      <li><code class="language-plaintext highlighter-rouge">"a"</code> → Huruf kecil</li>
      <li><code class="language-plaintext highlighter-rouge">"I"</code> → Angka romawi kapital</li>
      <li><code class="language-plaintext highlighter-rouge">"i"</code> → Angka romawi kecil</li>
    </ul>
  </li>
  <li>
    <p><strong><code class="language-plaintext highlighter-rouge">start</code></strong> – Menentukan nomor awal dari daftar.</p>
  </li>
  <li><strong><code class="language-plaintext highlighter-rouge">reversed</code></strong> – Menampilkan daftar dalam urutan terbalik.</li>
</ul>

<h4 id="contoh-dengan-atribut"><strong>Contoh dengan Atribut:</strong></h4>
<div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="nt">&lt;ol</span> <span class="na">type=</span><span class="s">"A"</span> <span class="na">start=</span><span class="s">"5"</span> <span class="na">reversed</span><span class="nt">&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 5<span class="nt">&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 4<span class="nt">&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 3<span class="nt">&lt;/li&gt;</span>
<span class="nt">&lt;/ol&gt;</span>
</code></pre></div></div>

<hr />

<h3 id="b-unordered-list-ul"><strong>B. Unordered List (<code class="language-plaintext highlighter-rouge">&lt;ul&gt;</code>)</strong></h3>
<p><code class="language-plaintext highlighter-rouge">Unordered List</code> digunakan untuk membuat daftar tidak terurut (menggunakan simbol seperti lingkaran, kotak, atau titik).</p>

<h4 id="sintaks-dasar-1"><strong>Sintaks Dasar:</strong></h4>
<div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="nt">&lt;ul&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 1<span class="nt">&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 2<span class="nt">&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;</span>Item 3<span class="nt">&lt;/li&gt;</span>
<span class="nt">&lt;/ul&gt;</span>
</code></pre></div></div>

<h4 id="atribut-pada-ul"><strong>Atribut pada <code class="language-plaintext highlighter-rouge">&lt;ul&gt;</code></strong></h4>
<ul>
  <li><strong><code class="language-plaintext highlighter-rouge">type</code></strong> – Menentukan simbol untuk setiap item dalam daftar.<br />
  Nilai yang tersedia:
    <ul>
      <li><code class="language-plaintext highlighter-rouge">"disc"</code> → Lingkaran hitam (default)</li>
      <li><code class="language-plaintext highlighter-rouge">"circle"</code> → Lingkaran kosong</li>
      <li><code class="language-plaintext highlighter-rouge">"square"</code> → Kotak hitam</li>
    </ul>
  </li>
</ul>

<h4 id="contoh-dengan-atribut-1"><strong>Contoh dengan Atribut:</strong></h4>
<div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="nt">&lt;ul</span> <span class="na">type=</span><span class="s">"circle"</span><span class="nt">&gt;</span>
    <span class="nt">&lt;li&gt;</span>Apel<span class="nt">&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;</span>Pisang<span class="nt">&lt;/li&gt;</span>
<span class="nt">&lt;/ul&gt;</span>
</code></pre></div></div>

<hr />

<h2 id="3-gabungan-link-dan-list"><strong>3. Gabungan Link dan List</strong></h2>
<p>Berikut adalah contoh penggunaan <strong>link</strong> di dalam <strong>list</strong> untuk menautkan ke sumber daya terkait:</p>

<h4 id="contoh"><strong>Contoh:</strong></h4>
<div class="language-html highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="nt">&lt;h2&gt;</span>Daftar Teknologi Web<span class="nt">&lt;/h2&gt;</span>
<span class="nt">&lt;ol&gt;</span>
    <span class="nt">&lt;li&gt;&lt;a</span> <span class="na">href=</span><span class="s">"https://developer.mozilla.org/en-US/docs/Web/HTML"</span><span class="nt">&gt;</span>HTML<span class="nt">&lt;/a&gt;&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;&lt;a</span> <span class="na">href=</span><span class="s">"https://developer.mozilla.org/en-US/docs/Web/CSS"</span><span class="nt">&gt;</span>CSS<span class="nt">&lt;/a&gt;&lt;/li&gt;</span>
    <span class="nt">&lt;li&gt;&lt;a</span> <span class="na">href=</span><span class="s">"https://developer.mozilla.org/en-US/docs/Web/JavaScript"</span><span class="nt">&gt;</span>JavaScript<span class="nt">&lt;/a&gt;&lt;/li&gt;</span>
<span class="nt">&lt;/ol&gt;</span>
</code></pre></div></div>

<hr />

<h2 id="kesimpulan"><strong>Kesimpulan</strong></h2>
<ul>
  <li><strong>Link (<code class="language-plaintext highlighter-rouge">&lt;a&gt;</code>)</strong> digunakan untuk navigasi antar halaman atau sumber daya.</li>
  <li><strong>Ordered List (<code class="language-plaintext highlighter-rouge">&lt;ol&gt;</code>)</strong> digunakan untuk membuat daftar terurut (menggunakan angka, huruf, atau simbol).</li>
  <li><strong>Unordered List (<code class="language-plaintext highlighter-rouge">&lt;ul&gt;</code>)</strong> digunakan untuk membuat daftar tidak terurut (menggunakan bullet).</li>
</ul>

<p>Dengan memahami elemen <strong>link</strong> dan <strong>lists</strong>, Anda dapat membuat halaman web yang lebih terstruktur dan mudah dinavigasi.</p>



</body>
</html>