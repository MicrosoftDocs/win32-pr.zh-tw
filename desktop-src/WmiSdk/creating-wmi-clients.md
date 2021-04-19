---
description: WMI 提供標準化的系統管理基礎結構，可供許多不同的用戶端運用。
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: 建立 WMI 用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd6d89c63218ffd20ef66b2115e581bdb9c4373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978896"
---
# <a name="creating-wmi-clients"></a><span data-ttu-id="6bb1d-103">建立 WMI 用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb1d-103">Creating WMI Clients</span></span>

<span data-ttu-id="6bb1d-104">WMI 提供標準化的系統管理基礎結構，可供許多不同的用戶端運用。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-104">WMI provides a standardized system management infrastructure that can be leveraged by a number of different clients.</span></span> <span data-ttu-id="6bb1d-105">這些用戶端的範圍從 wmic.exe 命令列工具到 System Center Operations Manager。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-105">These clients range from the wmic.exe command line tool to System Center Operations Manager.</span></span> <span data-ttu-id="6bb1d-106">您可以使用 WMI 腳本 API、原生 c + + API，或使用 System. 管理 .NET Framework 類別庫命名空間中的類型，來撰寫自己的 WMI 用戶端。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-106">You can write your own WMI clients by using either the WMI Scripting API, the native C++ API or by using the types in the System.Management .NET Framework class library namespace.</span></span>

## <a name="how-to-create-a-wmi-client"></a><span data-ttu-id="6bb1d-107">如何建立 WMI 用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb1d-107">How to create a WMI client</span></span>

<span data-ttu-id="6bb1d-108">WMI 的核心功能包括從 WMI 存放庫中取出物件，以及檢查這些物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-108">The core functionality of WMI consists of retrieving objects from the WMI repository and examining the properties of those objects.</span></span> <span data-ttu-id="6bb1d-109">您也可以選擇更新這些屬性，或呼叫這些屬性上的方法。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-109">You can also choose to update those properties, or call methods on those properties.</span></span> <span data-ttu-id="6bb1d-110">下列範例示範如何執行基本的 WMI 管理工作：抓取本機電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-110">The following examples show how to perform a basic WMI administration task: retrieving the name of the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bb1d-111">詞彙</span><span class="sxs-lookup"><span data-stu-id="6bb1d-111">Term</span></span></th>
<th><span data-ttu-id="6bb1d-112">描述</span><span class="sxs-lookup"><span data-stu-id="6bb1d-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6bb1d-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>使用 PowerShell 建立用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb1d-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creating a client with PowerShell</span></span><br/></td>
<td><span data-ttu-id="6bb1d-114">WMI 和 PowerShell 緊密整合;因此，使用 PowerShell 來抓取 WMI 物件只需要呼叫 Get-WmiObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-114">WMI and PowerShell are tightly integrated; as such, retrieving WMI objects with PowerShell is simply a matter of calling the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="6bb1d-115">請注意，為了保持一致性，第一個程式碼片段會明確陳述許多預設值;第二個假設預設值是正確的。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-115">Note that for consistency, the first code snippet explicitly states many of the default values; the second assumes that the default values are correct.</span></span><br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bb1d-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6bb1d-116">PowerShell</span></span></th>
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
<td><p><span data-ttu-id="6bb1d-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>使用 VBScript 建立用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb1d-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creating a client with VBScript</span></span></p></td>
<td><p><span data-ttu-id="6bb1d-118">VBScript 是一般與 WMI 搭配使用的原始指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-118">VBScript was the original scripting language that had common use with WMI.</span></span> <span data-ttu-id="6bb1d-119">雖然 PowerShell 已越來越受歡迎，但本檔中有許多現有的程式碼範例都是以 VBScript 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-119">While PowerShell has become more popular, many of the existing code samples in this documentation are written in VBScript.</span></span> <span data-ttu-id="6bb1d-120">請注意，這個特定的 VBScript 範例會明確指出本機電腦路徑以及模擬等級;這並非必要，但通常是最佳作法。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-120">Note that this particular VBScript sample explicitly states both the local machine path as well as the impersonation level; this is not required, but is often a best practice.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bb1d-121">VB</span><span class="sxs-lookup"><span data-stu-id="6bb1d-121">VB</span></span></th>
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
<td><p><span data-ttu-id="6bb1d-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>使用 c # 建立用戶端 (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. 管理基礎結構</a>) </span><span class="sxs-lookup"><span data-stu-id="6bb1d-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creating a client with C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</span></span></p></td>
<td><p><span data-ttu-id="6bb1d-123">此命名空間包含使用受控碼來存取 WMI 的目前解決方案，也稱為 Windows 管理基礎結構 (MI 或 WMIv2) 。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-123">This namespace contains the current solution for accessing WMI with managed code, and is known as the Windows Management Infrastructure (MI, or WMIv2).</span></span> <span data-ttu-id="6bb1d-124">目前，MI 是建立受控管理用戶端的支援技術。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-124">Currently, MI is the supported technology for creating managed management clients.</span></span> <span data-ttu-id="6bb1d-125">如需詳細資訊，請參閱 <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">如何執行 MANAGED MI 用戶端</a> ，以及 <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">如何執行原生 MI 用戶端</a>。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-125">For more information, see <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">How to Implement a Managed MI Client</a> and <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">How to Implement a Native MI Client</a>.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bb1d-126">C#</span><span class="sxs-lookup"><span data-stu-id="6bb1d-126">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

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
<td><p><span data-ttu-id="6bb1d-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>使用 c # (<a href="/dotnet/api/system.management">System. 管理</a>) 建立用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb1d-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creating a client with C# (<a href="/dotnet/api/system.management">System.Management</a>)</span></span></p></td>
<td><p><span data-ttu-id="6bb1d-128">此命名空間包含使用受控碼來存取 WMI 的原始解決方案。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-128">This namespace contains the original solution for accessing WMI with managed code.</span></span> <span data-ttu-id="6bb1d-129">雖然 <a href="/dotnet/api/system.management">System. 管理</a> 類別仍然可用，但 <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft 管理的基礎結構</a> 類別通常更有效率，而且更適合調整規模。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-129">While the <a href="/dotnet/api/system.management">System.Management</a> classes are still available, the <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a> classes are generally more efficient and scale better.</span></span> <span data-ttu-id="6bb1d-130">因此，建議您使用 MI 類別，而不是使用原始的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-130">As such, it is recommended that you use the MI classes, rather than the original WMI classes.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bb1d-131">C#</span><span class="sxs-lookup"><span data-stu-id="6bb1d-131">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

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



 

