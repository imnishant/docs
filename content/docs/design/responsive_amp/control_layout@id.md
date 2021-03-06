---
$title: Tata letak & kueri media
---
[TOC]


AMP mendukung **kueri media** &amp; **kueri elemen**, juga disertai cara bawaan yang canggih untuk mengontrol **tata letak** masing-masing elemen. Atribut `layout` mempermudah pembuatan desain yang sepenuhnya responsif dibandingkan jika Anda hanya menggunakan CSS.

## Membuat gambar responsif dengan mudah

Buat gambar responsif dengan menetapkan atribut `width` dan `height`, menyetel tata letak ke `responsive`,
dan menunjukkan dengan [`srcset`](/id/docs/guides/responsive/art_direction.html)
aset gambar mana yang akan digunakan berdasarkan ukuran layar yang berbeda-beda:

[sourcecode:html]
<amp-img
    src="/img/narrow.jpg"
    srcset="/img/wide.jpg 640w,
           /img/narrow.jpg 320w"
    width="1698"
    height="2911"
    layout="responsive"
    alt="an image">
</amp-img>
[/sourcecode]

Elemen `amp-img` ini melakukan penyesuaian otomatis dengan lebar
elemen penampungnya,
dan tingginya otomatis ditetapkan sesuai rasio tinggi lebar
yang ditetapkan oleh atribut width dan height yang ditentukan. Cobalah dengan mengubah ukuran jendela browser ini:

<amp-img src="/static/img/background.jpg" width="1920" height="1080" layout="responsive"></amp-img>

