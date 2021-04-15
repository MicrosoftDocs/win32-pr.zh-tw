---
description: 進程的 WMI 工作會取得資訊，例如執行進程的帳戶。 您可以執行動作，例如建立進程。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: 2ae7c302-ab8b-4150-8ece-ffb66374b3f7
ms.tgt_platform: multiple
title: WMI 工作：處理序
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a720046d8f5cd25c55f2d5f367d2c23d5e4fc882
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104469553"
---
# <a name="wmi-tasks-processes"></a><span data-ttu-id="39325-105">WMI 工作：處理序</span><span class="sxs-lookup"><span data-stu-id="39325-105">WMI Tasks: Processes</span></span>

<span data-ttu-id="39325-106">進程的 WMI 工作會取得資訊，例如執行進程的帳戶。</span><span class="sxs-lookup"><span data-stu-id="39325-106">WMI tasks for processes obtain information such as the account under which a process is running.</span></span> <span data-ttu-id="39325-107">您可以執行動作，例如建立進程。</span><span class="sxs-lookup"><span data-stu-id="39325-107">You can perform actions like creating processes.</span></span> <span data-ttu-id="39325-108">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="39325-108">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="39325-109">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="39325-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="39325-110">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="39325-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="39325-111">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="39325-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="39325-112">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="39325-112">**To run a script**</span></span>

