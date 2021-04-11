---
description: 在監視腳本中，您可以使用 SWbemRefresher 物件來避免後續呼叫 GetObject。 SWbemRefresher 物件是一個容器，可保存數個 WMI 物件，其資料可在單一呼叫中重新整理。
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: 更新腳本中的 WMI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193638"
---
# <a name="refreshing-wmi-data-in-scripts"></a><span data-ttu-id="c715d-104">更新腳本中的 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="c715d-104">Refreshing WMI Data in Scripts</span></span>

<span data-ttu-id="c715d-105">在監視腳本中，您可以使用 [**SWbemRefresher**](swbemrefresher.md)物件來避免後續呼叫 **GetObject** 。</span><span class="sxs-lookup"><span data-stu-id="c715d-105">In monitoring scripts, you can avoid successive calls to **GetObject** by using an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="c715d-106">**SWbemRefresher** 物件是一個容器，可保存數個 WMI 物件，其資料可在單一呼叫中重新整理。</span><span class="sxs-lookup"><span data-stu-id="c715d-106">The **SWbemRefresher** object is a container that can hold several WMI objects whose data can be refreshed in one call.</span></span>

<span data-ttu-id="c715d-107">需要使用 [**SWbemRefresher**](swbemrefresher.md) 物件才能從 WMI 效能類別取得精確的資料，例如 [**win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) 或衍生自 win32 效能的其他預 [**安裝 \_**](/windows/desktop/CIMWin32Prov/win32-perf)類別。</span><span class="sxs-lookup"><span data-stu-id="c715d-107">Using an [**SWbemRefresher**](swbemrefresher.md) object is required to get accurate data from WMI performance classes, such as [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) or other preinstalled classes derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span>

<span data-ttu-id="c715d-108">下列程式描述如何在腳本中重新整理資料。</span><span class="sxs-lookup"><span data-stu-id="c715d-108">The following procedure describes how to refresh data in scripts.</span></span>

<span data-ttu-id="c715d-109">**若要在腳本中重新整理資料**</span><span class="sxs-lookup"><span data-stu-id="c715d-109">**To refresh data in scripts**</span></span>

