---
description: 若要從本機電腦或從遠端電腦取得 WMI 的資料，您必須連接到特定的命名空間，以連線至 WMI 服務。
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: WMI 工作：連接至 WMI 服務
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987472"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>WMI 工作：連接至 WMI 服務

若要從本機電腦或從遠端電腦取得 WMI 的資料，您必須連接到特定的 [*命名空間*](gloss-n.md)，以連線至 wmi 服務。 在大部分情況下，請使用速記的 [標記](creating-a-wmi-script.md) 連接或 [**定位器**](swbemlocator-connectserver.md) 連接。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。

遠端連線需要適用于 Windows 防火牆和 DCOM 的適當設定。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md) 並 [透過 Windows 防火牆連接](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)。 從 Windows Vista 開始， (UAC) 的「使用者帳戶控制」可能會影響 WMI 存取。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。

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
<td>...使用 WMI 連接到遠端電腦？</td>
<td>請在您的「 <a href="constructing-a-moniker-string.md">標記</a> 」連接字串中指定下列其中一項：<br/>
<ul>
<li>NetBIOS 電腦名稱稱，例如 &quot; atl-dc-01&quot;</li>
<li>完整的功能變數名稱，例如 &quot; atl-dc-01.fabrikam.com&quot;</li>
<li>IPv4 位址，例如 &quot; 192.168.1。1&quot;</li>
<li>從 Windows Vista 開始，如果目的電腦和您要進行連線的電腦都執行 IPv6，您就可以指定 IPv6 位址。<br/></li>
</ul>
如需詳細資訊，請參閱連線 <a href="connecting-to-wmi-on-a-remote-computer.md">到遠端電腦上的 wmi</a> ，以及 <a href="ipv6-and-ipv4-support-in-wmi.md">WMI 中的 IPv6 和 IPv4 支援</a>。<br/> <span data-codelanguage="VisualBasic"></span>
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>...執行替代認證下的 WMI 腳本？</td>
<td><p>使用 <a href="swbemlocator-connectserver.md"><strong>wbemscripting.swbemlocator. ConnectServer</strong></a> 方法或 c + + 中的 <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator：： ConnectServer</strong></a> ，並包含適當的使用者名稱和密碼。 連接到本機電腦時，您無法變更認證。 如需詳細資訊，請參閱 <a href="creating-a-wmi-script.md">建立 Wmi 腳本</a> 和 <a href="connecting-to-wmi-on-a-remote-computer.md">連接至遠端電腦上的 wmi</a>。</p>
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
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
