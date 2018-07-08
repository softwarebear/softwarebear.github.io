---
layout: post
title: Extract data to Excel compatible clipboard content
date: 2018-06-09T12:00:00Z
categories: jekyll update
---

Small Powershell script to create a table (a TSV) ...

```
$delimiter = "`t"; 

$fileInfo = Get-ChildItem -Recurse | Sort LastWriteTime | SELECT FullName, LastWriteTime 
$fileInfo | ConvertTo-Csv -Delimiter $delimiter | Set-Clipboard
```

... the clipboard can now be pasted into Excel and you'll end up with a nice table you can copy elsewhere, to email for instance, which doesn't like the CSV/TSV format.