1.  <span data-ttu-id="39325-113">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="39325-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="39325-114">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="39325-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="39325-115">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="39325-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="39325-116">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="39325-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="39325-117">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="39325-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="39325-118">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="39325-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="39325-119">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="39325-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="39325-120">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="39325-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="39325-121">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="39325-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="39325-122">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="39325-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39325-123">如何…</span><span class="sxs-lookup"><span data-stu-id="39325-123">How do I...</span></span></th>
<th><span data-ttu-id="39325-124">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="39325-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39325-125">...在隱藏視窗中執行應用程式？</span><span class="sxs-lookup"><span data-stu-id="39325-125">...run an application in a hidden window?</span></span></td>
<td><span data-ttu-id="39325-126">從使用 <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> 和 <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> 類別的腳本呼叫應用程式。</span><span class="sxs-lookup"><span data-stu-id="39325-126">Call the application from a script that uses the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> and <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> classes.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39325-127">VB</span><span class="sxs-lookup"><span data-stu-id="39325-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HIDDEN_WINDOW = 0
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objStartup = objWMIService.Get(&quot;Win32_ProcessStartup&quot;)
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject(&quot;winmgmts:root\cimv2:Win32_Process&quot;)
errReturn = objProcess.Create( &quot;Notepad.exe&quot;, null, objConfig, intProcessID)</code></pre></td>
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
<th><span data-ttu-id="39325-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="39325-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$startup=[wmiclass]&quot;Win32_ProcessStartup&quot;
$startup.Properties[&#39;ShowWindow&#39;].value=$False
([wmiclass]&quot;win32_Process&quot;).create(&#39;notepad.exe&#39;,&#39;C:\&#39;,$Startup)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="39325-129">...判斷哪些腳本正在本機電腦上執行？</span><span class="sxs-lookup"><span data-stu-id="39325-129">...determine which scripts are running on the local computer?</span></span></td>
<td><p><span data-ttu-id="39325-130">使用 <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> 類別，並傳回名稱為 Cscript.exe 或 Wscript.exe 的所有進程。</span><span class="sxs-lookup"><span data-stu-id="39325-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and return all processes with the name Cscript.exe or Wscript.exe.</span></span> <span data-ttu-id="39325-131">若要判斷在這些進程中執行的個別腳本，請檢查 [ <strong>命令列</strong> ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="39325-131">To determine the individual scripts running in these processes, check the value of the <strong>CommandLine</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39325-132">VB</span><span class="sxs-lookup"><span data-stu-id="39325-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Process&quot; & _
           &quot; WHERE Name = &#39;cscript.exe&#39;&quot; & &quot; OR Name = &#39;wscript.exe&#39;&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;-------------------------------------------&quot;
    Wscript.Echo &quot;CommandLine: &quot; & objItem.CommandLine
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
<th><span data-ttu-id="39325-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="39325-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32_Process&quot; -ComputerName &quot;.&quot; | `
     where {($_.name -eq &#39;cscript.exe&#39;) -or ($_.name -eq &#39;wscript.exe&#39;) } | `
     Format-List -Property CommandLine, Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39325-134">...找出正在執行進程的帳戶名稱嗎？</span><span class="sxs-lookup"><span data-stu-id="39325-134">...find out the account name under which a process is running?</span></span></td>
<td><p><span data-ttu-id="39325-135">使用 <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="39325-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39325-136">VB</span><span class="sxs-lookup"><span data-stu-id="39325-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    colProperties = objProcess.GetOwner( strNameOfUser,strUserDomain)
    Wscript.Echo &quot;Process &quot; & objProcess.Name & &quot; is owned by &quot; & strUserDomain & &quot;\&quot; & strNameOfUser & &quot;.&quot;
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
<th><span data-ttu-id="39325-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="39325-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -class win32_process -ComputerName &quot;.&quot; | ForEach-Object { $_.GetOwner() | Select -Property domain, user }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39325-138">...變更正在執行之進程的優先順序？</span><span class="sxs-lookup"><span data-stu-id="39325-138">...change the priority of a running process?</span></span></td>
<td><p><span data-ttu-id="39325-139">使用 <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>SetPriority</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="39325-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>SetPriority</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39325-140">VB</span><span class="sxs-lookup"><span data-stu-id="39325-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const ABOVE_NORMAL = 32768
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcesses
    objProcess.SetPriority(ABOVE_NORMAL) 
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
<th><span data-ttu-id="39325-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="39325-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$ABOVE_NORMAL = 32768
$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.SetPriority($ABOVE_NORMAL) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39325-142">...使用腳本終止進程？</span><span class="sxs-lookup"><span data-stu-id="39325-142">...terminate a process using a script?</span></span></td>
<td><p><span data-ttu-id="39325-143">使用 <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="39325-143">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39325-144">VB</span><span class="sxs-lookup"><span data-stu-id="39325-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcessList
    objProcess.Terminate()
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
<th><span data-ttu-id="39325-145">PowerShell</span><span class="sxs-lookup"><span data-stu-id="39325-145">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.Terminate() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39325-146">...判斷每個進程使用的處理器時間和記憶體數量為何？</span><span class="sxs-lookup"><span data-stu-id="39325-146">...determine how much processor time and memory each process is using?</span></span></td>
<td><p><span data-ttu-id="39325-147">使用 <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> 類別和屬性，例如 <strong>KernelModeTime</strong>、 <strong>WorkingSetSize</strong>、 <strong>PageFileUsage</strong>和 <strong>PageFaults</strong>。</span><span class="sxs-lookup"><span data-stu-id="39325-147">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and properties such as <strong>KernelModeTime</strong>, <strong>WorkingSetSize</strong>, <strong>PageFileUsage</strong>, and <strong>PageFaults</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39325-148">VB</span><span class="sxs-lookup"><span data-stu-id="39325-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery(&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcesses
    Wscript.Echo &quot;Process: &quot; & objProcess.Name
    sngProcessTime = (CSng(objProcess.KernelModeTime) + CSng(objProcess.UserModeTime)) / 10000000
    Wscript.Echo &quot;Processor Time: &quot; & sngProcessTime
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults
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
<th><span data-ttu-id="39325-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="39325-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32s_Process&quot; -ComputerName $strComputer | `
     Format-List -Property Name, KernelModeTime, UserModeTime, ProcessID, WorkingSetSize, PageFileUsage, PageFaults</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39325-150">...告訴哪些應用程式正在遠端電腦上執行？</span><span class="sxs-lookup"><span data-stu-id="39325-150">...tell what applications are running on a remote computer?</span></span></td>
<td><p><span data-ttu-id="39325-151">使用 <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="39325-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39325-152">VB</span><span class="sxs-lookup"><span data-stu-id="39325-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process: &quot; & objProcess.Name 
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID 
    Wscript.Echo &quot;Thread Count: &quot; & objProcess.ThreadCount 
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage 
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults 
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize 
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
<th><span data-ttu-id="39325-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="39325-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
get-wmiObject -class Win32_Process -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
   Format-list Name, ProcessID, ThreadCount, PageFileUsage, PageFaults, WorkingSetSize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="39325-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="39325-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39325-155">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="39325-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="39325-156">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="39325-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="39325-157">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="39325-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

