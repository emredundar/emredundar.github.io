---
layout: post
title: Check file size - Powershell
subtitle: Personal Wikipedia
---

A script I run generates a file as an output, but I could not know if the process is successful or not. That's why I need this simple "file size check" script.

{% highlight powershell linenos %}
$file = "C:\temp\test\test-file.zip"  # path of the file to check

if ((Get-Item $file).length -gt 3mb) { 
	Write-Output "info: File is greater than 3mb." 
} 
else {
	Write-Error "Error on previous step. The output file is not correct. Please check the logs." 
}
{% endhighlight %}
