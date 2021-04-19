---
description: 您可以使用 WMI，以程式設計方式從效能程式庫中的物件存取系統計數器資料。
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: 監視效能資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cee18ba88a8aff920c2d14b5709a0fd913e2ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984727"
---
# <a name="monitoring-performance-data"></a><span data-ttu-id="6e539-103">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="6e539-103">Monitoring Performance Data</span></span>

<span data-ttu-id="6e539-104">您可以使用 WMI，以程式設計方式從效能程式庫中的物件存取系統計數器資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-104">Using WMI, you can access system counter data programmatically from objects in the performance libraries.</span></span> <span data-ttu-id="6e539-105">這是在 Perfmon 公用程式中出現在系統監視器中的相同效能資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-105">This is the same performance data that appears in the System Monitor in the Perfmon utility.</span></span> <span data-ttu-id="6e539-106">使用預先安裝的 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) ，取得腳本或 c + + 應用程式中的效能資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-106">Use the preinstalled [performance counter classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) to obtain performance data in scripts or C++ applications.</span></span>

<span data-ttu-id="6e539-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="6e539-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="6e539-108">WMI 效能類別</span><span class="sxs-lookup"><span data-stu-id="6e539-108">WMI Performance Classes</span></span>](#wmi-performance-classes)
-   [<span data-ttu-id="6e539-109">效能資料提供者</span><span class="sxs-lookup"><span data-stu-id="6e539-109">Performance Data Providers</span></span>](#performance-data-providers)
-   [<span data-ttu-id="6e539-110">使用格式化的效能資料類別</span><span class="sxs-lookup"><span data-stu-id="6e539-110">Using Formatted Performance Data Classes</span></span>](#using-formatted-performance-data-classes)
-   [<span data-ttu-id="6e539-111">使用原始效能資料類別</span><span class="sxs-lookup"><span data-stu-id="6e539-111">Using Raw Performance Data Classes</span></span>](#using-raw-performance-data-classes)
-   [<span data-ttu-id="6e539-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e539-112">Related topics</span></span>](#related-topics)

## <a name="wmi-performance-classes"></a><span data-ttu-id="6e539-113">WMI 效能類別</span><span class="sxs-lookup"><span data-stu-id="6e539-113">WMI Performance Classes</span></span>

<span data-ttu-id="6e539-114">例如，「系統監視器」中的「NetworkInterface」物件在 WMI 中是以原始資料的 [**win32 \_ PerfRawData \_ tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) 類別，以及用於預先計算的 [**win32 \_ PerfFormattedData \_ tcpip \_ NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 類別，或是格式化的資料來表示。</span><span class="sxs-lookup"><span data-stu-id="6e539-114">As an example, the "NetworkInterface" object, in System Monitor, is represented in WMI by the [**Win32\_PerfRawData\_Tcpip\_NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) class for raw data and the [**Win32\_PerfFormattedData\_Tcpip\_NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class for precalculated, or formatted data.</span></span> <span data-ttu-id="6e539-115">從 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 衍生的類別必須與 [*複習*](gloss-r.md) 物件一起使用。</span><span class="sxs-lookup"><span data-stu-id="6e539-115">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) must be used with a [*refresher*](gloss-r.md) object.</span></span> <span data-ttu-id="6e539-116">在原始資料類別上，您的 c + + 應用程式或腳本必須執行計算，才能取得與 Perfmon.exe 相同的輸出。</span><span class="sxs-lookup"><span data-stu-id="6e539-116">On raw data classes, your C++ application or script must perform calculations to obtain the same output as Perfmon.exe.</span></span> <span data-ttu-id="6e539-117">格式化的資料類別提供預先計算的資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-117">Formatted data classes supply precalculated data.</span></span> <span data-ttu-id="6e539-118">如需在 c + + 應用程式中取得資料的詳細資訊，請參閱 [在 c + + 中存取效能資料](accessing-performance-data-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="6e539-118">For more information about obtaining data in C++ applications, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="6e539-119">如需腳本，請參閱在腳本中 [存取效能資料](accessing-performance-data-in-script.md) 以及在 [腳本中重新整理 WMI 資料](refreshing-wmi-data-in-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="6e539-119">For scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="6e539-120">下列 VBScript 程式碼範例會使用 [**Win32 \_ PerfFormattedData \_ perfproc.dll \_ 進程**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 來取得閒置進程的效能資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-120">The following VBScript code example uses [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) to obtain performance data for the Idle process.</span></span> <span data-ttu-id="6e539-121">腳本會顯示在 Perfmon 中針對 Process 物件的% Processor Time 計數器顯示的相同資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-121">The script displays the same data that appears in Perfmon for the % Processor Time counter of the Process object.</span></span> <span data-ttu-id="6e539-122">對 [**SWbemObjectEx \_**](swbemobjectex-refresh-.md)的呼叫會執行重新整理作業。</span><span class="sxs-lookup"><span data-stu-id="6e539-122">The call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) performs the refresh operation.</span></span> <span data-ttu-id="6e539-123">請注意，資料必須在租用一次之後重新整理，才能取得基準。</span><span class="sxs-lookup"><span data-stu-id="6e539-123">Be aware that the data must be refreshed, at lease once, to obtain a baseline.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")
set PerfProcess = objWMIService.Get(_
    "Win32_PerfFormattedData_PerfProc_Process.Name='Idle'")

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend
```



<span data-ttu-id="6e539-124">效能計數器類別也可以提供統計資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-124">Performance counter classes can also provide statistical data.</span></span> <span data-ttu-id="6e539-125">如需詳細資訊，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="6e539-125">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="performance-data-providers"></a><span data-ttu-id="6e539-126">效能資料提供者</span><span class="sxs-lookup"><span data-stu-id="6e539-126">Performance Data Providers</span></span>

<span data-ttu-id="6e539-127">WMI 具有預先安裝的提供者，可監視本機系統和遠端的系統效能。</span><span class="sxs-lookup"><span data-stu-id="6e539-127">WMI has preinstalled providers that monitor system performance on both the local system and remotely.</span></span> <span data-ttu-id="6e539-128">[WmiPerfClass](wmiperfclass-provider.md)提供者會建立從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)衍生的類別。</span><span class="sxs-lookup"><span data-stu-id="6e539-128">The [WmiPerfClass](wmiperfclass-provider.md) provider creates the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="6e539-129">[WmiPerfInst](wmiperfinst-provider.md)提供者會動態提供原始和格式化類別的資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-129">The [WmiPerfInst](wmiperfinst-provider.md) provider supplies data dynamically to both raw and formatted classes.</span></span>

## <a name="using-formatted-performance-data-classes"></a><span data-ttu-id="6e539-130">使用格式化的效能資料類別</span><span class="sxs-lookup"><span data-stu-id="6e539-130">Using Formatted Performance Data Classes</span></span>

<span data-ttu-id="6e539-131">下列 VBScript 程式碼範例會取得有關記憶體、磁碟分割和伺服器工作佇列的效能資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-131">The following VBScript code example obtains performance data about memory, disk partitions, and server work queues.</span></span> <span data-ttu-id="6e539-132">腳本接著會判斷值是否在可接受的範圍內。</span><span class="sxs-lookup"><span data-stu-id="6e539-132">The script then determines if the values are within an acceptable range.</span></span>

<span data-ttu-id="6e539-133">腳本會使用下列 WMI 提供者物件和腳本物件：</span><span class="sxs-lookup"><span data-stu-id="6e539-133">The script uses the following WMI provider objects and scripting objects:</span></span>

-   <span data-ttu-id="6e539-134">預先安裝的 WMI 效能計數器類別。</span><span class="sxs-lookup"><span data-stu-id="6e539-134">Preinstalled WMI performance counter classes.</span></span>
-   <span data-ttu-id="6e539-135">複習物件， [**SWbemRefresher**](swbemrefresher.md)。</span><span class="sxs-lookup"><span data-stu-id="6e539-135">The refresher object, [**SWbemRefresher**](swbemrefresher.md).</span></span>
-   <span data-ttu-id="6e539-136">要新增至複習容器的專案， [ **SWbemRefreshableItem**](swbemrefreshableitem.md)</span><span class="sxs-lookup"><span data-stu-id="6e539-136">Items to add to the refresher container, [**SWbemRefreshableItem**](swbemrefreshableitem.md)</span></span>


```VB
Set objCimv2 = GetObject("winmgmts:root\cimv2")
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add items to the SWbemRefresher
' Without the SWbemRefreshableItem.ObjectSet call,
' the script will fail
Set objMemory = objRefresher.AddEnum _
    (objCimv2, _ 
    "Win32_PerfFormattedData_PerfOS_Memory").ObjectSet
Set objDiskQueue = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfDisk_LogicalDisk").ObjectSet
Set objQueueLength = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfNet_ServerWorkQueues").ObjectSet

' Initial refresh needed to get baseline values
objRefresher.Refresh
intTotalHealth = 0
' Do three refreshes to get data
For i = 1 to 3
    WScript.Echo "Refresh " & i
    For each intAvailableBytes in objMemory
        WScript.Echo "Available megabytes of memory: " _
            & intAvailableBytes.AvailableMBytes
        If intAvailableBytes.AvailableMBytes < 4 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intDiskQueue in objDiskQueue
        WScript.Echo "Current disk queue length " & "Name: " _
            & intDiskQueue.Name & ":" _
            & intDiskQueue.CurrentDiskQueueLength
        If intDiskQueue.CurrentDiskQueueLength > 2 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intServerQueueLength in objQueueLength
        WScript.Echo "Server work queue length: " _
            & intServerQueueLength.QueueLength
        If intServerQueueLength.QueueLength > 4 Then
            intTotalHealth = intTotalHealth + 1                       
        End If
    Wscript.Echo "  "
    Next
    If intTotalHealth > 0 Then
        Wscript.Echo "Unhealthy."
    Else
        Wscript.Echo "Healthy."
    End If
    intTotalHealth = 0
    Wscript.Sleep 5000
' Refresh data for all objects in the collection
    objRefresher.Refresh
Next
```



## <a name="using-raw-performance-data-classes"></a><span data-ttu-id="6e539-137">使用原始效能資料類別</span><span class="sxs-lookup"><span data-stu-id="6e539-137">Using Raw Performance Data Classes</span></span>

<span data-ttu-id="6e539-138">下列 VBScript 程式碼範例會取得本機電腦上原始的目前百分比處理器時間，並將其轉換為百分比。</span><span class="sxs-lookup"><span data-stu-id="6e539-138">The following VBScript code example obtains raw, current percent processor time on the local computer and converts it to a percentage.</span></span> <span data-ttu-id="6e539-139">此範例會示範如何從 [**Win32 \_ PerfRawData \_ PerfOS \_ Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)類別的 **PercentProcessorTime** 屬性取得原始效能資料。</span><span class="sxs-lookup"><span data-stu-id="6e539-139">The example shows you how to obtain raw performance data from the **PercentProcessorTime** property of the [**Win32\_PerfRawData\_PerfOS\_Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class.</span></span>

<span data-ttu-id="6e539-140">若要計算 percent processor time 值，您必須尋找公式。</span><span class="sxs-lookup"><span data-stu-id="6e539-140">To calculate the percent processor time value, you must locate the formula.</span></span> <span data-ttu-id="6e539-141">在 **CounterType** 限定詞中查詢 [**CounterType 限定詞**](countertype-qualifier.md)資料表中 **PercentProcessorTime** 屬性的值，以取得常數名稱。</span><span class="sxs-lookup"><span data-stu-id="6e539-141">Look up the value in the **CounterType** qualifier for the **PercentProcessorTime** property in the [**CounterType Qualifier**](countertype-qualifier.md) table to get the constant name.</span></span> <span data-ttu-id="6e539-142">找出 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) 中的常數名稱，以取得公式。</span><span class="sxs-lookup"><span data-stu-id="6e539-142">Locate the constant name in [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) to obtain the formula.</span></span>


```VB
Set objService = GetObject( _
    "Winmgmts:{impersonationlevel=impersonate}!\Root\Cimv2")

For i = 1 to 8
    Set objInstance1 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N1 = objInstance1.PercentProcessorTime
    D1 = objInstance1.TimeStamp_Sys100NS

'Sleep for two seconds = 2000 ms
    WScript.Sleep(2000)

    Set perf_instance2 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N2 = perf_instance2.PercentProcessorTime
    D2 = perf_instance2.TimeStamp_Sys100NS
' Look up the CounterType qualifier for the PercentProcessorTime 
' and obtain the formula to calculate the meaningful data. 
' CounterType - PERF_100NSEC_TIMER_INV
' Formula - (1- ((N2 - N1) / (D2 - D1))) x 100

    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    WScript.Echo "% Processor Time=" , Round(PercentProcessorTime,2)
Next
```



## <a name="related-topics"></a><span data-ttu-id="6e539-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e539-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e539-144">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="6e539-144">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
