---
description: 使用從效能計數器取得資料的 WMI 類別，存取和重新整理有關電腦效能的資料。
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: WMI 工作：效能監視
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91302b0d6c6e13f86f275d755c5f4b6150de6a59dd400e47ed877d01f3fe876e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312054"
---
# <a name="wmi-tasks-performance-monitoring"></a>WMI 工作：效能監視

使用從效能計數器取得資料的 WMI 類別，存取和重新整理有關電腦效能的資料。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。 如需詳細資訊，請參閱 [效能程式庫和 WMI](performance-libraries-and-wmi.md) 和 [監視效能資料](monitoring-performance-data.md)。

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
<td>...取得我可以在腳本的 Perfmon 公用程式中看到的效能計數器資料嗎？</td>
<td>使用名稱以 Win32_PerfFormattedData 開頭的類別 &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes"></a> &quot; ，例如<a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>。 名稱類似 <strong>PageFileBytes</strong> 的屬性會對應到您在 Perfmon 中看到的效能計數器。 &quot;Win32_PerfFormattedData &quot; 類別會為您計算計數器的最終值。<br/></td>
</tr>
<tr class="even">
<td>...取得單一進程、磁片磁碟機和其他資料的持續效能資料嗎？</td>
<td>使用 <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> 或適當的格式化 <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">效能計數器類別</a> 和 <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> 方法。 如需詳細資訊，請參閱 <a href="scripting-with-swbemobject.md">使用 SWbemObject 編寫腳本</a>。<br/> 在 c + + 中，請使用 <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher：： AddObjectByPath</strong></a> 和 <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher：： Refresh</strong></a>。 如需詳細資訊，請參閱 <a href="monitoring-performance-data.md">監視效能資料</a>。<br/> 下列腳本會在電腦重新開機、WMI 已停止或腳本停止之前執行。 若要手動停止腳本，請使用工作管理員停止進程。 若要以程式設計方式停止它，請使用<a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a>類別中的<a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a>方法。<br/> <span data-codelanguage="VisualBasic"></span>
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
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set PerfProcess = objWMIService.Get(_
    &quot;Win32_PerfFormattedData_PerfProc_Process.Name=&#39;Idle&#39;&quot;)

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td>...取得所有進程的持續效能資料，而不重複輪詢？</td>
<td><p>使用名稱開頭為 &quot; Win32_PerfFormattedData &quot; 和 <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> 物件的類別。 複習器會保存物件，因此您不需要重複取得集合。 需要最少兩個值來計算效能資料，因為大部分的計數器都是速率計數器。 當您第一次顯示重新整理程式資料時，它會是空的。</p>
<p>下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。 若要手動停止腳本，請使用工作管理員停止進程。 若要以程式設計方式停止它，請使用<a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a>類別中的<a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a>方法。</p>
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
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set objRefresher = CreateObject(&quot;WbemScripting.Swbemrefresher&quot;)
Set objProcessor = objRefresher.AddEnum _
    (objWMIService, _
    &quot;Win32_PerfFormattedData_PerfOS_Processor&quot;).ObjectSet

While (True)
    objRefresher.Refresh
        For each RefreshItem in objRefresher
            For each objProcess in RefreshItem.ObjectSet
                Wscript.Echo objProcess.GetObjectText_
            Next
        Next
     Wscript.Sleep 5000
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>...取得和計算 Windows 2000 上進程的效能資料？</td>
<td><p>使用 &quot; Win32_PerfRawData &quot; 類別，例如 <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>。 取得特定進程的屬性資料，例如 <strong>PercentProcessorTime</strong>、兩次。 查閱 <a href="countertype-qualifier.md"><strong>CounterType</strong></a> 限定詞中針對屬性指定的公式，然後計算。 範例中的 CounterType 是 <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>。 如需詳細資訊，請參閱 <a href="monitoring-performance-data.md">監視效能資料</a>。</p>
<p>下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。 若要手動停止腳本，請使用工作管理員停止進程。 若要以程式設計方式停止它，請使用<a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a>類別中的<a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a>方法。</p>
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
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)

While (True)
    Set object1 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N1 = object1.PercentProcessorTime
    D1 = object1.TimeStamp_Sys100NS
    Wscript.Sleep(1000)
    set object2 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N2 = object2.PercentProcessorTime
    D2 = object2.TimeStamp_Sys100NS
    &#39; CounterType - PERF_100NSEC_TIMER_INV
    &#39; Formula - (1- ((N2 - N1) / (D2 - D1))) x 100
    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    Wscript.Echo &quot;% Processor Time=&quot; , PercentProcessorTime
Wend</code></pre></td>
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
