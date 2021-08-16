---
description: WMI 排程工作會建立並取得已排程工作的相關資訊。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: WMI 工作：已排程的工作
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee4fcf193296d5c474987a3a99877b3bfb43868f79527200893303df351920cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738837"
---
# <a name="wmi-tasks-scheduled-tasks"></a>WMI 工作：已排程的工作

WMI 排程工作會建立並取得已排程工作的相關資訊。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。

本主題所顯示的腳本範例只會從本機電腦取得資料。 如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。


下列程式描述如何執行腳本。

**執行指令碼**

1.  複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。 確定您的文字編輯器不會在檔案中加入 .txt 延伸模組。
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
<td>...使用腳本建立排定的工作？</td>
<td>使用 <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> 方法。 如果您在 Windows 7 或更新版本上執行此工作時遇到困難，請參閱<strong>Win32_ScheduledJob</strong>備註區段;您的設定可能會導致您無法使用類別。<br/> <span data-codelanguage="VisualBasic"></span>
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
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p>在 &quot; Create 方法) 的 StartTime 參數值中使用的字串 * * * * * * * 143000.000000-420 (中，* * * * * * * * &quot; <em></em> <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong></strong></a> &quot; 143000.000000 &quot; 指定工作從 14.30 (2:30 P.M. 開始 ) 和 &quot; -420 &quot; 則指定時區。 時區號碼是本地時間轉譯的目前偏差。 偏差是 UTC 時間與當地時間之間的差異。 若要計算時區的偏差，請將您時區提前或晚于格林威治標準時間的小時數乘以60的 (GMT)  (如果您的時區是在 GMT 之前，則以小時為單位，如果您的時區晚于 gmt) ，則為負數。 如果您的時區使用日光節約時間，請在您的計算中加入額外的60。 例如，太平洋標準時區是 GMT 後八小時，因此偏差等於-420 (-8 * 60 + 60) 當日光節約時間正在使用中，且當日光節約時間未使用時，則為-480 (-8 * 60) 。 您也可以藉由查詢 <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> 類別的偏差屬性來判斷偏差的值。</p></td>
</tr>
<tr class="even">
<td>...傳回電腦上所有排程工作的清單嗎？</td>
<td><p>使用 <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> 類別。 請注意，這個類別只能傳回使用腳本或 AT.exe 所建立的工作。 它無法傳回排程工作 wizard 所建立或修改之作業的相關資訊。</p>
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
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
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

 

