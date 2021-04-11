---
description: 桌面管理的 WMI 工作可以控制和取得遠端桌面或本機電腦的資料。
ms.assetid: bb8356bf-de38-4925-a501-6ad47d23ea8f
ms.tgt_platform: multiple
title: WMI 工作：桌面管理
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33f027c808a30463f2747d11020f45d1b8d40edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848736"
---
# <a name="wmi-tasks-desktop-management"></a><span data-ttu-id="207c8-103">WMI 工作：桌面管理</span><span class="sxs-lookup"><span data-stu-id="207c8-103">WMI Tasks: Desktop Management</span></span>

<span data-ttu-id="207c8-104">桌面管理的 WMI 工作可以控制和取得遠端桌面或本機電腦的資料。</span><span class="sxs-lookup"><span data-stu-id="207c8-104">WMI tasks for desktop management can exert control and obtain data from either a remote desktop or a local computer.</span></span> <span data-ttu-id="207c8-105">例如，您可以判斷本機電腦上的螢幕保護裝置是否需要密碼。</span><span class="sxs-lookup"><span data-stu-id="207c8-105">For example, you can determine whether the screensaver on a local computer requires a password.</span></span> <span data-ttu-id="207c8-106">WMI 也提供您關閉遠端電腦的能力。</span><span class="sxs-lookup"><span data-stu-id="207c8-106">WMI also gives you the ability shut down a remote computer.</span></span> <span data-ttu-id="207c8-107">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="207c8-107">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="207c8-108">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="207c8-108">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="207c8-109">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="207c8-109">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="207c8-110">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="207c8-110">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="207c8-111">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="207c8-111">**To run a script**</span></span>

