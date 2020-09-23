<div align="center">

## Upload / Download code using System\.Net\.WebClient Class, POST DATA, or download HTML webpages etc


</div>

### Description

This code can send data to a webpage using the HTTP POST method, or download an HTML webpage and return a string response value in both cases.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jon Barker](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jon-barker.md)
**Level**          |Intermediate
**User Rating**    |3.7 (11 globes from 3 users)
**Compatibility**  |VB\.NET
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__10-9.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jon-barker-upload-download-code-using-system-net-webclient-class-post-data-or-download-htm__10-794/archive/master.zip)





### Source Code

```
====== < PUT RIGHT AT TOP OF MODULE
Imports System
Imports System.text
======= < PUT RIGHT AT TOP OF MODULE
Function DownloadPage(ByVal sCompleteURL As String) As String
  Dim wDownload As System.Net.WebClient = New System.Net.WebClient()
  Dim bHTML As Byte() = wDownload.DownloadData(sCompleteURL)
  Dim sWebPage As String = Encoding.ASCII.GetChars(bHTML)
  Return sWebpage
 End Function
Function PostData(ByVal sAddress As String, ByVal sData As String) As String
  Dim wUpload As Net.WebClient = New System.Net.WebClient()
  Dim bPostArray As Byte() = Encoding.ASCII.GetBytes(sData)
  Dim bResponse As Byte() = wUpload.UploadData(sAddress, "POST", bPostArray)
  Dim sWebPage As String = Encoding.ASCII.GetChars(bResponse)
  Return sWebPage
 End Function
```

