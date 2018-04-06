---
layout: post
title: Dosya boyutu kontrolü - Powershell
subtitle: açık not defteri
meta-title: "Dosya boyutu kontrolü - Powershell - Emre Dündar"
permalink: /blog/powershell-dosya-boyutu/
tags: [powershell, script]
---

Kişisel not deferime not ettiğim ufak script'lerden ilkini bu platforma taşıyorum.

Çalıştırdığım hazır bir uygulama çıktı olarak bir dosya üretiyor. Uygulama hata alsa da sıfır boyutla bu dosyayı üretip başarılıymış gibi devam ediyor. Uygulamanın çalışma başarısını kontrol etmem mümkün olmadığı için üretilen dosyanın boyut bilgisini kullanıp doğrulama yapabiliyorum. Bu ihtiyaç nedeniyle aşağıdaki basit "dosya boyutu kontrolü" script'ini hazırladım.
Windows platformunda ve TFS2017 build taskları arasında çalıştırdığım için tercihimi powershell'den yana kullandım.

{% highlight powershell linenos %}
$file = "C:\temp\test\test-file.zip"   #kontrol edilecek dosya yolu
$control_size = "3mb"   #beklenen dosya boyutu için kontrol değeri

if ((Get-Item $file).length -gt $control_size) { 
	Write-Output "info: File is greater than $control_size." 
} 
else {
	Write-Error "Error on previous step. The output file is not correct. Please check the logs." 
}
{% endhighlight %}

<br/>
