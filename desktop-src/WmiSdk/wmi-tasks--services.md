---
description: 服務的 WMI 工作會取得服務的相關資訊，包括相依或之前的服務。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: 1cd92981-c074-4ff7-a32c-ce492e6d6aa5
ms.tgt_platform: multiple
title: WMI 工作：服務
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b786ce0e358a59922728be4e90bc8cdeaa37a298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985689"
---
# <a name="wmi-tasks-services"></a><span data-ttu-id="c0711-104">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="c0711-104">WMI Tasks: Services</span></span>

<span data-ttu-id="c0711-105">服務的 WMI 工作會取得服務的相關資訊，包括相依或之前的服務。</span><span class="sxs-lookup"><span data-stu-id="c0711-105">WMI tasks for services obtain information about services, including dependent or antecedent services.</span></span> <span data-ttu-id="c0711-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="c0711-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="c0711-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="c0711-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="c0711-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="c0711-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="c0711-109">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="c0711-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="c0711-110">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="c0711-110">**To run a script**</span></span>

1.  <span data-ttu-id="c0711-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="c0711-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="c0711-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="c0711-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="c0711-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="c0711-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="c0711-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="c0711-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="c0711-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="c0711-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="c0711-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="c0711-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="c0711-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="c0711-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="c0711-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="c0711-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="c0711-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="c0711-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="c0711-120">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="c0711-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>




