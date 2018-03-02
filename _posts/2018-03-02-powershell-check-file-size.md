---
layout: post
title: Check file size - Powershell
subtitle: Personal Wikipedia
---

coming soon...

{% highlight powershell linenos %}
$file = "test-file.zip"

if ((Get-Item $file).length -gt 3mb) { 
	Write-Output "info: Greater than 3mb." 
} 
else {
	Write-Error "Error on previous step. Please check the logs." 
}
{% endhighlight %}
