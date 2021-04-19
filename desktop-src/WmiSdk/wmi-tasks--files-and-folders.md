---
description: 檔案和資料夾的 WMI 工作會透過 WMI 變更檔案或資料夾屬性，包括建立共用或重新命名檔案。
ms.assetid: 91281fe1-0461-48da-ac5c-cab7e8e1b285
ms.tgt_platform: multiple
title: WMI 工作：檔案和資料夾
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b24d5f7708b88507cd08b73c0b08a83c94f6bb28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975291"
---
# <a name="wmi-tasks-files-and-folders"></a>WMI 工作：檔案和資料夾

檔案和資料夾的 WMI 工作會透過 WMI 變更檔案或資料夾屬性，包括建立共用或重新命名檔案。 如果您想要複製檔案或讀取和寫入檔案，最簡單的方式是使用 Windows Script Host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) ，而不是 WMI。 如需其他範例，請參閱[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)的檔案[和資料夾](/previous-versions/tn-archive/ee176985(v=technet.10))一節。

[**CIM \_資料檔案**](/windows/desktop/CIMWin32Prov/cim-datafile) 是在 WMI 中執行的幾個 [CIM 類別](cimclas.md) 之一。 避免列舉或查詢電腦上 **CIM \_ 資料檔案** 的所有實例，因為資料量可能會影響效能或造成電腦停止回應。

本主題所顯示的腳本範例只會從本機電腦取得資料。 如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。


下列程式描述如何執行腳本。

**執行指令碼**

1.  複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。 確定您的文字編輯器不會將 .txt 副檔名新增至檔案。
2.  開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。
3.  在命令提示字元中，輸入 **cscript filename.vbs** 。
4.  如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。 某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。

> [!Note]  
> 依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。 由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。 在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。

 

下表列出可用於從本機電腦取得各種資料類型的腳本範例。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>如何…</th>
<th>WMI 類別或方法</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>...重新命名檔案而不收到錯誤訊息？</td>
<td>使用 <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> 類別。 請確定您在呼叫 <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>重新命名</strong></a> 方法時傳遞整個路徑名稱，例如C:\Scripts\Test.txt， &quot; &quot; 而不是 &quot;Text.txt&quot; 。 針對 PowerShell，使用 <strong>CIM_DataFile</strong> 可能沒有效率。 因此，您可以直接使用 Rename-Item Cmdlet。<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery (&quot;Select * from CIM_DataFile where Name = &quot; & &quot;&#39;c:\\scripts\\toggle_service.vbs&#39;&quot;)
For Each objFile in colFiles
    errResult = objFile.Rename(&quot;c:\scripts\toggle_service.old&quot;)
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>rename-item c:\scripts\toggle_service.vbs toggle_service.old</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>...判斷使用者是否有。MP3 檔案儲存在其電腦上？</td>
<td><p>使用 <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> 類別，並使用下列 <a href="querying-with-wql.md">WQL</a> <strong>Where</strong> 子句選取檔案： where Extension = &quot; MP3 &quot; 。</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery(&quot;Select * from CIM_DataFile where Extension = &#39;mp3&#39;&quot;)
For Each objFile in colFiles
    Wscript.Echo &quot;File Name: &quot; & objFile.Name & &quot;.&quot; & objFile.Extension
    Wscript.Echo &quot;Path: &quot; & objFile.Path
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class CIM_DataFile -namespace &quot;root\cimv2&quot; -Filter &quot;Extension = &#39;mp3&#39;&quot; | `
   format-list Name, Extension, Path</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>...在電腦上建立共用資料夾？</td>
<td><p>使用 <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> 方法。</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 25
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objNewShare = objWMIService.Get(&quot;Win32_Share&quot;)
errReturn = objNewShare.Create(&quot;C:\Finance&quot;, &quot;FinanceShare&quot;, FILE_SHARE, MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;)</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$FILE_SHARE = 0
$MAXIMUM_CONNECTIONS = 25

$NewDir = new-item C:\Finance -type directory 
$Shares= [WMICLASS]&quot;Win32_Share&quot;
[void]$Shares.Create(&quot;C:\Finance&quot;,&quot;FinanceShare&quot;, $FILE_SHARE, $MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;) </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>...要複製資料夾嗎？</td>
<td><p>使用 <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>複製</strong></a> 方法。 針對 PowerShell，您可以直接使用 Copy-Item Cmdlet。</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery(&quot;Select * from Win32_Directory where Name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy(&quot;D:\Archive&quot;) 
Next </code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Copy-Item C:\Scripts -Destination D:\Archive -Recurse</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>...要移動資料夾嗎？</td>
<td><p>使用 <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>重新命名</strong></a> 方法。 針對 PowerShell，您可以直接使用 Move-Item Cmdlet。</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; _ 
    & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery _ 
    (&quot;Select * from Win32_Directory where name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename(&quot;C:\Admins\Documents\Archive\VBScript&quot;) 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>move-item -path C:\Scripts -destination C:\Admins\Documents\Archive\PowerShell</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[腳本和應用程式的 WMI 工作](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[WMI c + + 應用程式範例](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
