---
description: WMI 排程工作會建立並取得已排程工作的相關資訊。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: WMI 工作：已排程的工作
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4051df4348ee47710b5d2d1f5dcc3f59f607d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987471"
---
# <a name="wmi-tasks-scheduled-tasks"></a><span data-ttu-id="c230d-104">WMI 工作：已排程的工作</span><span class="sxs-lookup"><span data-stu-id="c230d-104">WMI Tasks: Scheduled Tasks</span></span>

<span data-ttu-id="c230d-105">WMI 排程工作會建立並取得已排程工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c230d-105">WMI scheduled tasks create and get information about scheduled tasks.</span></span> <span data-ttu-id="c230d-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="c230d-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="c230d-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="c230d-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="c230d-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="c230d-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="c230d-109">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="c230d-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="c230d-110">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="c230d-110">**To run a script**</span></span>

1.  <span data-ttu-id="c230d-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="c230d-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="c230d-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="c230d-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="c230d-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="c230d-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="c230d-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="c230d-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="c230d-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="c230d-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="c230d-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="c230d-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="c230d-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="c230d-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="c230d-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="c230d-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="c230d-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="c230d-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="c230d-120">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="c230d-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c230d-121">如何…</span><span class="sxs-lookup"><span data-stu-id="c230d-121">How do I...</span></span></th>
<th><span data-ttu-id="c230d-122">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="c230d-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c230d-123">...使用腳本建立排定的工作？</span><span class="sxs-lookup"><span data-stu-id="c230d-123">...create scheduled tasks using scripts?</span></span></td>
<td><span data-ttu-id="c230d-124">使用 <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="c230d-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method.</span></span> <span data-ttu-id="c230d-125">如果您在 Windows 7 或更新版本上進行這項工作時遇到困難，請參閱 <strong>Win32_ScheduledJob</strong> 備註一節。您的設定可能會導致您無法使用類別。</span><span class="sxs-lookup"><span data-stu-id="c230d-125">If you are having difficulty making this task work on Windows 7 or later, see the <strong>Win32_ScheduledJob</strong> Remarks section; likely your settings are preventing you from using the class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c230d-126">VB</span><span class="sxs-lookup"><span data-stu-id="c230d-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="c230d-127">在 &quot; Create 方法) 的 StartTime 參數值中使用的字串 \* \* \* \* \* \* \* 143000.000000-420 (中，\* \* \* \* \* \* \* \* &quot; <em></em> <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong></strong></a> &quot; 143000.000000 &quot; 指定工作從 14.30 (2:30 P.M. 開始 ) 和 &quot; -420 &quot; 則指定時區。</span><span class="sxs-lookup"><span data-stu-id="c230d-127">In the string &quot;\*\*\*\*\*\*\*\*143000.000000-420&quot; (used in the <em>StartTime</em> parameter value of the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method), &quot;\*\*\*\*\*\*\*\*143000.000000&quot; specifies that the task starts at 14.30 (2:30 P.M.) and &quot;-420&quot; specifies the time zone.</span></span> <span data-ttu-id="c230d-128">時區號碼是本地時間轉譯的目前偏差。</span><span class="sxs-lookup"><span data-stu-id="c230d-128">The time zone number is the current bias of the local time translation.</span></span> <span data-ttu-id="c230d-129">偏差是 UTC 時間與當地時間之間的差異。</span><span class="sxs-lookup"><span data-stu-id="c230d-129">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="c230d-130">若要計算時區的偏差，請將您時區提前或晚于格林威治標準時間的小時數乘以60的 (GMT)  (如果您的時區是在 GMT 之前，則以小時為單位，如果您的時區晚于 gmt) ，則為負數。</span><span class="sxs-lookup"><span data-stu-id="c230d-130">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="c230d-131">如果您的時區使用日光節約時間，請在您的計算中加入額外的60。</span><span class="sxs-lookup"><span data-stu-id="c230d-131">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="c230d-132">例如，太平洋標準時區是 GMT 後八小時，因此偏差等於-420 (-8 \* 60 + 60) 當日光節約時間正在使用中，且當日光節約時間未使用時，則為-480 (-8 \* 60) 。</span><span class="sxs-lookup"><span data-stu-id="c230d-132">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="c230d-133">您也可以藉由查詢 <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> 類別的偏差屬性來判斷偏差的值。</span><span class="sxs-lookup"><span data-stu-id="c230d-133">You can also determine the value of the bias by querying the bias property of the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c230d-134">...傳回電腦上所有排程工作的清單嗎？</span><span class="sxs-lookup"><span data-stu-id="c230d-134">...return a list of all the scheduled tasks on a computer?</span></span></td>
<td><p><span data-ttu-id="c230d-135">使用 <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="c230d-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class.</span></span> <span data-ttu-id="c230d-136">請注意，這個類別只能傳回使用腳本或 AT.exe 所建立的工作。</span><span class="sxs-lookup"><span data-stu-id="c230d-136">Note that this class can only return jobs that are created using either a script or AT.exe.</span></span> <span data-ttu-id="c230d-137">它無法傳回排程工作 wizard 所建立或修改之作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c230d-137">It cannot return information about jobs that are either created by or modified by the Scheduled Task wizard.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c230d-138">VB</span><span class="sxs-lookup"><span data-stu-id="c230d-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c230d-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="c230d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c230d-140">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="c230d-140">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="c230d-141">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="c230d-141">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="c230d-142">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="c230d-142">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

