---
description: WMI 提供標準化的系統管理基礎結構，可供許多不同的用戶端運用。
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: 建立 WMI 用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95123d4462408a25591df2babb8b1ddd83942e5e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883055"
---
# <a name="creating-wmi-clients"></a>建立 WMI 用戶端

WMI 提供標準化的系統管理基礎結構，可供許多不同的用戶端運用。 這些用戶端的範圍從 wmic.exe 命令列工具到 System Center Operations Manager。 您可以使用 wmi 腳本 API、原生 c + + api，或使用 System. 管理 .NET Framework 類別庫命名空間中的類型，來撰寫自己的 wmi 用戶端。

## <a name="how-to-create-a-wmi-client"></a>如何建立 WMI 用戶端

WMI 的核心功能包括從 WMI 存放庫中取出物件，以及檢查這些物件的屬性。 您也可以選擇更新這些屬性，或呼叫這些屬性上的方法。 下列範例示範如何執行基本的 WMI 管理工作：抓取本機電腦的名稱。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>詞彙</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>使用 PowerShell 建立用戶端<br/></td>
<td>WMI 和 PowerShell 緊密整合;因此，使用 PowerShell 來抓取 WMI 物件只需要呼叫 Get-WmiObject Cmdlet。 請注意，為了保持一致性，第一個程式碼片段會明確陳述許多預設值;第二個假設預設值是正確的。<br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#explicitly states many of the default parameters
$myComputer = Get-WmiObject -ComputerName &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Query &quot;SELECT * FROM Win32_ComputerSystem&quot;
foreach ($computer in $myComputer)
{ &quot;System Name: &quot; + $computer.name }

#assumes the default values are correct
Get-WmiObject Win32_ComputerSystem | Format-Table &quot;Name&quot;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><p><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>使用 VBScript 建立用戶端</p></td>
<td><p>VBScript 是一般與 WMI 搭配使用的原始指令碼語言。 雖然 PowerShell 已越來越受歡迎，但本檔中有許多現有的程式碼範例都是以 VBScript 撰寫的。 請注意，這個特定的 VBScript 範例會明確指出本機電腦路徑以及模擬等級;這並非必要，但通常是最佳作法。</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Computer Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>使用 c # 建立用戶端 (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. 管理基礎結構</a>) </p></td>
<td><p>此命名空間包含使用受控碼來存取 WMI 的目前解決方案，也稱為 Windows 管理基礎結構 (MI 或 WMIv2) 。 目前，MI 是建立受控管理用戶端的支援技術。 如需詳細資訊，請參閱 <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">如何執行 MANAGED MI 用戶端</a> ，以及 <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">如何執行原生 MI 用戶端</a>。</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>使用 c # (<a href="/dotnet/api/system.management">System. 管理</a>) 建立用戶端</p></td>
<td><p>此命名空間包含使用受控碼來存取 WMI 的原始解決方案。 雖然 <a href="/dotnet/api/system.management">System. 管理</a> 類別仍然可用，但 <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft 管理的基礎結構</a> 類別通常更有效率，而且更適合調整規模。 因此，建議您使用 MI 類別，而不是使用原始的 WMI 類別。</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

下表列出此章節所涵蓋的主題。



| 主題                                                                                                        | 描述                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)                         | 描述當用戶端在遠端電腦上使用 WMI 基礎結構時，所發生的一些問題。                                                                                          |
| [腳本和應用程式的 WMI 工作](wmi-tasks-for-scripts-and-applications.md)                         | 顯示範例 WMI 用戶端程式代碼。                                                                                                                                                                 |
| [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)                             | 提供有關建立各種 WMI 用戶端的資訊。                                                                                                                                       |
| [監視效能資料](monitoring-performance-data.md)                                               | 說明如何使用 WMI 來監視效能資料。                                                                                                                                          |
| [接收 WMI 事件](receiving-a-wmi-event.md)                                                           | 說明如何查看 WMI 事件。                                                                                                                                                              |
| [監視事件](monitoring-events.md)                                                                   | 描述如何監視 WMI 事件。                                                                                                                                                           |
| [使用 WQL 查詢](querying-with-wql.md)                                                                   | 介紹 (WQL) 的 WMI 查詢語言。                                                                                                                                                       |
| [查詢選用功能的狀態](querying-the-status-of-optional-features.md)                     | 在 Windows 7 中，WMI 已實作為 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)類別。 此類別會抓取存在於電腦上之選用功能的狀態。 |
| [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)                       | 著重于描述 WMI 受管理實體位置的語法。                                                                                                                     |
| [使用 WMI 存取其他作業系統功能](accessing-other-operating-system-features-with-wmi.md) | 說明如何撰寫可存取設備磁碟機、Active Directory 和 SNMP 裝置的 WMI 用戶端。                                                                                             |
| [存取 Interop 命名空間中的資料](accessing-data-in-the-interop-namespace.md)                       | 關聯提供者可讓 Windows Management Instrumentation (WMI) 用戶端，以從不同的命名空間來進行設定檔和相關聯的類別實例。                      |
| [操作類別和實例資訊](manipulating-class-and-instance-information.md)               | 描述 WMI 用戶端必須執行的一般工作。                                                                                                                                      |
| [將類別連結在一起](linking-classes-together.md)                                                     | 討論 view 提供者，以及如何使用它來結合多個 WMI 類別的資訊。                                                                                    |
| [修改系統登錄](modifying-the-system-registry.md)                                           | 描述 WMI 用戶端如何使用 WMI 來管理系統註冊表資訊。                                                                                                                   |



 

