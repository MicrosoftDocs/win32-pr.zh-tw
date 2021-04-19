---
description: 磁片和檔案系統的 WMI 工作會取得磁片磁碟機硬體狀態和邏輯磁片區的相關資訊。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: d310e5e6-3b67-41bc-b5f2-cea33d0a7a2b
ms.tgt_platform: multiple
title: WMI 工作：磁碟和檔案系統
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0357a91d893120ec1bb72a7c1d54ad4a5e9a0acf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106985921"
---
# <a name="wmi-tasks-disks-and-file-systems"></a><span data-ttu-id="0ec31-104">WMI 工作：磁碟和檔案系統</span><span class="sxs-lookup"><span data-stu-id="0ec31-104">WMI Tasks: Disks and File Systems</span></span>

<span data-ttu-id="0ec31-105">磁片和檔案系統的 WMI 工作會取得磁片磁碟機硬體狀態和邏輯磁片區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ec31-105">WMI tasks for disks and file systems obtain information about disk drive hardware state and logical volumes.</span></span> <span data-ttu-id="0ec31-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="0ec31-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="0ec31-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="0ec31-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="0ec31-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="0ec31-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="0ec31-109">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="0ec31-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="0ec31-110">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="0ec31-110">**To run a script**</span></span>

1.  <span data-ttu-id="0ec31-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="0ec31-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="0ec31-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="0ec31-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="0ec31-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="0ec31-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="0ec31-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="0ec31-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="0ec31-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="0ec31-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="0ec31-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="0ec31-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="0ec31-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="0ec31-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="0ec31-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="0ec31-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="0ec31-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="0ec31-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="0ec31-120">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="0ec31-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-121">如何…</span><span class="sxs-lookup"><span data-stu-id="0ec31-121">How do I...</span></span></th>
<th><span data-ttu-id="0ec31-122">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="0ec31-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ec31-123">...找出電腦上每位使用者目前使用多少磁碟空間？</span><span class="sxs-lookup"><span data-stu-id="0ec31-123">...find out how much disk space each user is currently using on a computer?</span></span></td>
<td><span data-ttu-id="0ec31-124">如果您使用的是磁片配額，請使用 <a href="/previous-versions/windows/desktop/wmipdskq/win32-diskquota"><strong>Win32_DiskQuota</strong></a> 類別，並取出 <strong>使用者</strong> 和 <strong>DiskSpaceUsed</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0ec31-124">If you are using disk quotas, then use the <a href="/previous-versions/windows/desktop/wmipdskq/win32-diskquota"><strong>Win32_DiskQuota</strong></a> class and retrieve the values of the <strong>User</strong> and <strong>DiskSpaceUsed</strong> properties.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-125">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuotas = objWMIService.ExecQuery (&quot;Select * from Win32_DiskQuota&quot;)
For each objQuota in colQuotas
    Wscript.Echo &quot;Volume: &quot;& vbTab &  objQuota.QuotaVolume
    Wscript.Echo &quot;User: &quot;& vbTab &  objQuota.User      
    Wscript.Echo &quot;Disk Space Used: &quot; & vbTab &  objQuota.DiskSpaceUsed
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
<th><span data-ttu-id="0ec31-126">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0ec31-126">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_DiskQuota -ComputerName $strComputer
foreach ($objQuota in $colItems) 
{ 
    &quot;Volume: &quot; + $objQuota.QuotaVolume
    &quot;User: &quot; + $objQuota.User      
    &quot;Disk Space Used: &quot; + $objQuota.DiskSpaceUsed
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ec31-127">...判斷何時已在電腦上新增或移除卸載式磁片磁碟機？</span><span class="sxs-lookup"><span data-stu-id="0ec31-127">...determine when a removable drive has been added to or removed from a computer?</span></span></td>
<td><p><span data-ttu-id="0ec31-128">使用查詢 <a href="/windows/desktop/CIMWin32Prov/win32-volumechangeevent"><strong>Win32_VolumeChangeEvent</strong></a> 類別的監視腳本。</span><span class="sxs-lookup"><span data-stu-id="0ec31-128">Use a monitoring script that queries the <a href="/windows/desktop/CIMWin32Prov/win32-volumechangeevent"><strong>Win32_VolumeChangeEvent</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-129">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-129">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colMonitoredEvents = objWMIService. ExecNotificationQuery( &quot;Select * from Win32_VolumeChangeEvent&quot;)
Do
    Set objLatestEvent = colMonitoredEvents.NextEvent
    Wscript.Echo objLatestEvent.DriveName
    Wscript.Echo objLatestEvent.EventType
    Wscript.Echo objLatestEvent.Time_Created
Loop</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ec31-130">...判斷 cd 是否在 cd-rom 光碟機中？</span><span class="sxs-lookup"><span data-stu-id="0ec31-130">...determine if a CD is in a CD-ROM drive?</span></span></td>
<td><p><span data-ttu-id="0ec31-131">使用 <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> 類別和 <strong>MediaLoaded</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec31-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> class and the <strong>MediaLoaded</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-132">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery( &quot;Select * from Win32_CDROMDrive&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Media Loaded: &quot; & objItem.MediaLoaded
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
<th><span data-ttu-id="0ec31-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0ec31-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_CDROMDrive -ComputerName $strComputer
foreach ($objItem in $colItems)
{
    &quot;Device ID: &quot; + $objItem.DeviceID
    &quot;MediaLoaded: &quot; + $objItem.MediaLoaded
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ec31-134">...判斷磁片磁碟機中是否有磁片？</span><span class="sxs-lookup"><span data-stu-id="0ec31-134">...determine if a disk is in the floppy drive?</span></span></td>
<td><p><span data-ttu-id="0ec31-135">使用 <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> 類別，並檢查 [ <strong>可用空間</strong> ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec31-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and check the <strong>FreeSpace</strong> property.</span></span> <span data-ttu-id="0ec31-136">如果值為 Null，則磁片磁碟機中沒有任何磁片。</span><span class="sxs-lookup"><span data-stu-id="0ec31-136">If the value is Null, then no disk is in the drive.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-137">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-137">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery (&quot;Select * From Win32_LogicalDisk Where DeviceID = &#39;A:&#39;&quot;)

For Each objItem in colItems
    intFreeSpace = objItem.FreeSpace
    If IsNull(intFreeSpace) Then
        Wscript.Echo &quot;There is no disk in the floppy drive.&quot;
    Else
        Wscript.Echo &quot;There is a disk in the floppy drive.&quot;
    End If
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
<th><span data-ttu-id="0ec31-138">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0ec31-138">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_LogicalDisk -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
    Where-Object { $_.DeviceID -eq &quot;A:&quot; }

foreach ($objItem in $colItems)
{
    $intFreeSpace = $objItem.FreeSpace
    if ($intFreeSpace -eq $null) { &quot;There is no disk in the floppy drive.&quot; }
    else { &quot;There is a disk in the floppy drive.&quot; }
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ec31-139">...要區別固定硬碟和可移動硬碟嗎？</span><span class="sxs-lookup"><span data-stu-id="0ec31-139">...distinguish between a fixed hard disk and a removable hard disk?</span></span></td>
<td><p><span data-ttu-id="0ec31-140">使用 <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> 類別，並檢查 <strong>DriveType</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0ec31-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and check the value of the <strong>DriveType</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-141">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery _
    (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot;& vbTab _
        &  objDisk.DeviceID       
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo &quot;No root directory. &quot; & &quot;Drive type could not be &quot; & &quot;determined.&quot;
        Case 2
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Removable drive.&quot;
        Case 3
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Local hard disk.&quot;
        Case 4
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Network disk.&quot;      
        Case 5
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Compact disk.&quot;      
        Case 6
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;RAM disk.&quot;   
        Case Else
            Wscript.Echo &quot;Drive type could not be&quot; & &quot; determined.&quot;
    End Select
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
<th><span data-ttu-id="0ec31-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0ec31-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colDisks = Get-WmiObject -Class Win32_LogicalDisk -ComputerName $strComputer 

foreach ($objDisk in $colDisks)
{
    &quot;DeviceID: &quot; + $objDisk.deviceID
    switch ($objDisk.DriveType)
    {
        &#39;1&#39; { &quot;No root directory. Drive type could not be determined.&quot; }
        &#39;2&#39; { &quot;DriveType: Removable drive.&quot; }
        &#39;3&#39; { &quot;DriveType: Local hard disk.&quot; }
        &#39;4&#39; { &quot;DriveType: Network disk.&quot; }
        &#39;5&#39; { &quot;DriveType: Compact disk.&quot; }
        &#39;6&#39; { &quot;DriveType: RAM disk.&quot; }
        default: { &quot;Drive type could not be determined.&quot; }
    }
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ec31-143">...判斷磁片磁碟機上使用的檔案系統為何？</span><span class="sxs-lookup"><span data-stu-id="0ec31-143">...determine what file system is in use on a drive?</span></span></td>
<td><p><span data-ttu-id="0ec31-144">使用 <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> 類別和 <strong>FileSystem</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec31-144">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and the <strong>FileSystem</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-145">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-145">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;File System: &quot; & objDisk.FileSystem
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ec31-146">...判斷磁片磁碟機上有多少可用空間？</span><span class="sxs-lookup"><span data-stu-id="0ec31-146">...determine how much free space is available on a drive?</span></span></td>
<td><p><span data-ttu-id="0ec31-147">使用 <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> 類別和 [ <strong>可用空間</strong> ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec31-147">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and the <strong>FreeSpace</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-148">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;Free Disk Space: &quot; & objDisk.FreeSpace
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ec31-149">...決定磁片磁碟機的大小嗎？</span><span class="sxs-lookup"><span data-stu-id="0ec31-149">...determine the size of a drive?</span></span></td>
<td><p><span data-ttu-id="0ec31-150">使用 <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> 類別和 <strong>Size</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec31-150">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class, and the <strong>Size</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-151">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-151">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;Disk Size: &quot; & objDisk.Size
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ec31-152">...找出電腦上對應的磁片磁碟機有哪些？</span><span class="sxs-lookup"><span data-stu-id="0ec31-152">...find out what drives are mapped on a computer?</span></span></td>
<td><p><span data-ttu-id="0ec31-153">使用 <a href="/windows/desktop/CIMWin32Prov/win32-mappedlogicaldisk"><strong>Win32_MappedLogicalDisk</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="0ec31-153">Use the <a href="/windows/desktop/CIMWin32Prov/win32-mappedlogicaldisk"><strong>Win32_MappedLogicalDisk</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-154">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService. ExecQuery(&quot;Select * from Win32_MappedLogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;Device ID: &quot; & objDisk.DeviceID
    Wscript.Echo &quot;Name: &quot; & objDisk.Name
    Wscript.Echo &quot;Free Space: &quot; & objDisk.FreeSpace
    Wscript.Echo &quot;Size: &quot; & objDisk.Size
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ec31-155">...重組硬碟？</span><span class="sxs-lookup"><span data-stu-id="0ec31-155">...defragment a hard disk?</span></span></td>
<td><p><span data-ttu-id="0ec31-156">使用 <a href="/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)"><strong>Win32_Volume</strong></a> 類別和 <a href="/previous-versions/windows/desktop/vdswmi/defrag-method-in-class-win32-volume"><strong>Defrag</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="0ec31-156">Use the <a href="/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)"><strong>Win32_Volume</strong></a> class and the <a href="/previous-versions/windows/desktop/vdswmi/defrag-method-in-class-win32-volume"><strong>Defrag</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-157">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colVolumes = objWMIService.ExecQuery (&quot;Select * from Win32_Volume Where Name = &#39;K:\\&#39;&quot;)
For Each objVolume in colVolumes
     errResult = objVolume.Defrag()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ec31-158">...偵測哪個磁碟機號與邏輯磁碟分割相關聯？</span><span class="sxs-lookup"><span data-stu-id="0ec31-158">...detect which drive letter is associated with a logical disk partition?</span></span></td>
<td><ol>
<li><span data-ttu-id="0ec31-159">從<a href="/windows/desktop/CIMWin32Prov/win32-diskdrive"><strong>Win32_DiskDrive</strong></a>類別開始，然後使用<strong>DeviceID</strong>屬性和<a href="/windows/desktop/CIMWin32Prov/win32-diskdrivetodiskpartition"><strong>Win32_DiskDriveToDiskPartition</strong></a>關聯類別來查詢<a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition</strong></a>的實例。</span><span class="sxs-lookup"><span data-stu-id="0ec31-159">Start with the <a href="/windows/desktop/CIMWin32Prov/win32-diskdrive"><strong>Win32_DiskDrive</strong></a> class and query for instances of <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition</strong></a> using the <strong>DeviceID</strong> property and the <a href="/windows/desktop/CIMWin32Prov/win32-diskdrivetodiskpartition"><strong>Win32_DiskDriveToDiskPartition</strong></a> association class.</span></span> <span data-ttu-id="0ec31-160">您現在已有實體磁片磁碟機上的磁碟分割集合。</span><span class="sxs-lookup"><span data-stu-id="0ec31-160">Now you have a collection of the partitions on the physical drive.</span></span></li>
<li><span data-ttu-id="0ec31-161">使用<a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition DeviceID</strong></a>屬性和<a href="/windows/desktop/CIMWin32Prov/win32-logicaldisktopartition"><strong>Win32_LogicalDiskToPartition</strong></a>關聯類別來查詢表示資料分割的<a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="0ec31-161">Query for the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> that represents the partition using the <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition.DeviceID</strong></a> property and <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisktopartition"><strong>Win32_LogicalDiskToPartition</strong></a> association class.</span></span></li>
<li><span data-ttu-id="0ec31-162">從 <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a>取得磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="0ec31-162">Get the drive letter from the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk.DeviceID</strong></a>.</span></span></li>
</ol>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec31-163">VB</span><span class="sxs-lookup"><span data-stu-id="0ec31-163">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>ComputerName = &quot;.&quot;
Set wmiServices  = GetObject ( _
    &quot;winmgmts:{impersonationLevel=Impersonate}!//&quot; & ComputerName)
&#39; Get physical disk drive
Set wmiDiskDrives =  wmiServices.ExecQuery ( &quot;SELECT Caption, DeviceID FROM Win32_DiskDrive&quot;)

For Each wmiDiskDrive In wmiDiskDrives
    WScript.Echo &quot;Disk drive Caption: &quot; & wmiDiskDrive.Caption & VbNewLine & &quot;DeviceID: &quot; & &quot; (&quot; & wmiDiskDrive.DeviceID & &quot;)&quot;

&#39;Use the disk drive device id to
&#39; find associated partition
query = &quot;ASSOCIATORS OF {Win32_DiskDrive.DeviceID=&#39;&quot; _
        & wmiDiskDrive.DeviceID & &quot;&#39;} WHERE AssocClass = Win32_DiskDriveToDiskPartition&quot;    
Set wmiDiskPartitions = wmiServices.ExecQuery(query)

For Each wmiDiskPartition In wmiDiskPartitions
    &#39;Use partition device id to find logical disk
    Set wmiLogicalDisks = wmiServices.ExecQuery _
        (&quot;ASSOCIATORS OF {Win32_DiskPartition.DeviceID=&#39;&quot; _
             & wmiDiskPartition.DeviceID & &quot;&#39;} WHERE AssocClass = Win32_LogicalDiskToPartition&quot;)

For Each wmiLogicalDisk In wmiLogicalDisks
    WScript.Echo &quot;Drive letter associated&quot; _
        & &quot; with disk drive = &quot; _ 
        & wmiDiskDrive.Caption _
        & wmiDiskDrive.DeviceID _
        & VbNewLine & &quot; Partition = &quot; _
        & wmiDiskPartition.DeviceID _
        & VbNewLine & &quot; is &quot; _
        & wmiLogicalDisk.DeviceID
    Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0ec31-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ec31-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ec31-165">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="0ec31-165">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="0ec31-166">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="0ec31-166">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="0ec31-167">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="0ec31-167">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
