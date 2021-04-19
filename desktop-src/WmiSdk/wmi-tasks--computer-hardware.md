---
description: 電腦硬體的 WMI 工作會取得硬體元件的狀態、狀態或屬性的相關資訊。
ms.assetid: eb4c2c38-4853-4486-b889-93a843d88edb
ms.tgt_platform: multiple
title: WMI 工作：電腦硬體
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5589c634a5a7bf11b95bc2d90ebeab038eb8af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980781"
---
# <a name="wmi-tasks-computer-hardware"></a><span data-ttu-id="72948-103">WMI 工作：電腦硬體</span><span class="sxs-lookup"><span data-stu-id="72948-103">WMI Tasks: Computer Hardware</span></span>

<span data-ttu-id="72948-104">電腦硬體的 WMI 工作會取得硬體元件的狀態、狀態或屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="72948-104">WMI tasks for computer hardware obtain information about the presence, state, or properties of hardware components.</span></span> <span data-ttu-id="72948-105">例如，您可以判斷電腦是否為桌上型電腦或膝上型電腦。</span><span class="sxs-lookup"><span data-stu-id="72948-105">For example, you can determine whether a computer is a desktop or laptop.</span></span> <span data-ttu-id="72948-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="72948-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="72948-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="72948-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="72948-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="72948-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-run-a-script"></a><span data-ttu-id="72948-109">執行指令碼</span><span class="sxs-lookup"><span data-stu-id="72948-109">To run a script</span></span>

<span data-ttu-id="72948-110">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="72948-110">The following procedure describes how to run a script.</span></span>

1.  <span data-ttu-id="72948-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="72948-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="72948-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="72948-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="72948-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="72948-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="72948-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="72948-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="72948-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="72948-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="72948-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="72948-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="72948-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="72948-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="72948-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="72948-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="72948-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="72948-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="72948-120">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="72948-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-121">如何…</span><span class="sxs-lookup"><span data-stu-id="72948-121">How do I...</span></span></th>
<th><span data-ttu-id="72948-122">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="72948-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="72948-123">...判斷電腦有多少可用記憶體？</span><span class="sxs-lookup"><span data-stu-id="72948-123">...determine how much free memory a computer has?</span></span></td>
<td><span data-ttu-id="72948-124">使用類別 <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> 與 <strong>FreePhysicalMemory</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="72948-124">Use the class <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> and the <strong>FreePhysicalMemory</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-125">VB</span><span class="sxs-lookup"><span data-stu-id="72948-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colSettings 
    Wscript.Echo &quot;Available Physical Memory: &quot; & objOperatingSystem.FreePhysicalMemory
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
<th><span data-ttu-id="72948-126">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-126">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$mem = Get-WmiObject -Class Win32_OperatingSystem
&quot;System : {0}&quot; -f $mem.csname
&quot;Free Memory: {0}&quot; -f $mem.FreePhysicalMemory</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="72948-127">...判斷電腦是否有 DVD 光碟機？</span><span class="sxs-lookup"><span data-stu-id="72948-127">...determine whether a computer has a DVD drive?</span></span></td>
<td><p><span data-ttu-id="72948-128">使用 <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> 類別，並在 [ <strong>名稱</strong> ] 或 [ <strong>DeviceID</strong> ] 屬性中檢查縮寫 DVD。</span><span class="sxs-lookup"><span data-stu-id="72948-128">Use the <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> class and check for the acronym DVD in the <strong>Name</strong> or <strong>DeviceID</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-129">VB</span><span class="sxs-lookup"><span data-stu-id="72948-129">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_CDROMDrive&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Name: &quot; & objItem.Name 
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
<th><span data-ttu-id="72948-130">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-130">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$drives = Get-WmiObject -Class Win32_CDROMDrives
$drives | Format-Table DeviceID, Description, Name -autosize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72948-131">...判斷電腦上安裝了多少 RAM？</span><span class="sxs-lookup"><span data-stu-id="72948-131">...determine how much RAM is installed in a computer?</span></span></td>
<td><p><span data-ttu-id="72948-132">使用 <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> 類別，並檢查 <strong>TotalPhysicalMemory</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="72948-132">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>TotalPhysicalMemory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-133">VB</span><span class="sxs-lookup"><span data-stu-id="72948-133">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Total Physical Memory: &quot; & objComputer.TotalPhysicalMemory
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
<th><span data-ttu-id="72948-134">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-134">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$mem = Get-WmiObject -Class Win32_ComputerSystem</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72948-135">...判斷電腦是否有一個以上的處理器？</span><span class="sxs-lookup"><span data-stu-id="72948-135">...determine if a computer has more than one processor?</span></span></td>
<td><p><span data-ttu-id="72948-136">使用 <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> 類別和屬性 <strong>NumberOfProcessors</strong>。</span><span class="sxs-lookup"><span data-stu-id="72948-136">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the property <strong>NumberOfProcessors</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-137">VB</span><span class="sxs-lookup"><span data-stu-id="72948-137">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Number of Processors: &quot; & objComputer.NumberOfProcessors
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
<th><span data-ttu-id="72948-138">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-138">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&quot;System Name : {0}&quot; -f $system.Name
&quot;Number of Processors: {0}&quot; -f $system.NumberOfProcessors</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72948-139">...判斷電腦是否有 PCMCIA 插槽？</span><span class="sxs-lookup"><span data-stu-id="72948-139">...determine whether a computer has a PCMCIA slot?</span></span></td>
<td><p><span data-ttu-id="72948-140">使用 <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> 類別，並檢查 <strong>Count</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="72948-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> class and check the value of the <strong>Count</strong> property.</span></span> <span data-ttu-id="72948-141">如果 <strong>Count</strong> 是0，表示電腦沒有 PCMCIA 插槽。</span><span class="sxs-lookup"><span data-stu-id="72948-141">If <strong>Count</strong> is 0, then the computer has no PCMCIA slots.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-142">VB</span><span class="sxs-lookup"><span data-stu-id="72948-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PCMCIAController&quot;)
Wscript.Echo &quot;Number of PCMCIA slots: &quot; & colItems.Count</code></pre></td>
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
<th><span data-ttu-id="72948-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Pcmcia = Get-WmiObject -Class Win32_PCMCIAController

