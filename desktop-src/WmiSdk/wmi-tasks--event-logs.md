---
description: 事件記錄檔的 WMI 工作會從事件記錄檔取得事件資料，並執行備份或清除記錄檔等作業。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: f6d4e68e-d757-44aa-be74-3b26168626b8
ms.tgt_platform: multiple
title: WMI 工作：事件記錄
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fdcfe3f547e58fa60e552abad9867f8556fc8b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976823"
---
# <a name="wmi-tasks-event-logs"></a><span data-ttu-id="8c17f-104">WMI 工作：事件記錄</span><span class="sxs-lookup"><span data-stu-id="8c17f-104">WMI Tasks: Event Logs</span></span>

<span data-ttu-id="8c17f-105">事件記錄檔的 WMI 工作會從事件記錄檔取得事件資料，並執行備份或清除記錄檔等作業。</span><span class="sxs-lookup"><span data-stu-id="8c17f-105">WMI tasks for event logs obtain event data from event log files and perform operations like backing up or clearing log files.</span></span> <span data-ttu-id="8c17f-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="8c17f-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="8c17f-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="8c17f-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="8c17f-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17f-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="8c17f-109">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="8c17f-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="8c17f-110">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="8c17f-110">**To run a script**</span></span>

1.  <span data-ttu-id="8c17f-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="8c17f-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="8c17f-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="8c17f-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="8c17f-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="8c17f-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="8c17f-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="8c17f-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="8c17f-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="8c17f-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="8c17f-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="8c17f-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="8c17f-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="8c17f-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="8c17f-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="8c17f-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="8c17f-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="8c17f-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="8c17f-120">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="8c17f-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c17f-121">如何…</span><span class="sxs-lookup"><span data-stu-id="8c17f-121">How do I...</span></span></th>
<th><span data-ttu-id="8c17f-122">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="8c17f-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c17f-123">...取得安全性事件記錄檔的相關資訊？</span><span class="sxs-lookup"><span data-stu-id="8c17f-123">...retrieve information about the Security event log?</span></span></td>
<td><span data-ttu-id="8c17f-124">連接到<a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a>類別時，請包含<a href="privilege-constants.md">安全性</a>許可權。</span><span class="sxs-lookup"><span data-stu-id="8c17f-124">Include the <a href="privilege-constants.md">Security</a> privilege when connecting to the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class.</span></span> <span data-ttu-id="8c17f-125">如需詳細資訊，請參閱 <a href="executing-privileged-operations-using-vbscript.md">使用 VBScript 執行特殊許可權作業</a>。</span><span class="sxs-lookup"><span data-stu-id="8c17f-125">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c17f-126">VB</span><span class="sxs-lookup"><span data-stu-id="8c17f-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate,(Security)}!\\&quot; & _
        strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTEventLogFile &quot; _
        & &quot;Where LogFileName=&#39;Security&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
    Wscript.Echo &quot;Maximum Size: &quot; _
    &  objLogfile.MaxFileSize 
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
<th><span data-ttu-id="8c17f-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c17f-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;security&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    &quot;Record Number: &quot; + $objLogFile.NumberOfRecords
    &quot;Maximum Size: &quot; + $objLogFile.MaxFileSize
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c17f-128">...要備份事件記錄檔嗎？</span><span class="sxs-lookup"><span data-stu-id="8c17f-128">...back up an event log?</span></span></td>
<td><p><span data-ttu-id="8c17f-129">使用 <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> 類別和 <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="8c17f-129">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="8c17f-130">連接到 WMI 時，您可能需要包含 <a href="privilege-constants.md">備份</a> 許可權。</span><span class="sxs-lookup"><span data-stu-id="8c17f-130">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="8c17f-131">如需詳細資訊，請參閱 <a href="executing-privileged-operations-using-vbscript.md">使用 VBScript 執行特殊許可權作業</a>。</span><span class="sxs-lookup"><span data-stu-id="8c17f-131">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c17f-132">VB</span><span class="sxs-lookup"><span data-stu-id="8c17f-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    errBackupLog = objLogFile.BackupEventLog(&quot;c:\scripts\application.evt&quot;)
    WScript.Echo &quot;File saved as c:\scripts\applications.evt&quot;
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
<th><span data-ttu-id="8c17f-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c17f-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.BackupEventlog(&quot;c:\scripts\applications.evt&quot;)
    &quot;File saved as c:\scripts\applications.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c17f-134">...要多次備份事件記錄檔嗎？</span><span class="sxs-lookup"><span data-stu-id="8c17f-134">...back up an event log more than once?</span></span></td>