{% call callout('Tips', type='success') %}
Lihat demo langsung berdampingan tentang `amp-img`: [Demo Langsung AMP by Example](https://ampbyexample.com/components/amp-img/).
{% endcall %}

## Atribut layout

Atribut `layout` memberi Anda kontrol per-elemen yang mudah terkait
rendering elemen di layar. Banyak dari hal ini dapat dilakukan dengan CSS murni – tapi
prosesnya jauh lebih sulit, dan membutuhkan banyak modifikasi. Sebagai gantinya, gunakan atribut `layout`.

### Nilai yang didukung untuk atribut `layout`

Nilai berikut dapat digunakan untuk atribut `layout`:

<table>
  <thead>
    <tr>
      <th data-th="Layout type" class="col-thirty">Jenis tata letak</th>
      <th data-th="Width/height required" class="col-twenty">Lebar/<br>tinggi diperlukan</th>
      <th data-th="Behavior">Perilaku</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td data-th="Layout type"><code>nodisplay</code></td>
      <td data-th="Description">Tidak</td>
      <td data-th="Behavior">Elemen tidak ditampilkan. Tata letak ini dapat diterapkan ke setiap elemen AMP. Komponen tersebut tidak menggunakan ruang sama sekali di layar karena tidak memiliki gaya tampilan. Diasumsikan bahwa elemen ini dapat tampil dengan sendirinya di tindakan pengguna, misalnya, <a href="/id/docs/reference/components/amp-lightbox.html"><code>amp-lightbox</code></a>.</td>
    </tr>
    <tr>
      <td data-th="Layout type"><code>fixed</code></td>
      <td data-th="Description">Ya</td>
      <td data-th="Behavior">Elemen memiliki lebar dan tinggi yang tetap tetapi tidak mendukung responsivitas. Satu-satunya pengecualian adalah elemen <a href="/id/docs/reference/components/amp-pixel.html"><code>amp-pixel</code></a> dan <a href="/id/docs/reference/components/amp-audio.html"><code>amp-audio</code></a>.</td>
    </tr>
    <tr>
      <td data-th="Layout type"><code>responsive</code></td>
      <td data-th="Description">Ya</td>
      <td data-th="Behavior">Elemen disesuaikan dengan lebar elemen penampungnya dan tingginya otomatis diubah sesuai rasio tinggi lebar yang ditentukan oleh atribut width dan height. Tata letak ini berfungsi sangat baik untuk sebagian besar elemen AMP, termasuk <a href="/id/docs/reference/components/amp-img.html"><code>amp-img</code></a> dan <a href="/id/docs/reference/components/amp-video.html"><code>amp-video</code></a>. Ruang yang tersedia bergantung pada elemen induk dan juga dapat disesuaikan menggunakan CSS <code>max-width</code>.<p><strong>Catatan</strong>: Elemen dengan <code>"layout=responsive"</code> tidak memiliki ukuran intrinsik. Ukuran elemen ini ditentukan dari elemen penampungnya. Untuk memastikan elemen AMP Anda ditampilkan, Anda harus menetapkan lebar dan tinggi untuk elemen penampungnya. Jangan tetapkan <code>"display:table"</code> pada elemen penampung karena ini akan menggantikan tampilan elemen AMP, yang membuat elemen AMP menjadi tidak terlihat.</p></td>
    </tr>
    <tr>
      <td data-th="Layout type"><code>fixed-height</code></td>
      <td data-th="Description">Hanya tinggi</td>
      <td data-th="Behavior">Elemen menempati ruang yang disediakan, tapi tingginya tidak diubah. Tata letak ini berfungsi dengan baik untuk elemen seperti <a href="/id/docs/reference/components/amp-carousel.html"><code>amp-carousel</code></a> yang menggunakan konten yang diposisikan secara horizontal. Atribut <code>width</code> harus tidak ada atau sama dengan <code>auto</code>.</td>
    </tr>
    <tr>
      <td data-th="Layout type"><code>fill</code></td>
      <td data-th="Description">Tidak</td>
      <td data-th="Behavior">Elemen menempati ruang yang disediakan, baik untuk tinggi maupun lebarnya. Dengan kata lain, tata letak elemen fill (isian) sesuai dengan induknya. Agar elemen mengisi penampung induknya, pastikan penampung induk menetapkan `position:relative` atau `position:absolute`.</td>
    </tr>
    <tr>
      <td data-th="Layout type"><code>container</code></td>
      <td data-th="Description">Tidak</td>
      <td data-th="Behavior">Elemen memungkinkan turunannya menentukan ukurannya, sama seperti <code>div</code> HTML biasa. Komponen diasumsikan tidak memiliki tata letak spesifik, melainkan hanya berfungsi sebagai penampung. Turunannya dirender dengan seketika.</td>
    </tr>
    <tr>
      <td data-th="Layout type"><code>flex-item</code></td>
      <td data-th="Description">Tidak</td>
      <td data-th="Behavior">Elemen dan elemen lain dalam induknya menempati ruang yang tersisa di penampung induk jika induk tersebut merupakan penampung fleksibel (artinya, <code>display:flex</code>). Ukuran elemen ditentukan oleh elemen induk dan jumlah elemen lain yang berada di dalam induk berdasarkan tata letak CSS <code>display:flex</code>.</td>
    </tr>
    <tr>
      <td data-th="Layout type"><code>intrinsic</code></td>
      <td data-th="Description">Ya</td>
      <td data-th="Behavior">Elemen ini menempati ruang yang disediakan untuknya dan ukuran tingginya otomatis diubah sesuai rasio tinggi lebar yang ditentukan oleh atribut <code>width</code> dan <code>height</code> <em>hingga</em> mencapai ukuran yang wajar untuk elemen itu atau mencapai batasan CSS (misalnya max-width). Atribut width dan height harus ada. Tata letak ini berfungsi sangat baik untuk sebagian besar elemen AMP, termasuk <code>amp-img</code>, <code>amp-carousel</code>, dll. Ruang yang tersedia bergantung pada elemen induk dan juga dapat disesuaikan menggunakan CSS <code>max-width</code>. Tata letak ini berbeda dengan <code>responsive</code> karena memiliki tinggi dan lebar intrinsik. Hal ini terlihat jelas pada elemen mengambang di mana tata letak <code>responsive</code> akan merender 0x0, sedangkan tata letak <code>intrinsic</code> akan menyusut ke ukuran yang lebih kecil dari ukuran wajarnya atau ke batas ukuran CSS. </td>
    </tr>
  </tbody>
</table>

{% call callout('Tips', type='success') %}
Kunjungi halaman [Mendemonstrasikan tata letak AMP](/id/docs/design/amp-html-layout/layouts_demonstrated.html) untuk melihat bagaimana berbagai tata letak merespons perubahan ukuran layar. Anda juga dapat menemukan lebih banyak informasi di [AMP By Example](https://ampbyexample.com/advanced/layout_system/).
{% endcall %}


### Bagaimana jika atribut width dan height tidak ditentukan?

Dalam beberapa kasus, jika `width` atau `height` tidak ditentukan,
AMP runtime dapat menetapkan nilai berikut sebagai default:

* [`amp-pixel`](/id/docs/reference/components/amp-pixel.html): Lebar dan tinggi ditetapkan secara default ke 0.
* [`amp-audio`](/id/docs/reference/components/amp-audio.html): Lebar dan tinggi default disimpulkan dari browser.

### Bagaimana jika atribut <code>layout</code> tidak ditentukan?

Jika atribut <code>layout</code> tidak ditentukan, AMP akan mencoba menyimpulkan atau menebak
nilai yang sesuai:

<table>
  <thead>
    <tr>
      <th data-th="Rule">Aturan</th>
      <th data-th="Inferred layout" class="col-thirty">Tata letak yang disimpulkan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td data-th="Rule">Atribut <code>height</code> ada tetapi atribut <code>width</code> tidak ada atau sama dengan <code>auto</code></td>
      <td data-th="Inferred layout"><code>fixed-height</code></td>
    </tr>
    <tr>
      <td data-th="Rule">Atribut <code>width</code> atau <code>height</code> ada beserta atribut <code>sizes</code></td>
      <td data-th="Inferred layout"><code>responsive</code></td>
    </tr>
    <tr>
      <td data-th="Rule">Atribut <code>width</code> atau <code>height</code> ada</td>
      <td data-th="Inferred layout"><code>fixed</code></td>
    </tr>
    <tr>
      <td data-th="Rule">Atribut <code>width</code> dan <code>height</code> tidak ada</td>
      <td data-th="Inferred layout"><code>container</code></td>
    </tr>
  </tbody>
</table>

## Menggunakan kueri media

### Kueri media CSS

Gunakan [`@media`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)
untuk mengontrol tampilan dan perilaku tata letak halaman, seperti yang akan Anda lakukan di situs lainnya.
Jika jendela browser berubah ukuran atau orientasi,
kueri media akan dievaluasi ulang dan elemen disembunyikan atau ditampilkan
berdasarkan hasil baru.

{% call callout('Baca selengkapnya', type='read') %}
Pelajari lebih lanjut cara mengontrol tata letak dengan menerapkan kueri media di [Menggunakan kueri media CSS untuk meningkatkan respons](https://developers.google.com/web/fundamentals/design-and-ui/responsive/fundamentals/use-media-queries?hl=id).
{% endcall %}

### Kueri media elemen

Salah satu fitur tambahan untuk desain responsif yang tersedia di AMP adalah atribut `media`.
Atribut ini dapat digunakan di setiap elemen AMP;
cara kerjanya mirip dengan kueri media di stylesheet global,
tapi hanya memengaruhi elemen tertentu pada satu halaman.

Misalnya, di sini terdapat 2 gambar dengan kueri media yang berdiri sendiri.

[sourcecode:html]
<amp-img
    media="(min-width: 650px)"
    src="wide.jpg"
    width=466
    height=355
    layout="responsive">
</amp-img>
[/sourcecode]

Tergantung lebar layarnya, salah satu gambar akan diambil dan dirender.

[sourcecode:html]
<amp-img
    media="(max-width: 649px)"
    src="narrow.jpg"
    width=527
    height=193
    layout="responsive">
</amp-img>
[/sourcecode]
 