if (!$pcmcia.count) {
    &quot;Number of PCMCIA Slots: {0}&quot; -f 1
}else {
    &quot;Number of PCMCIA Slots: {0}&quot; -f $pcmcia.count
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72948-144">...找出 (<strong>裝置管理員</strong>) 中標示驚嘆號圖示的裝置無法運作？</span><span class="sxs-lookup"><span data-stu-id="72948-144">...identify devices that are not working (those marked with an exclamation point icon in <strong>Device Manager</strong>)?</span></span></td>
<td><p><span data-ttu-id="72948-145">使用 <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> 類別，並在您的 <a href="querying-with-wql.md">WQL</a> 查詢中使用下列子句。</span><span class="sxs-lookup"><span data-stu-id="72948-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> class and use the following clause in your <a href="querying-with-wql.md">WQL</a> query.</span></span> <span data-ttu-id="72948-146"><strong>其中 ConfigManagerErrorCode <> 0</strong> 請注意，此程式碼可能無法偵測到缺少驅動程式的 USB 裝置。</span><span class="sxs-lookup"><span data-stu-id="72948-146"><strong>WHERE ConfigManagerErrorCode <> 0</strong> Note that this code may not detect USB devices that are missing drivers.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-147">VB</span><span class="sxs-lookup"><span data-stu-id="72948-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PnPEntity WHERE ConfigManagerErrorCode <> 0&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Class GUID: &quot; & objItem.ClassGuid
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Manufacturer: &quot; & objItem.Manufacturer
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Service: &quot; & objItem.Service
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
<th><span data-ttu-id="72948-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$baddevices = Get-WmiObject Win32_PNPEntity | where {$_.ConfigManagerErrorcode -ne 0}
&quot; Total Bad devices: {0}&quot; -f $baddevices.count
foreach ($device in $baddevices) {
    &quot;Name : {0}&quot; -f $device.name
    &quot;Class Guid : {0}&quot; -f $device.Classguid
    &quot;Description : {0}&quot; -f $device.Description
    &quot;Device ID : {0}&quot; -f $device.deviceid
    &quot;Manufacturer : {0}&quot; -f $device.manufactuer
    &quot;PNP Devcice Id : {0}&quot; -f $device.PNPDeviceID
    &quot;Service Name : {0}&quot; -f $device.service
    &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72948-149">...要判斷電腦上使用的滑鼠屬性嗎？</span><span class="sxs-lookup"><span data-stu-id="72948-149">...determine the properties of the mouse used on computer?</span></span></td>
<td><p><span data-ttu-id="72948-150">使用 <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="72948-150">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> class.</span></span> <span data-ttu-id="72948-151">這會傳回所有指標裝置的屬性，而不只是滑鼠裝置。</span><span class="sxs-lookup"><span data-stu-id="72948-151">This returns the properties of all pointing devices, not just mouse devices.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-152">VB</span><span class="sxs-lookup"><span data-stu-id="72948-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PointingDevice&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Device Interface: &quot; & objItem.DeviceInterface
    Wscript.Echo &quot;Double Speed Threshold: &quot; & objItem.DoubleSpeedThreshold
    Wscript.Echo &quot;Handedness: &quot; & objItem.Handedness
    Wscript.Echo &quot;Hardware Type: &quot; & objItem.HardwareType
    Wscript.Echo &quot;INF File Name: &quot; & objItem.InfFileName
    Wscript.Echo &quot;INF Section: &quot; & objItem.InfSection
    Wscript.Echo &quot;Manufacturer: &quot; & objItem.Manufacturer
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Number Of Buttons: &quot; & objItem.NumberOfButtons
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Pointing Type: &quot; & objItem.PointingType
    Wscript.Echo &quot;Quad Speed Threshold: &quot; & objItem.QuadSpeedThreshold
    Wscript.Echo &quot;Resolution: &quot; & objItem.Resolution
    Wscript.Echo &quot;Sample Rate: &quot; & objItem.SampleRate
    Wscript.Echo &quot;Synch: &quot; & objItem.Synch
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
<th><span data-ttu-id="72948-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Get Mouse information

$mouse = Get-WmiObject -Class Win32_PointingDevice

<# Decode detalis #>

function Deviceinterface {
    param ($value)
    switch ($value) {
        0 {&quot;Other&quot;}
        1 {&quot;Unknown&quot;}
        3 {&quot;Serial&quot;}
        4 {&quot;PS/2&quot;}
        5 {&quot;Infrared&quot;}
        6 {&quot;HP-HIL&quot;}
        7 {&quot;Bus Mouse&quot;}
        8 {&quot;ADP (Apple Desktop Bus)&quot;}
        160 {&quot;Bus Mouse DB-9&quot;}
        161 {&quot;Bus Mouse Micro-DIN&quot;}
        162 {&quot;USB&quot;}
    }
}

function Handedness {
    param ($value)
    switch ($value) {
        0 {&quot;Unknown&quot;}
        1 {&quot;Not Applicable&quot;}
        2 {&quot;Right-Handed Operation&quot;}
        3 {&quot;Left-Handed Operation&quot;}
    }
}

function Pointingtype {

param ($value)
    switch ($value) {
        1 {&quot;Other&quot;}
        2 {&quot;Unknown&quot;}
        3 {&quot;Mouse&quot;}
        4 {&quot;Track Ball&quot;}
        5 {&quot;Track Point&quot;}
        6 {&quot;Glide Point&quot;}
        7 {&quot;Touch Pad&quot;}
        8 {&quot;Touch Screen&quot;}
        9 {&quot;Mouse - Optical Sensor&quot;}
    }
}

<# Display details #>

&quot;Mouse Information on System: {0}&quot; -f $mouse.systemname
&quot;Description : {0}&quot; -f $mouse.Description
&quot;Device ID : {0}&quot; -f $mouse.DeviceID
&quot;Device Interface : {0}&quot; -f (Deviceinterface($mouse.DeviceInterface))
&quot;Double Speed Threshold : {0}&quot; -f $mouse.DoubleSpeedThreshold
&quot;Handedness : {0}&quot; -f (Handedness($mouse.handedness))
&quot;Hardware Type : {0}&quot; -f $mouse.Hardwaretype
&quot;INF FIle Name : {0}&quot; -f $mouse.InfFileName
&quot;Inf Section : {0}&quot; -f $mouse.InfSection
&quot;Manufacturer : {0}&quot; -f $mouse.Manufacturer
&quot;Name : {0}&quot; -f $mouse.Name
&quot;Number of buttons : {0}&quot; -f $mouse.NumberOfButtons
&quot;PNP Device ID : {0}&quot; -f $mouse.PNPDeviceID
&quot;Pointing Type : {0}&quot; -f (Pointingtype ($mouse.PointingType))
&quot;Quad Speed Threshold : {0}&quot; -f $mouse.QuadSpeedThreshold
&quot;Resolution : {0}&quot; -f $mouse.Resolution
&quot;Sample Rate : {0}&quot; -f $mouse.SampleRate
&quot;Synch : {0}&quot; -f $mouse.Synch</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72948-154">...判斷電腦上所安裝處理器的速度？</span><span class="sxs-lookup"><span data-stu-id="72948-154">...determine the speed of a processor installed in a computer?</span></span></td>
<td><p><span data-ttu-id="72948-155">使用 <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> 類別，並檢查 <strong>MaxClockSpeed</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="72948-155">Use the <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> class and check the value of the <strong>MaxClockSpeed</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-156">VB</span><span class="sxs-lookup"><span data-stu-id="72948-156">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Processor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Processor Id: &quot; & objItem.ProcessorId
    Wscript.Echo &quot;Maximum Clock Speed: &quot; & objItem.MaxClockSpeed
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72948-157">...判斷電腦是塔式、迷你塔式、膝上型電腦等等嗎？</span><span class="sxs-lookup"><span data-stu-id="72948-157">...determine whether a computer is a tower, a mini-tower, a laptop, and so on?</span></span></td>
<td><p><span data-ttu-id="72948-158">使用 <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> 類別，並檢查 <strong>ChassisType</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="72948-158">Use the <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> class and check the value of the <strong>ChassisType</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-159">VB</span><span class="sxs-lookup"><span data-stu-id="72948-159">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colChassis = objWMIService.ExecQuery(&quot;Select * from Win32_SystemEnclosure&quot;)
For Each objChassis in colChassis
    For Each objItem in objChassis.ChassisTypes
        Wscript.Echo &quot;Chassis Type: &quot; & objItem
    Next
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
<th><span data-ttu-id="72948-160">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-160">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$processors = Get-WmiObject -Class Win32_Processor
foreach ($proc in $processors)
{
    &quot;Processor ID: &quot; + $proc.ProcessorID
    &quot;Maximum Clock Speed: &quot; + $proc.MaxClockSpeed
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72948-161">...取得電腦的序號和資產標記？</span><span class="sxs-lookup"><span data-stu-id="72948-161">...get the serial number and asset tag of a computer?</span></span></td>
<td><p><span data-ttu-id="72948-162">使用 <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> 類別，以及 <strong>SerialNumber</strong> 和 <strong>SMBIOSAssetTag</strong>屬性。</span><span class="sxs-lookup"><span data-stu-id="72948-162">Use the <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> class, and the properties <strong>SerialNumber</strong> and <strong>SMBIOSAssetTag</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-163">VB</span><span class="sxs-lookup"><span data-stu-id="72948-163">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSMBIOS = objWMIService.ExecQuery(&quot;Select * from Win32_SystemEnclosure&quot;)
For Each objSMBIOS in colSMBIOS
    Wscript.Echo &quot;Part Number: &quot; & objSMBIOS.PartNumber
    Wscript.Echo &quot;Serial Number: &quot; & objSMBIOS.SerialNumber
    Wscript.Echo &quot;Asset Tag: &quot; & objSMBIOS.SMBIOSAssetTag
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
<th><span data-ttu-id="72948-164">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-164">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSMBIOS = Get-WmiObject -Class Win32_SystemEnclosure

foreach ($objSMBIOS in $colSMBIOS)
{
    &quot;Part Number: &quot; + $objSMBIOS.PartNumber
    &quot;Serial Number: &quot; + $objSMBIOS.SerialNumber
    &quot;Asset Tag: &quot; + $objSMBIOS.SMBIOSAssetTag
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72948-165">...判斷哪種裝置插入 USB 埠？</span><span class="sxs-lookup"><span data-stu-id="72948-165">...determine what kind of device is plugged into a USB port?</span></span></td>
<td><p><span data-ttu-id="72948-166">使用 <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> 類別並檢查 <strong>Description</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="72948-166">Use the <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> class and check the <strong>Description</strong> property.</span></span> <span data-ttu-id="72948-167">這個屬性的值可能如 &quot; 大量儲存裝置 &quot; 或 &quot; 列印支援 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="72948-167">This property may have a value such as &quot;Mass Storage Device&quot; or &quot;Printing Support&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-168">VB</span><span class="sxs-lookup"><span data-stu-id="72948-168">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_USBHub&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo
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
<th><span data-ttu-id="72948-169">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-169">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colItems = Get-WmiObject -Class Win32_USBHub

foreach ($objItem in $colItems)
{
    &quot;Device ID: &quot; + $objItem.DeviceID
    &quot;PNP Device ID: &quot; + $objItem.PNPDeviceID
    &quot;Description: &quot; + $objItem.Description
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72948-170">...判斷電腦上安裝了多少磁帶機？</span><span class="sxs-lookup"><span data-stu-id="72948-170">...determine how many tape drives are installed on a computer?</span></span></td>
<td><p><span data-ttu-id="72948-171">使用類別 <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> 類別，然後使用 <a href="swbemobjectset-count.md"><strong>swbemobjectset 搭配使用. Count</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="72948-171">Use the class <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> class and then use the <a href="swbemobjectset-count.md"><strong>SWbemObjectSet.Count</strong></a> method.</span></span> <span data-ttu-id="72948-172">如果 Count = 0，表示電腦上沒有安裝任何磁帶機。</span><span class="sxs-lookup"><span data-stu-id="72948-172">If Count = 0, then no tape drives are installed on the computer.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72948-173">VB</span><span class="sxs-lookup"><span data-stu-id="72948-173">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TapeDrive&quot;)
Wscript.Echo &quot;Number of tape drives: &quot; & colItems.Count</code></pre></td>
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
<th><span data-ttu-id="72948-174">PowerShell</span><span class="sxs-lookup"><span data-stu-id="72948-174">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colItems = Get-WmiObject -Class Win32_TapeDrive

foreach ($objItem in $colItems)
{
    &quot;Number of Drives: &quot; + $colItems.Count
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="72948-175">範例</span><span class="sxs-lookup"><span data-stu-id="72948-175">Examples</span></span>

<span data-ttu-id="72948-176">下列 TechNet 資源庫的 [範例程式碼](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) 說明如何列出數部電腦的所有磁片磁碟機的可用空間。</span><span class="sxs-lookup"><span data-stu-id="72948-176">The following TechNet Gallery [example code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) describes how to list the free space of all drives for several machines.</span></span>

<span data-ttu-id="72948-177">[本機/遠端電腦上的 get-computerinfo-查詢電腦資訊（ (WMI) ](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell 範例： TechNet 資源庫會使用一些硬體和軟體的呼叫，來顯示本機或遠端系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="72948-177">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software to display information about a local or remote system.</span></span>

<span data-ttu-id="72948-178">在 TechNetGallery 上 [使用 powershell powershell 範例收集的多執行緒系統資產](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) 會透過 WMI 和使用 powershell 的多執行緒，收集實用系統資訊的眾多。</span><span class="sxs-lookup"><span data-stu-id="72948-178">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell sample on TechNetGallery gathers a plethora of useful system information via WMI and multithreading with powershell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72948-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="72948-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72948-180">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="72948-180">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="72948-181">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="72948-181">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="72948-182">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="72948-182">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

