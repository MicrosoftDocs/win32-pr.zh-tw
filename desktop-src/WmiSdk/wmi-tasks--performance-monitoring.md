---
description: 使用從效能計數器取得資料的 WMI 類別，存取和重新整理有關電腦效能的資料。
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: WMI 工作：效能監視
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbb254e14280bec5a928bdc32aaa9a3e03c7a4f4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "107000641"
---
# <a name="wmi-tasks-performance-monitoring"></a><span data-ttu-id="91427-103">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="91427-103">WMI Tasks: Performance Monitoring</span></span>

<span data-ttu-id="91427-104">使用從效能計數器取得資料的 WMI 類別，存取和重新整理有關電腦效能的資料。</span><span class="sxs-lookup"><span data-stu-id="91427-104">Use the WMI classes that obtain data from performance counters to access and refresh data about computer performance.</span></span> <span data-ttu-id="91427-105">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="91427-105">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span> <span data-ttu-id="91427-106">如需詳細資訊，請參閱 [效能程式庫和 WMI](performance-libraries-and-wmi.md) 和 [監視效能資料](monitoring-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="91427-106">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

<span data-ttu-id="91427-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="91427-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="91427-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="91427-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="91427-109">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="91427-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="91427-110">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="91427-110">**To run a script**</span></span>

1.  <span data-ttu-id="91427-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="91427-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="91427-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="91427-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="91427-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="91427-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="91427-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="91427-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="91427-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="91427-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="91427-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="91427-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="91427-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="91427-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="91427-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="91427-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="91427-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="91427-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="91427-120">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="91427-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91427-121">如何…</span><span class="sxs-lookup"><span data-stu-id="91427-121">How do I...</span></span></th>
<th><span data-ttu-id="91427-122">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="91427-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91427-123">...取得我可以在腳本的 Perfmon 公用程式中看到的效能計數器資料嗎？</span><span class="sxs-lookup"><span data-stu-id="91427-123">...obtain the performance counter data that I can see in the Perfmon utility in a script?</span></span></td>
<td><span data-ttu-id="91427-124">使用名稱以 Win32_PerfFormattedData 開頭的類別 &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes"></a> &quot; ，例如<a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="91427-124">Use classes that have names that begin with &quot;<a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>&quot;, for example <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="91427-125">名稱類似 <strong>PageFileBytes</strong> 的屬性會對應到您在 Perfmon 中看到的效能計數器。</span><span class="sxs-lookup"><span data-stu-id="91427-125">Properties with names like <strong>PageFileBytes</strong> correspond to performance counters you see in Perfmon.</span></span> <span data-ttu-id="91427-126">&quot;Win32_PerfFormattedData &quot; 類別會為您計算計數器的最終值。</span><span class="sxs-lookup"><span data-stu-id="91427-126">The &quot;Win32_PerfFormattedData&quot; classes calculate the final values of counters for you.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91427-127">...取得單一進程、磁片磁碟機和其他資料的持續效能資料嗎？</span><span class="sxs-lookup"><span data-stu-id="91427-127">...get on-going performance data for a single process, disk drive, and other data?</span></span></td>
<td><span data-ttu-id="91427-128">使用 <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> 或適當的格式化 <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">效能計數器類別</a> 和 <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="91427-128">Use the <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> or the appropriate formatted <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Performance Counter Class</a> and the <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> method.</span></span> <span data-ttu-id="91427-129">如需詳細資訊，請參閱 <a href="scripting-with-swbemobject.md">使用 SWbemObject 編寫腳本</a>。</span><span class="sxs-lookup"><span data-stu-id="91427-129">For more information, see <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.</span></span><br/> <span data-ttu-id="91427-130">在 c + + 中，請使用 <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher：： AddObjectByPath</strong></a> 和 <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher：： Refresh</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="91427-130">In C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> and <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>.</span></span> <span data-ttu-id="91427-131">如需詳細資訊，請參閱 <a href="monitoring-performance-data.md">監視效能資料</a>。</span><span class="sxs-lookup"><span data-stu-id="91427-131">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span><br/> <span data-ttu-id="91427-132">下列腳本會在電腦重新開機、WMI 已停止或腳本停止之前執行。</span><span class="sxs-lookup"><span data-stu-id="91427-132">The following script runs until the computer is restarted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="91427-133">若要手動停止腳本，請使用工作管理員停止進程。</span><span class="sxs-lookup"><span data-stu-id="91427-133">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="91427-134">若要以程式設計方式停止它，請使用<a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a>類別中的<a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a>方法。</span><span class="sxs-lookup"><span data-stu-id="91427-134">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91427-135">VB</span><span class="sxs-lookup"><span data-stu-id="91427-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set PerfProcess = objWMIService.Get(_
    &quot;Win32_PerfFormattedData_PerfProc_Process.Name=&#39;Idle&#39;&quot;)

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91427-136">...取得所有進程的持續效能資料，而不重複輪詢？</span><span class="sxs-lookup"><span data-stu-id="91427-136">...get on-going performance data for all processes without repeated polling?</span></span></td>
<td><p><span data-ttu-id="91427-137">使用名稱開頭為 &quot; Win32_PerfFormattedData &quot; 和 <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> 物件的類別。</span><span class="sxs-lookup"><span data-stu-id="91427-137">Use classes that have names that begin with &quot;Win32_PerfFormattedData&quot; and an <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> object.</span></span> <span data-ttu-id="91427-138">複習器會保存物件，因此您不需要重複取得集合。</span><span class="sxs-lookup"><span data-stu-id="91427-138">The refresher holds the objects so you do not need to get the collection repeatedly.</span></span> <span data-ttu-id="91427-139">需要最少兩個值來計算效能資料，因為大部分的計數器都是速率計數器。</span><span class="sxs-lookup"><span data-stu-id="91427-139">A minimum of two values are needed to calculate performance data because most counters are rate counters.</span></span> <span data-ttu-id="91427-140">當您第一次顯示重新整理程式資料時，它會是空的。</span><span class="sxs-lookup"><span data-stu-id="91427-140">The first time you display the refresher data it is empty.</span></span></p>
<p><span data-ttu-id="91427-141">下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。</span><span class="sxs-lookup"><span data-stu-id="91427-141">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="91427-142">若要手動停止腳本，請使用工作管理員停止進程。</span><span class="sxs-lookup"><span data-stu-id="91427-142">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="91427-143">若要以程式設計方式停止它，請使用<a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a>類別中的<a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a>方法。</span><span class="sxs-lookup"><span data-stu-id="91427-143">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91427-144">VB</span><span class="sxs-lookup"><span data-stu-id="91427-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set objRefresher = CreateObject(&quot;WbemScripting.Swbemrefresher&quot;)
Set objProcessor = objRefresher.AddEnum _
    (objWMIService, _
    &quot;Win32_PerfFormattedData_PerfOS_Processor&quot;).ObjectSet

While (True)
    objRefresher.Refresh
        For each RefreshItem in objRefresher
            For each objProcess in RefreshItem.ObjectSet
                Wscript.Echo objProcess.GetObjectText_
            Next
        Next
     Wscript.Sleep 5000
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91427-145">...取得和計算 Windows 2000 上進程的效能資料嗎？</span><span class="sxs-lookup"><span data-stu-id="91427-145">...get and calculate performance data for processes on Windows 2000?</span></span></td>
<td><p><span data-ttu-id="91427-146">使用 &quot; Win32_PerfRawData &quot; 類別，例如 <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="91427-146">Use the &quot;Win32_PerfRawData&quot; classes, such as <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="91427-147">取得特定進程的屬性資料，例如 <strong>PercentProcessorTime</strong>、兩次。</span><span class="sxs-lookup"><span data-stu-id="91427-147">Get the property data, such as <strong>PercentProcessorTime</strong>, twice for a specific process.</span></span> <span data-ttu-id="91427-148">查閱 <a href="countertype-qualifier.md"><strong>CounterType</strong></a> 限定詞中針對屬性指定的公式，然後計算。</span><span class="sxs-lookup"><span data-stu-id="91427-148">Look up the formula specified in the <a href="countertype-qualifier.md"><strong>CounterType</strong></a> qualifier for the property and calculate.</span></span> <span data-ttu-id="91427-149">範例中的 CounterType 是 <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>。</span><span class="sxs-lookup"><span data-stu-id="91427-149">The CounterType in the example is <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span></span> <span data-ttu-id="91427-150">如需詳細資訊，請參閱 <a href="monitoring-performance-data.md">監視效能資料</a>。</span><span class="sxs-lookup"><span data-stu-id="91427-150">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span></p>
<p><span data-ttu-id="91427-151">下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。</span><span class="sxs-lookup"><span data-stu-id="91427-151">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="91427-152">若要手動停止腳本，請使用工作管理員停止進程。</span><span class="sxs-lookup"><span data-stu-id="91427-152">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="91427-153">若要以程式設計方式停止它，請使用<a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a>類別中的<a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a>方法。</span><span class="sxs-lookup"><span data-stu-id="91427-153">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91427-154">VB</span><span class="sxs-lookup"><span data-stu-id="91427-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)

While (True)
    Set object1 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N1 = object1.PercentProcessorTime
    D1 = object1.TimeStamp_Sys100NS
    Wscript.Sleep(1000)
    set object2 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N2 = object2.PercentProcessorTime
    D2 = object2.TimeStamp_Sys100NS
    &#39; CounterType - PERF_100NSEC_TIMER_INV
    &#39; Formula - (1- ((N2 - N1) / (D2 - D1))) x 100
    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    Wscript.Echo &quot;% Processor Time=&quot; , PercentProcessorTime
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="91427-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="91427-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91427-156">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="91427-156">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="91427-157">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="91427-157">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="91427-158">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="91427-158">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