1.  <span data-ttu-id="207c8-112">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="207c8-112">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="207c8-113">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="207c8-113">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="207c8-114">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="207c8-114">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="207c8-115">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="207c8-115">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="207c8-116">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="207c8-116">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="207c8-117">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="207c8-117">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="207c8-118">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="207c8-118">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="207c8-119">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="207c8-119">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="207c8-120">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="207c8-120">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="207c8-121">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="207c8-121">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="207c8-122">如何…</span><span class="sxs-lookup"><span data-stu-id="207c8-122">How do I...</span></span></th>
<th><span data-ttu-id="207c8-123">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="207c8-123">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="207c8-124">...判斷遠端電腦是否已在具有網路狀態的安全模式中啟動？</span><span class="sxs-lookup"><span data-stu-id="207c8-124">...determine if a remote computer has booted up in the Safe Mode with Networking state?</span></span></td>
<td><span data-ttu-id="207c8-125">使用 <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> 類別，並檢查 <strong>PrimaryOwnerName</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="207c8-125">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>PrimaryOwnerName</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="207c8-126">VB</span><span class="sxs-lookup"><span data-stu-id="207c8-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery (&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Registered owner: &quot; & objComputer.PrimaryOwnerName
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
<th><span data-ttu-id="207c8-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="207c8-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSettings = Get-WmiObject -Class Win32_ComputerSystem
foreach ($objComputer in $colSettings)
{
    &quot;System Name: &quot; + $objComputer.Name
    &quot;Registered owner: &quot; + $objComputer.PrimaryOwnerName
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="207c8-128">...判斷電腦螢幕保護裝置是否需要密碼？</span><span class="sxs-lookup"><span data-stu-id="207c8-128">...determine if a computer screensaver requires a password?</span></span></td>
<td><p><span data-ttu-id="207c8-129">使用 <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> 類別，並檢查 <strong>ScreenSaverSecure</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="207c8-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> class and check the value of the <strong>ScreenSaverSecure</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="207c8-130">VB</span><span class="sxs-lookup"><span data-stu-id="207c8-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Desktop&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Saver Secure: &quot; & objItem.ScreenSaverSecure
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
<th><span data-ttu-id="207c8-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="207c8-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$Desktops = Get-WMIObject -class Win32_Desktop -ComputerName $computer
&quot;{0} desktops found as follows&quot; -f $desktops.count
foreach ($desktop in $desktops) {
     &quot;Desktop      : {0}&quot;  -f $Desktop.Name
     &quot;Screen Saver : {0}&quot;  -f $desktop.ScreensaverExecutable
     &quot;Secure       : {0} &quot; -f $desktop.ScreenSaverSecure
     &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="207c8-132">...確認電腦螢幕是否已設定800圖元乘以600圖元？</span><span class="sxs-lookup"><span data-stu-id="207c8-132">...verify that a computer screen has been set for 800 pixels by 600 pixels?</span></span></td>
<td><p><span data-ttu-id="207c8-133">使用 <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> 類別，並檢查屬性的值 <strong>ScreenHeight</strong> 和 <strong>ScreenWidth</strong>。</span><span class="sxs-lookup"><span data-stu-id="207c8-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> class and check the values of the properties <strong>ScreenHeight</strong> and <strong>ScreenWidth</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="207c8-134">VB</span><span class="sxs-lookup"><span data-stu-id="207c8-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_DesktopMonitor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Height: &quot; & objItem.ScreenHeight
    Wscript.Echo &quot;Screen Width: &quot; & objItem.ScreenWidth
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
<th><span data-ttu-id="207c8-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="207c8-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><# Get desktop information #>
$computer = &quot;.&quot;
$desktops = Get-WmiObject -Class Win32_DesktopMonitor
$hostname = hostname

<span data-ttu-id="207c8-136">< # 顯示桌面詳細資料 # > &quot; 有 {0} 桌上型電腦開啟如下 {1} ： &quot; f $desktops。計數，$hostname &quot; &quot; $i = 1 # 此系統上的桌面計數</span><span class="sxs-lookup"><span data-stu-id="207c8-136"><# Display desktop details #> &quot;There are {0} Desktops on {1} as follows:&quot; -f $desktops.Count, $hostname &quot;&quot; $i=1 # count of desktops on this system</span></span>

<span data-ttu-id="207c8-137">foreach ($desktop $desktops) { &quot; desktop {0} ： {1} &quot; -f $i + +，$Desktop 標題 &quot; 螢幕高度： {0} &quot; -f $desktop。ScreenHeight &quot; 螢幕寬度： {0} &quot; -f $desktop。ScreenWidth &quot; &quot; }</code></span><span class="sxs-lookup"><span data-stu-id="207c8-137">foreach ($desktop in $desktops) { &quot;Desktop {0}: {1}&quot; -f  $i++, $Desktop.Caption &quot;Screen Height : {0}&quot; -f $desktop.ScreenHeight &quot;Screen Width  : {0}&quot; -f $desktop.ScreenWidth &quot;&quot; }</code></span></span></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="207c8-138">...判斷電腦執行的時間長度？</span><span class="sxs-lookup"><span data-stu-id="207c8-138">...determine how long a computer has been running?</span></span></td>
<td><p><span data-ttu-id="207c8-139">使用 <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> 類別和 <strong>LastBootUpTime</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="207c8-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>LastBootUpTime</strong> property.</span></span> <span data-ttu-id="207c8-140">從目前的時間減去該值，以取得系統執行時間。</span><span class="sxs-lookup"><span data-stu-id="207c8-140">Subtract that value from the current time to get the system uptime.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="207c8-141">VB</span><span class="sxs-lookup"><span data-stu-id="207c8-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
 
For Each objOS in colOperatingSystems
    dtmBootup = objOS.LastBootUpTime
    dtmLastBootUpTime = WMIDateStringToDate(dtmBootup)
    dtmSystemUptime = DateDiff(&quot;h&quot;, dtmLastBootUpTime, Now)
    Wscript.Echo dtmSystemUptime 
Next
 
Function WMIDateStringToDate(dtmBootup)
    WMIDateStringToDate =  CDate(Mid(dtmBootup, 5, 2) & &quot;/&quot; & _
        Mid(dtmBootup, 7, 2) & &quot;/&quot; & Left(dtmBootup, 4) & &quot; &quot; & Mid (dtmBootup, 9, 2) & &quot;:&quot; & _
        Mid(dtmBootup, 11, 2) & &quot;:&quot; & Mid(dtmBootup, 13, 2))
End Function</code></pre></td>
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
<th><span data-ttu-id="207c8-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="207c8-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDate($Bootup) {
[System.Management.ManagementDateTimeconverter]::ToDateTime($Bootup)
}

<# Main script #>
$Computer = &quot;.&quot; # adjust as needed
$computers = Get-WMIObject -class Win32_OperatingSystem -computer $computer

foreach ($system in $computers) {
    $Bootup = $system.LastBootUpTime
    $LastBootUpTime = WMIDateStringToDate($Bootup)
    $now = Get-Date
 $Uptime = $now-$lastBootUpTime
    &quot;System Up for: {0}&quot; -f $UpTime
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="207c8-143">...要重新開機或關閉遠端電腦嗎？</span><span class="sxs-lookup"><span data-stu-id="207c8-143">...reboot or shut down a remote computer?</span></span></td>
<td><p><span data-ttu-id="207c8-144">使用 <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="207c8-144">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> method.</span></span> <span data-ttu-id="207c8-145">連接到 WMI 時，您必須包含 <a href="privilege-constants.md">RemoteShutdown</a> 許可權。</span><span class="sxs-lookup"><span data-stu-id="207c8-145">You must include the <a href="privilege-constants.md">RemoteShutdown</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="207c8-146">如需詳細資訊，請參閱 <a href="executing-privileged-operations-using-vbscript.md">使用 VBScript 執行特殊許可權作業</a>。</span><span class="sxs-lookup"><span data-stu-id="207c8-146">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span> <span data-ttu-id="207c8-147">與<strong>Win32_OperatingSystem</strong>上的<a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>shutdown</strong></a>方法不同的是， <strong>Win32Shutdown</strong>方法可讓您設定旗標來控制關機行為。</span><span class="sxs-lookup"><span data-stu-id="207c8-147">Unlike the <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> method on <strong>Win32_OperatingSystem</strong>, the <strong>Win32Shutdown</strong> method allows you to set flags to control the shutdown behavior.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="207c8-148">VB</span><span class="sxs-lookup"><span data-stu-id="207c8-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Shutdown)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    ObjOperatingSystem.Shutdown(1)
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
<th><span data-ttu-id="207c8-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="207c8-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
$colOperatingSystem = Get-WmiObject -Class Win32_OperatingSystem -ComputerName $strComputer -Namespace &quot;wmi\cimv2&quot;
foreach ($objOperatingSystem in $colOperatingSystem)
{
    [void]$objOperatingSystem.Shutdown()
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="207c8-150">...判斷每次啟動 Windows 時，會自動執行哪些應用程式？</span><span class="sxs-lookup"><span data-stu-id="207c8-150">...determine what applications automatically run each time I start Windows?</span></span></td>
<td><p><span data-ttu-id="207c8-151">使用 <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="207c8-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="207c8-152">VB</span><span class="sxs-lookup"><span data-stu-id="207c8-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colStartupCommands = objWMIService.ExecQuery _
    (&quot;Select * from Win32_StartupCommand&quot;)
For Each objStartupCommand in colStartupCommands
    Wscript.Echo &quot;Command: &quot; & objStartupCommand.Command & VBNewLine _
    & &quot;Description: &quot; & objStartupCommand.Description & VBNewLine _
    & &quot;Location: &quot; & objStartupCommand.Location & VBNewLine _
    & &quot;Name: &quot; & objStartupCommand.Name & VBNewLine _
    & &quot;SettingID: &quot; & objStartupCommand.SettingID & VBNewLine _
    & &quot;User: &quot; & objStartupCommand.User
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
<th><span data-ttu-id="207c8-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="207c8-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_StartupCommand -ComputerName $strComputer
foreach ($objStartupCommand in $colItems) 
{ 
    &quot;Command: &quot; + $objStartupCommand.Command
    &quot;Description: &quot; + $objStartupCommand.Description 
    &quot;Location: &quot; + $objStartupCommand.Location 
    &quot;Name: &quot; + $objStartupCommand.Name 
    &quot;SettingID: &quot; + $objStartupCommand.SettingID 
    &quot;User: &quot; + $objStartupCommand.User
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="207c8-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="207c8-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="207c8-155">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="207c8-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="207c8-156">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="207c8-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="207c8-157">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="207c8-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