<span data-ttu-id="6bb1d-132">下表列出此章節所涵蓋的主題。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-132">The following table lists the topics covered in this section.</span></span>



| <span data-ttu-id="6bb1d-133">主題</span><span class="sxs-lookup"><span data-stu-id="6bb1d-133">Topic</span></span>                                                                                                        | <span data-ttu-id="6bb1d-134">描述</span><span class="sxs-lookup"><span data-stu-id="6bb1d-134">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bb1d-135">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="6bb1d-135">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)                         | <span data-ttu-id="6bb1d-136">描述當用戶端在遠端電腦上使用 WMI 基礎結構時，所發生的一些問題。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-136">Describes a number of issues that arise when clients use the WMI infrastructure on a remote computer.</span></span>                                                                                          |
| [<span data-ttu-id="6bb1d-137">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="6bb1d-137">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)                         | <span data-ttu-id="6bb1d-138">顯示範例 WMI 用戶端程式代碼。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-138">Shows example WMI client code.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="6bb1d-139">建立 WMI 應用程式或腳本</span><span class="sxs-lookup"><span data-stu-id="6bb1d-139">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)                             | <span data-ttu-id="6bb1d-140">提供有關建立各種 WMI 用戶端的資訊。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-140">Provides information about creating various WMI clients.</span></span>                                                                                                                                       |
| [<span data-ttu-id="6bb1d-141">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="6bb1d-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)                                               | <span data-ttu-id="6bb1d-142">說明如何使用 WMI 來監視效能資料。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-142">Describes how to use WMI to monitor performance data.</span></span>                                                                                                                                          |
| [<span data-ttu-id="6bb1d-143">接收 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="6bb1d-143">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)                                                           | <span data-ttu-id="6bb1d-144">說明如何查看 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-144">Describes how to view WMI events.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="6bb1d-145">監視事件</span><span class="sxs-lookup"><span data-stu-id="6bb1d-145">Monitoring Events</span></span>](monitoring-events.md)                                                                   | <span data-ttu-id="6bb1d-146">描述如何監視 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-146">Describes how to monitor WMI events.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="6bb1d-147">使用 WQL 查詢</span><span class="sxs-lookup"><span data-stu-id="6bb1d-147">Querying with WQL</span></span>](querying-with-wql.md)                                                                   | <span data-ttu-id="6bb1d-148">介紹 (WQL) 的 WMI 查詢語言。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-148">Introduces the WMI Query Language (WQL).</span></span>                                                                                                                                                       |
| [<span data-ttu-id="6bb1d-149">查詢選用功能的狀態</span><span class="sxs-lookup"><span data-stu-id="6bb1d-149">Querying the Status of Optional Features</span></span>](querying-the-status-of-optional-features.md)                     | <span data-ttu-id="6bb1d-150">在 Windows 7 中，WMI 已實作為 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) 類別。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-150">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="6bb1d-151">此類別會抓取存在於電腦上之選用功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-151">This class retrieves the status of the optional features that are present on a computer.</span></span> |
| [<span data-ttu-id="6bb1d-152">描述 WMI 物件的位置</span><span class="sxs-lookup"><span data-stu-id="6bb1d-152">Describing the Location of a WMI Object</span></span>](describing-the-location-of-a-wmi-object.md)                       | <span data-ttu-id="6bb1d-153">著重于描述 WMI 受管理實體位置的語法。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-153">Focuses on the syntax for describing the location of a WMI managed entity.</span></span>                                                                                                                     |
| [<span data-ttu-id="6bb1d-154">使用 WMI 存取其他作業系統功能</span><span class="sxs-lookup"><span data-stu-id="6bb1d-154">Accessing Other Operating System Features with WMI</span></span>](accessing-other-operating-system-features-with-wmi.md) | <span data-ttu-id="6bb1d-155">說明如何撰寫可存取設備磁碟機、Active Directory 和 SNMP 裝置的 WMI 用戶端。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-155">Describes how to write WMI clients that access device drivers, Active Directory, and SNMP devices.</span></span>                                                                                             |
| [<span data-ttu-id="6bb1d-156">存取 Interop 命名空間中的資料</span><span class="sxs-lookup"><span data-stu-id="6bb1d-156">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)                       | <span data-ttu-id="6bb1d-157">關聯提供者可讓 Windows Management Instrumentation (WMI) 用戶端，以從不同的命名空間來進行設定檔和相關聯的類別實例。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-157">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>                      |
| [<span data-ttu-id="6bb1d-158">操作類別和實例資訊</span><span class="sxs-lookup"><span data-stu-id="6bb1d-158">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)               | <span data-ttu-id="6bb1d-159">描述 WMI 用戶端必須執行的一般工作。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-159">Describes the common tasks that WMI clients must perform.</span></span>                                                                                                                                      |
| [<span data-ttu-id="6bb1d-160">將類別連結在一起</span><span class="sxs-lookup"><span data-stu-id="6bb1d-160">Linking Classes Together</span></span>](linking-classes-together.md)                                                     | <span data-ttu-id="6bb1d-161">討論 view 提供者，以及如何使用它來結合多個 WMI 類別的資訊。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-161">Discusses the view provider and how it can be used to bring together information from multiple WMI classes.</span></span>                                                                                    |
| [<span data-ttu-id="6bb1d-162">修改系統登錄</span><span class="sxs-lookup"><span data-stu-id="6bb1d-162">Modifying the System Registry</span></span>](modifying-the-system-registry.md)                                           | <span data-ttu-id="6bb1d-163">描述 WMI 用戶端如何使用 WMI 來管理系統註冊表資訊。</span><span class="sxs-lookup"><span data-stu-id="6bb1d-163">Describes how WMI clients can use WMI to manage system registry information.</span></span>                                                                                                                   |



 

