---
layout: post
title: instela'da paylaş butonu
fullview: true
author: çağatay gürtürk
---

 **instela** kullanıcıları için internet'in değişik yerlerinde gördükleri linkleri referans vererek başlıklar açmak  oldukça alışılmış bir harekettir. bugüne kadar instela'da toplam **50000**'i aşkın web sitesine ait link paylaşılmıştır ve her gün bunlara yenileri eklenmektedir. instela üzerinde yer alan linkler kullanılarak diğer sitelere aylık 5.000.000'un üzerinde ziyaret aktarılmakta ve paylaşım butonlarının yaygınlaşması ile birlikte bu rakamın yalnızca 6 ay içerisinde iki katına çıkması beklenmektedir.

eğer bir web sitesi sahibiyseniz, haber, video, fotoğraf gibi özgün içerikler oluşturuyorsanız sitenize **instela'da paylaş** butonu ekleyerek
<ul>
<li>instela kullanıcılarının yayınladığınız içeriğe ait bağlantıyı takipçileri ile paylaşması sayesinde sitenize trafik sağlayabilir</li>
<li>bu içeriklerin başlıklarla eşleştirilmesi halinde viral yayılım sağlama şansına erişebilirsiniz.</li>
</ul>
  
### kullanım

paylaşım butonunu yerleştirmek istediğiniz yere aşağıdaki kodu yapıştırın:

{% highlight html %}
<a href="https://tr.instela.com" class="instela-share">instela'da paylaş</a>
<script>!function(d, s, id) {var js, ijs = d.getElementsByTagName(s)[0], p = /^http:/.test(d.location) ? 'http' : 'https';if (!d.getElementById(id)) {js = d.createElement(s);js.id = id;js.src = p + '://widgets.instela.com/instela.js';ijs.parentNode.insertBefore(js, ijs);}}(document, 'script', 'instela-sjs');</script>
{% endhighlight %}
<br>

### buton tipleri

değişik tasarımlarda **4** adet paylaş butonu bulunmaktadır. buton tipleri ``a`` (anchor) etiketine verilecek ``data-type`` parametresiyle seçilebilir.

<table class="table table-bordered table-striped">
<colgroup>
        <col class="col-xs-1">
        <col class="col-xs-2">
</colgroup>
<tr>
<td>
<a href="https://tr.instela.com" class="instela-share" data-type="normal">instela'da paylaş</a>
</td>
<td>normal</td>
</tr>
<tr>
<td>
<a href="https://tr.instela.com" class="instela-share" data-type="small">instela'da paylaş</a>
</td>
<td>small</td>
</tr>
<tr>
<td>
<a href="https://tr.instela.com" class="instela-share" data-type="large">instela'da paylaş</a>
</td>
<td>large</td>
</tr>
<tr>
<td>
<a href="https://tr.instela.com" class="instela-share" data-type="square">instela'da paylaş</a>
</td>
<td>square</td>
</tr>
</table><br>

### özelleştirme

``<a>`` etiketi bazı parametreler alabilir

<div class="table-responsive">
<table class="table table-bordered table-striped">
<colgroup>
        <col class="col-xs-2">
        <col class="col-xs-2">
        <col class="col-xs-8">
</colgroup>
<thead>
<tr>
<td>parametre</td><td>öntanımlı değer ve olası değerler</td><td>açıklama</td>
</tr>
</thead>
<tbody>
<tr>
<td><code>data-url</code></td>
<td>location.href</td>
<td>paylaşılacak sayfa url'si. <i>bir değer belirtilmediğinde  ``location.href`` değeri paylaşılacak sayfa url'si olarak kabul edilir.</i></td>
</tr>
<tr>
<td><code>data-type</code></td>
<td>[<b>normal</b>|small|large|square]</td>
<td>buton tipi. değişik türler için aşağıya bakınız.</i></td>
</tr>
<tr>
<td><code>data-lang</code></td>
<td>[<b>tr</b>|en]</td>
<td>paylaşılacak instela dili.</i></td>
</tr>
</tbody>
</table>
</div><br>

### api

web sitesi sahipleri için web sitelerindeki linklerin instela'da paylaşım istatistiklerini sunan bir api'miz de bulunmaktadır. bu api'nin nasıl kullanılacağını öğrenmek için [api dökümantasyonunu](http://docs.instela.apiary.io/#reference/links){:target"_blank" class="external"} inceleyebilirsiniz.
<br>
<br>

### bazı notlar

javascript kütüphanesi yüklendikten sonra web sayfası üzerinde bulunan her instela paylaşım linki bir ``iframe`` etiketine dönüştürülür. bu iframe'in yerleşimi için sayfanızda bazı css önergeleri tanımlanamanız gerekebilir. bunları ``iframe.instela-share-button`` css sınıfını kullanarak tanımlayabilirsiniz. örneğin bu dökümantasyon sayfasının en sonunda kullanılan **instela'da paylaş** butonu için şu **css** özellikleri tanımlanmıştır:

{% highlight css %}
iframe.instela-share-button {
    display: inline-block;
    vertical-align: middle;
}
{% endhighlight %}

birden fazla paylaşım butonunun olduğu sayfalarda ``javascript`` kodunu yalnızca bir kere ``<head></head>`` linkleri arasına yerleştirmek yeterlidir.