1.  <span data-ttu-id="c715d-110">呼叫 **CreateObject** 來建立 [**SWbemRefresher**](swbemrefresher.md) 重新整理程式物件。</span><span class="sxs-lookup"><span data-stu-id="c715d-110">Call **CreateObject** to create an [**SWbemRefresher**](swbemrefresher.md) refresher object.</span></span>

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  <span data-ttu-id="c715d-111">連接到 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="c715d-111">Connect to the WMI namespace.</span></span> <span data-ttu-id="c715d-112">若要使用預先安裝的 [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-perf) 效能效能等級，請連接到 **根 \\ cimv2**。</span><span class="sxs-lookup"><span data-stu-id="c715d-112">To use preinstalled [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) performances classes, connect to **root\\cimv2**.</span></span>

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  <span data-ttu-id="c715d-113">新增單一物件 (呼叫 [**SWbemRefresher。新增**](swbemrefresher-add.md)) 或集合 (呼叫 [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) 至複習。</span><span class="sxs-lookup"><span data-stu-id="c715d-113">Add a single object (call [**SWbemRefresher.Add**](swbemrefresher-add.md)) or a collection (call [**SWbemRefresher.AddEnum**](swbemrefresher-addenum.md)) to the refresher.</span></span>

    <span data-ttu-id="c715d-114">使用衍生自 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的預先計算資料類別，例如 [**win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) ，而不是 [**win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="c715d-114">Use the precalculated data classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), for example, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) instead of [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="c715d-115">否則，您必須計算簡單計數器以外的所有屬性值。</span><span class="sxs-lookup"><span data-stu-id="c715d-115">Otherwise, you must calculate the values for all of the properties other than simple counters.</span></span>

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  <span data-ttu-id="c715d-116">重新整理資料一次，以取得初始效能資料。</span><span class="sxs-lookup"><span data-stu-id="c715d-116">Refresh the data one time to get the initial performance data.</span></span>

    <span data-ttu-id="c715d-117">請呼叫 [**SWbemRefresher**](swbemrefresher-refresh.md)方法或泛型 [**SWbemObjectEx \_**](swbemobjectex-refresh-.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c715d-117">Call either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the generic [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

    ```VB
    objRefresher.Refresh
    ```

    

5.  <span data-ttu-id="c715d-118">如果您正在監視效能，並且在重新整理器物件中有集合，請在集合物件中執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="c715d-118">If you are monitoring performance and have a collection in the refresher object, loop through the collection objects.</span></span>

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  <span data-ttu-id="c715d-119">藉由呼叫 [**SWbemRefresher DeleteAll**](swbemrefresher-deleteall.md) ，或藉由呼叫 [**SWbemRefresher**](swbemrefresher-remove.md)來移除特定專案，以清除重新整理程式中的專案。</span><span class="sxs-lookup"><span data-stu-id="c715d-119">Clear the items from the refresher by calling [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) or remove specific items by calling [**SwbemRefresher.Remove**](swbemrefresher-remove.md).</span></span>

<span data-ttu-id="c715d-120">下列 VBScript 程式碼範例顯示如何重新整理本機電腦上的單一物件。</span><span class="sxs-lookup"><span data-stu-id="c715d-120">The following VBScript code example shows how to refresh a single object on the local computer.</span></span> <span data-ttu-id="c715d-121">腳本會建立重新整理程式容器，並加入 [**Win32 \_ PerfFormattedData \_ perfproc.dll \_ 進程**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 實例的枚舉器實例。</span><span class="sxs-lookup"><span data-stu-id="c715d-121">The script creates a refresher container and adds an instance of an enumerator for [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instances.</span></span> <span data-ttu-id="c715d-122">重新 [**整理呼叫會**](swbemrefresher-refresh.md) 進行三次，以針對使用超過一% 處理器時間的處理常式，示範 **PercentProcessorTime** 屬性中的變更。</span><span class="sxs-lookup"><span data-stu-id="c715d-122">The [**Refresh**](swbemrefresher-refresh.md) call is made three times to demonstrate the changes in the **PercentProcessorTime** property for processes using more than one percent of the processor time.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



<span data-ttu-id="c715d-123">傳回之 [**SWbemRefreshableItem**](swbemrefreshableitem.md)的 [**index**](swbemrefreshableitem-index.md)屬性代表重新整理程式集合中的物件索引。</span><span class="sxs-lookup"><span data-stu-id="c715d-123">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span> <span data-ttu-id="c715d-124">您可以呼叫 [**SWbemRefreshableItem IsSet**](swbemrefreshableitem-isset.md) 屬性，以判斷重新整理程式中的某個專案是單一專案或集合。</span><span class="sxs-lookup"><span data-stu-id="c715d-124">You can call [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) property to determine whether or not an item in a refresher is a single item or a collection.</span></span> <span data-ttu-id="c715d-125">若要存取單一專案，請使用 [**SWbemRefreshableItem 物件**](swbemrefreshableitem-object.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c715d-125">To access a single item, use the [**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) property.</span></span> <span data-ttu-id="c715d-126">如果您未對 **SWbemRefreshableItem** 進行呼叫，則腳本會在您嘗試存取物件時失敗。</span><span class="sxs-lookup"><span data-stu-id="c715d-126">If you do not make the call to **SWbemRefreshableItem.Object**, then the script fails when you try to access the object.</span></span> <span data-ttu-id="c715d-127">若要存取集合，請使用 [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c715d-127">To access a collection, use the [**SWbemRefreshableItem.ObjectSet**](swbemrefreshableitem-objectset.md) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c715d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="c715d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c715d-129">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="c715d-129">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="c715d-130">存取腳本中的效能資料</span><span class="sxs-lookup"><span data-stu-id="c715d-130">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="c715d-131">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="c715d-131">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="c715d-132">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="c715d-132">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
