---
description: 作業系統的 WMI 工作會取得作業系統的相關資訊，例如版本、是否已啟用，或已安裝的修補程式。
ms.assetid: a216ad56-2650-4d93-86e1-449b56019361
ms.tgt_platform: multiple
title: WMI 工作：作業系統
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8d4dff83cebf5fd3336aeec2cc45ac4d8498cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989007"
---
# <a name="wmi-tasks-operating-systems"></a><span data-ttu-id="01be8-103">WMI 工作：作業系統</span><span class="sxs-lookup"><span data-stu-id="01be8-103">WMI Tasks: Operating Systems</span></span>

<span data-ttu-id="01be8-104">作業系統的 WMI 工作會取得作業系統的相關資訊，例如版本、是否已啟用，或已安裝的修補程式。</span><span class="sxs-lookup"><span data-stu-id="01be8-104">WMI tasks for operating systems obtain information about the operating system, such as version, whether it is activated, or which hotfixes are installed.</span></span>

<span data-ttu-id="01be8-105">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="01be8-105">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="01be8-106">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="01be8-106">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="01be8-107">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="01be8-107">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="01be8-108">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="01be8-108">**To run a script**</span></span>

1.  <span data-ttu-id="01be8-109">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="01be8-109">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="01be8-110">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="01be8-110">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="01be8-111">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="01be8-111">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="01be8-112">在命令提示字元中，輸入 **CScript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="01be8-112">Type **CScript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="01be8-113">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="01be8-113">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="01be8-114">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="01be8-114">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="01be8-115">依預設，CScript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="01be8-115">By default, CScript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="01be8-116">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="01be8-116">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="01be8-117">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="01be8-117">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="01be8-118">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="01be8-118">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01be8-119">如何…</span><span class="sxs-lookup"><span data-stu-id="01be8-119">How do I...</span></span></th>
<th><span data-ttu-id="01be8-120">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="01be8-120">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01be8-121">...判斷是否已在電腦上安裝 service pack？</span><span class="sxs-lookup"><span data-stu-id="01be8-121">...determine if a service pack has been installed on a computer?</span></span></td>
<td><span data-ttu-id="01be8-122">使用 <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> 類別，並檢查 <strong>ServicePackMajorVersion</strong> 和 <strong>ServicePackMinorVersion</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="01be8-122">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and check the value of the <strong>ServicePackMajorVersion</strong> and <strong>ServicePackMinorVersion</strong> properties.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01be8-123">VB</span><span class="sxs-lookup"><span data-stu-id="01be8-123">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.ServicePackMajorVersion & &quot;.&quot; & objOperatingSystem.ServicePackMinorVersion
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
<th><span data-ttu-id="01be8-124">PowerShell</span><span class="sxs-lookup"><span data-stu-id="01be8-124">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | `
   format-list ServicePackMajorVersion, ServicePackMinorVersion</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="01be8-125">...判斷作業系統安裝在電腦上的時間？</span><span class="sxs-lookup"><span data-stu-id="01be8-125">...determine when the operating system was installed on a computer?</span></span></td>
<td><p><span data-ttu-id="01be8-126">使用 <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> 類別和 <strong>InstallDate</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="01be8-126">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>InstallDate</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01be8-127">VB</span><span class="sxs-lookup"><span data-stu-id="01be8-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Install Date: &quot; & objOperatingSystem.InstallDate 
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
<th><span data-ttu-id="01be8-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="01be8-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list InstallDate</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01be8-129">...判斷電腦上安裝的 Windows 作業系統版本為何？</span><span class="sxs-lookup"><span data-stu-id="01be8-129">...determine which version of the Windows operating system is installed on a computer?</span></span></td>
<td><p><span data-ttu-id="01be8-130">使用 <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> 類別，並同時抓取 <strong>Name</strong> 和 <strong>Version</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="01be8-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and retrieve both the <strong>Name</strong> and <strong>Version</strong> properties.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01be8-131">VB</span><span class="sxs-lookup"><span data-stu-id="01be8-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.Caption & &quot;  &quot; & objOperatingSystem.Version
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
<th><span data-ttu-id="01be8-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="01be8-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list Caption, Version</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01be8-133">...判斷哪一個資料夾是電腦上 (% Windir% ) 的 Windows 資料夾？</span><span class="sxs-lookup"><span data-stu-id="01be8-133">...determine which folder is the Windows folder (%Windir%) on a computer?</span></span></td>
<td><p><span data-ttu-id="01be8-134">使用 <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> 類別，並檢查 <strong>WindowsDirectory</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="01be8-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and check the value of the <strong>WindowsDirectory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01be8-135">VB</span><span class="sxs-lookup"><span data-stu-id="01be8-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Windows Folder: &quot; & objOperatingSystem.WindowsDirectory
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
<th><span data-ttu-id="01be8-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="01be8-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list WindowsDirectory</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01be8-137">...判斷電腦上已安裝哪些修補程式？</span><span class="sxs-lookup"><span data-stu-id="01be8-137">...determine what hotfixes have been installed on a computer?</span></span></td>
<td><p><span data-ttu-id="01be8-138">使用 <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="01be8-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01be8-139">VB</span><span class="sxs-lookup"><span data-stu-id="01be8-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuickFixes = objWMIService.ExecQuery (&quot;Select * from Win32_QuickFixEngineering&quot;)
For Each objQuickFix in colQuickFixes
    Wscript.Echo &quot;Description: &quot; & objQuickFix.Description
    Wscript.Echo &quot;Hotfix ID: &quot; & objQuickFix.HotFixID
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
<th><span data-ttu-id="01be8-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="01be8-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_QuickFixEngineering -Namespace &quot;root\cimv2&quot; | format-list Description, HotFixIDs</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01be8-141">...判斷我是否需要在電腦上啟動作業系統？</span><span class="sxs-lookup"><span data-stu-id="01be8-141">...determine if I need to activate the operating system on a computer?</span></span></td>
<td><p><span data-ttu-id="01be8-142">使用 <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> 類別，並檢查 <strong>ActivationRequired</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="01be8-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> class and check the value of the <strong>ActivationRequired</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01be8-143">VB</span><span class="sxs-lookup"><span data-stu-id="01be8-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colWPA = objWMIService.ExecQuery (&quot;Select * from Win32_WindowsProductActivation&quot;)
For Each objWPA in colWPA
    Wscript.Echo &quot;Activation Required: &quot; & objWPA.ActivationRequired
    Wscript.Echo &quot;Remaining Evaluation Period: &quot; & objWPA.RemainingEvaluationPeriod
    Wscript.Echo &quot;Remaining Grace Period: &quot; & objWPA.RemainingGracePeriod
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
<th><span data-ttu-id="01be8-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="01be8-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_WindowsProductActivation -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | `
     format-list ActivationRequired, RemainingEvaluationPeriod, RemainingGracePeriod</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="01be8-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="01be8-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01be8-146">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="01be8-146">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="01be8-147">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="01be8-147">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="01be8-148">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="01be8-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