<td><p><span data-ttu-id="8c17f-135">使用 <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> 和 <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> 方法之前，請確定備份檔案具有唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c17f-135">Ensure that the backup file has a unique name before using the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="8c17f-136">作業系統不允許您覆寫現有的備份檔案;您必須移動備份檔案或將其重新命名，才能再次執行腳本。</span><span class="sxs-lookup"><span data-stu-id="8c17f-136">The operating system does not allow you to overwrite an existing backup file; you must either move the backup file or rename it before you can run the script again.</span></span> <span data-ttu-id="8c17f-137">連接到 WMI 時，您可能需要包含 <a href="privilege-constants.md">備份</a> 許可權。</span><span class="sxs-lookup"><span data-stu-id="8c17f-137">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="8c17f-138">如需詳細資訊，請參閱 <a href="executing-privileged-operations-using-vbscript.md">使用 VBScript 執行特殊許可權作業</a>。</span><span class="sxs-lookup"><span data-stu-id="8c17f-138">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c17f-139">VB</span><span class="sxs-lookup"><span data-stu-id="8c17f-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>dtmThisDay = Day(Date)
dtmThisMonth = Month(Date)
dtmThisYear = Year(Date)
strBackupName = dtmThisYear & &quot;_&quot; & dtmThisMonth & &quot;_&quot; & dtmThisDay
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.BackupEventLog(&quot;c:\scripts\&quot; & strBackupName & &quot;_application.evt&quot;)
    objLogFile.ClearEventLog()
    WScript.Echo &quot;File saved: &quot; & strBackupName & &quot;_application.evt&quot;
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
<th><span data-ttu-id="8c17f-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c17f-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$CurDate = Get-Date
$strBackupName = $curDate.Year.ToString() + &quot;_&quot; + $curDate.Month.ToString() + &quot;_&quot; + $CurDate.Day.ToString()

$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    $BackupFile = $objLogFile.BackupEventlog(&quot;c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;)
    &quot;File saved: c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c17f-141">...判斷事件記錄檔中的記錄數目？</span><span class="sxs-lookup"><span data-stu-id="8c17f-141">...determine the number of records in an event log?</span></span></td>
<td><p><span data-ttu-id="8c17f-142">使用 <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> 類別，並檢查 <strong>NumberOfRecords</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="8c17f-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and check the value of the <strong>NumberOfRecords</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c17f-143">VB</span><span class="sxs-lookup"><span data-stu-id="8c17f-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;System&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
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
<th><span data-ttu-id="8c17f-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c17f-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    $objLogFile.NumberOfRecords
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c17f-145">...要清除我的事件記錄檔嗎？</span><span class="sxs-lookup"><span data-stu-id="8c17f-145">...clear my event logs?</span></span></td>
<td><p><span data-ttu-id="8c17f-146">使用 <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> 類別和 <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="8c17f-146">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c17f-147">VB</span><span class="sxs-lookup"><span data-stu-id="8c17f-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup, Security)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.ClearEventLog()
    WScript.Echo &quot;Cleared application event log file&quot;
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
<th><span data-ttu-id="8c17f-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c17f-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.ClearEventlog()
    &quot;Cleared application event log file&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c17f-149">...要從事件記錄檔讀取事件嗎？</span><span class="sxs-lookup"><span data-stu-id="8c17f-149">...read events from the event logs?</span></span></td>
<td><p><span data-ttu-id="8c17f-150">使用 <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="8c17f-150">Use the <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c17f-151">VB</span><span class="sxs-lookup"><span data-stu-id="8c17f-151">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colLoggedEvents = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTLogEvent &quot; _
        & &quot;Where Logfile = &#39;System&#39;&quot;)
For Each objEvent in colLoggedEvents
    Wscript.Echo &quot;Category: &quot; & objEvent.Category & VBNewLine _
    & &quot;Computer Name: &quot; & objEvent.ComputerName & VBNewLine _
    & &quot;Event Code: &quot; & objEvent.EventCode & VBNewLine _
    & &quot;Message: &quot; & objEvent.Message & VBNewLine _
    & &quot;Record Number: &quot; & objEvent.RecordNumber & VBNewLine _
    & &quot;Source Name: &quot; & objEvent.SourceName & VBNewLine _
    & &quot;Time Written: &quot; & objEvent.TimeWritten & VBNewLine _
    & &quot;Event Type: &quot; & objEvent.Type & VBNewLine _
    & &quot;User: &quot; & objEvent.User
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
<th><span data-ttu-id="8c17f-152">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c17f-152">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTLogEvent -ComputerName $strComputer | Where-Object {$_.LogFile -eq &#39;System&#39;}

foreach ($objEvent in $colLoggedEvents) 
{ 
    &quot;Category: &quot; + $objEvent.Category
    &quot;Computer Name: &quot; + $objEvent.ComputerName
    &quot;Event Code: &quot; + $objEvent.EventCode
    &quot;Message: &quot; + $objEvent.Message
    &quot;Record Number: &quot; + $objEvent.RecordNumber
    &quot;Source Name: &quot; + $objEvent.SourceName
    &quot;Time Written: &quot; + $objEvent.TimeWritten
    &quot;Event Type: &quot; + $objEvent.Type
    &quot;User: &quot; + $objEvent.Use
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8c17f-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c17f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c17f-154">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="8c17f-154">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="8c17f-155">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="8c17f-155">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="8c17f-156">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="8c17f-156">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