<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0711-121">如何…</span><span class="sxs-lookup"><span data-stu-id="c0711-121">How do I...</span></span></th>
<th><span data-ttu-id="c0711-122">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="c0711-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0711-123">...判斷哪些服務正在執行，哪些服務不是？</span><span class="sxs-lookup"><span data-stu-id="c0711-123">...determine which services are running and which ones are not?</span></span></td>
<td><span data-ttu-id="c0711-124">使用 <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> 類別來檢查所有服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0711-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class to check the state of all of the services.</span></span> <span data-ttu-id="c0711-125">[狀態] 屬性可讓您知道服務是否已停止或正在執行。</span><span class="sxs-lookup"><span data-stu-id="c0711-125">The state property lets you know if a service is stopped or running.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0711-126">VB</span><span class="sxs-lookup"><span data-stu-id="c0711-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Service&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;Service Name: &quot; & objItem.Name & VBNewLine & &quot;State: &quot; & objItem.State
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
<th><span data-ttu-id="c0711-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0711-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | format-list Name, State</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0711-128">...要停止 Power 使用者啟動某些服務嗎？</span><span class="sxs-lookup"><span data-stu-id="c0711-128">...stop Power Users from starting certain services?</span></span></td>
<td><p><span data-ttu-id="c0711-129">使用 <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> 方法，將 <strong>StartMode</strong> 屬性設定為 Disabled。</span><span class="sxs-lookup"><span data-stu-id="c0711-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> method to set the <strong>StartMode</strong> property to Disabled.</span></span> <span data-ttu-id="c0711-130">停用的服務無法啟動，而且根據預設，Power Users 無法變更服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="c0711-130">Disabled services cannot be started, and, by default, Power Users cannot change the start mode of a service.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0711-131">VB</span><span class="sxs-lookup"><span data-stu-id="c0711-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service where StartMode = &#39;Manual&#39;&quot;)
For Each objService in colServiceList
    errReturnCode = objService.Change( , , , , &quot;Disabled&quot;)
    WScript.Echo &quot;Changed manual service to disabled: &quot; & objService.Name   
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
<th><span data-ttu-id="c0711-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0711-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.startMode -eq &quot;Manual&quot;} | `
    foreach-object { [void]$_.changeStartMode(&#39;Disabled&#39;) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0711-133">...要啟動和停止服務嗎？</span><span class="sxs-lookup"><span data-stu-id="c0711-133">...start and stop services?</span></span></td>
<td><p><span data-ttu-id="c0711-134">使用 <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> 類別以及 <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>StopService</strong></a> 和 <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="c0711-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>StopService</strong></a> and <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0711-135">VB</span><span class="sxs-lookup"><span data-stu-id="c0711-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colListOfServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where Name =&#39;Alerter&#39;&quot;)
For Each objService in colListOfServices
    objService.StartService()
    Wscript.Echo &quot;Started Alerter service&quot;
Next
</code></pre></td>
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
<th><span data-ttu-id="c0711-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0711-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.Name -eq &quot;Alerter&quot;} | `
    foreach-object { [void]$_.StartService() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0711-137">...使用腳本變更服務帳戶密碼？</span><span class="sxs-lookup"><span data-stu-id="c0711-137">...change service account passwords using a script?</span></span></td>
<td><p><span data-ttu-id="c0711-138">使用 <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>變更</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="c0711-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Change</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0711-139">VB</span><span class="sxs-lookup"><span data-stu-id="c0711-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service&quot;)
For Each objservice in colServiceList
    If objService.StartName = &quot;.\netsvc&quot; Then
        errReturn = objService.Change( , , , , , , , &quot;password&quot;)  
    End If 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0711-140">..判斷可以停止哪些服務？</span><span class="sxs-lookup"><span data-stu-id="c0711-140">..determine which services I can stop?</span></span></td>
<td><p><span data-ttu-id="c0711-141">使用 <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> 類別，並檢查 <strong>AcceptStop</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c0711-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class, and check the value of the <strong>AcceptStop</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0711-142">VB</span><span class="sxs-lookup"><span data-stu-id="c0711-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where AcceptStop = True&quot;)
For Each objService in colServices
    Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="c0711-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0711-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.AcceptStop -eq &quot;True&quot;} | `
     format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0711-144">...在啟動 DHCP 服務之前，請先找出必須執行的服務嗎？</span><span class="sxs-lookup"><span data-stu-id="c0711-144">...find the services that must be running before I can start the DHCP service?</span></span></td>
<td><p><span data-ttu-id="c0711-145">查詢名<a href="associators-of-statement.md"></a>為 DHCP 的<a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a>類別的 &quot; associators of &quot; ，該類別位於<a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a>類別中且 &quot; 相依于 &quot; <strong>Role</strong>屬性。</span><span class="sxs-lookup"><span data-stu-id="c0711-145">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Dependent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="c0711-146"><strong>角色</strong> 是指 DHCP 服務的角色：在此情況下，它相依于正在啟動的其他服務。</span><span class="sxs-lookup"><span data-stu-id="c0711-146"><strong>Role</strong> means the role of the DHCP service: in this case, it is dependent on the other services that are being started.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0711-147">VB</span><span class="sxs-lookup"><span data-stu-id="c0711-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery(&quot;Associators Of &quot; _ 
    & &quot;{Win32_Service.Name=&#39;dhcp&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Dependent&quot;) 
For Each objService in colServiceList
Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="c0711-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0711-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators Of {Win32_Service.Name=&#39;dhcp&#39;} Where AssocClass=Win32_DependentService Role=Dependent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0711-149">...找出需要 WMI 服務 (Winmgmt) 服務在開始之前執行的服務嗎？</span><span class="sxs-lookup"><span data-stu-id="c0711-149">...find the services that require the WMI service (Winmgmt) service to be running before they can start?</span></span></td>
<td><p><span data-ttu-id="c0711-150">查詢 Win32_DependentService 類別中名為 DHCP 的<a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a>類別的<a href="associators-of-statement.md">associators of</a> &quot; &quot; ， <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong></strong></a>並且在 &quot; &quot; <strong>Role</strong>屬性中具有 Antecendent。</span><span class="sxs-lookup"><span data-stu-id="c0711-150">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Antecendent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="c0711-151"><strong>角色</strong> 表示 rasman 服務的角色：在此情況下，必須在相依服務之前啟動之前的。</span><span class="sxs-lookup"><span data-stu-id="c0711-151"><strong>Role</strong> means the role of the rasman service: in this case, it is antecedent to must be started before the dependent services.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0711-152">VB</span><span class="sxs-lookup"><span data-stu-id="c0711-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\ & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = _
    objWMIService.ExecQuery(&quot;Associators of &quot; _
    & &quot;{Win32_Service.Name=&#39;winmgmt&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Antecedent&quot; )
For Each objService in colServiceList
Wscript.Echo &quot;Name: &quot; & objService.Name & VBTab & &quot;Display Name: &quot; & objService.DisplayName 
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
<th><span data-ttu-id="c0711-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0711-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators of {Win32_Service.Name=&#39;winmgmt&#39;} Where AssocClass=Win32_DependentService Role=Antecedent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list Name, DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c0711-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0711-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0711-155">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="c0711-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="c0711-156">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="c0711-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="c0711-157">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="c0711-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
