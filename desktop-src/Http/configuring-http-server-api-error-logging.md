---
title: 設定 HTTP 伺服器 API 錯誤記錄
description: HTTP 伺服器 API 錯誤記錄是由 HTTP 參數索引鍵下的三個登錄值所控制 \\ 。
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- HTTP 伺服器 API，設定錯誤記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372164"
---
# <a name="configuring-http-server-api-error-logging"></a>設定 HTTP 伺服器 API 錯誤記錄

Http 伺服器 API 錯誤記錄是由位於以下位置的 **HTTP** \\ **參數** 機碼底下的三個登錄值所控制：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> 在未來的 Windows 作業系統版本中，設定值的位置和格式可能會變更。

 

使用者必須擁有系統管理員/本機系統許可權，才能修改登錄值，以及查看或修改記錄檔和包含它們的資料夾。

啟動 HTTP 伺服器 API 驅動程式時，會讀取登錄值中的設定資訊。 如此一來，如果設定已變更，則必須停止並重新啟動驅動程式，才能讀取新的值。 您可以使用下列主控台命令來完成這項作業：

**net stop HTTP**

**net start HTTP**

記錄檔會使用下列慣例來命名：

**HTTPerr +** *SequenceNumber* **+ .log**

例如： "HTTPerr4"。

當記錄檔達到 **ErrorLogFileTruncateSize** 登錄值所指定的大小上限時，就會迴圈記錄檔，而且此值不能小於 1 mb 的 (MB) 。

如果錯誤記錄的設定無效，或寫入記錄檔時發生任何種類的失敗，則 HTTP 伺服器 API 會使用事件記錄來通知系統管理員未進行錯誤記錄。

下表說明登錄設定值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>登錄值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td>可以設定為<strong>TRUE</strong>以啟用錯誤記錄的<strong>DWORD</strong> ，或設定為<strong>FALSE</strong>以停用它。 預設值為 <strong>TRUE</strong>。<br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td><strong>DWORD</strong> ，指定錯誤記錄檔的大小上限（以位元組為單位）。 預設值是 (0x100000) 的一 MB。<br/>
<blockquote>
[!Note]<br />
指定的值不能小於預設值。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td><strong>字串</strong>，指定 HTTP 伺服器 API 用來放置記錄檔的資料夾。 <br/> HTTP 伺服器 API &quot; &quot; 會在放置記錄檔的指定資料夾下建立名為 HTTPERR 的子資料夾。 這個子資料夾和記錄檔都會收到相同的許可權設定，這表示系統管理員和本機系統帳戶具有完整存取權，而其他使用者則沒有存取權。<br/> 如果登錄中未指定資料夾，預設資料夾如下：<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
ErrorLoggingDir 字串值必須是完整路徑，但它可以包含 &quot; % SystemRoot% &quot; 。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





