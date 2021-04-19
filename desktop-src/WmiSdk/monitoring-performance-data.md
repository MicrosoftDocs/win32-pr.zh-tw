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
# <a name="monitoring-performance-data"></a>監視效能資料

您可以使用 WMI，以程式設計方式從效能程式庫中的物件存取系統計數器資料。 這是在 Perfmon 公用程式中出現在系統監視器中的相同效能資料。 使用預先安裝的 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) ，取得腳本或 c + + 應用程式中的效能資料。

本主題將討論下列各節：

-   [WMI 效能類別](#wmi-performance-classes)
-   [效能資料提供者](#performance-data-providers)
-   [使用格式化的效能資料類別](#using-formatted-performance-data-classes)
-   [使用原始效能資料類別](#using-raw-performance-data-classes)
-   [相關主題](#related-topics)

## <a name="wmi-performance-classes"></a>WMI 效能類別

例如，「系統監視器」中的「NetworkInterface」物件在 WMI 中是以原始資料的 [**win32 \_ PerfRawData \_ tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) 類別，以及用於預先計算的 [**win32 \_ PerfFormattedData \_ tcpip \_ NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 類別，或是格式化的資料來表示。 從 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 衍生的類別必須與 [*複習*](gloss-r.md) 物件一起使用。 在原始資料類別上，您的 c + + 應用程式或腳本必須執行計算，才能取得與 Perfmon.exe 相同的輸出。 格式化的資料類別提供預先計算的資料。 如需在 c + + 應用程式中取得資料的詳細資訊，請參閱 [在 c + + 中存取效能資料](accessing-performance-data-in-c--.md)。 如需腳本，請參閱在腳本中 [存取效能資料](accessing-performance-data-in-script.md) 以及在 [腳本中重新整理 WMI 資料](refreshing-wmi-data-in-scripts.md)。

下列 VBScript 程式碼範例會使用 [**Win32 \_ PerfFormattedData \_ perfproc.dll \_ 進程**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 來取得閒置進程的效能資料。 腳本會顯示在 Perfmon 中針對 Process 物件的% Processor Time 計數器顯示的相同資料。 對 [**SWbemObjectEx \_**](swbemobjectex-refresh-.md)的呼叫會執行重新整理作業。 請注意，資料必須在租用一次之後重新整理，才能取得基準。


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



效能計數器類別也可以提供統計資料。 如需詳細資訊，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md)。

## <a name="performance-data-providers"></a>效能資料提供者

WMI 具有預先安裝的提供者，可監視本機系統和遠端的系統效能。 [WmiPerfClass](wmiperfclass-provider.md)提供者會建立從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)衍生的類別。 [WmiPerfInst](wmiperfinst-provider.md)提供者會動態提供原始和格式化類別的資料。

## <a name="using-formatted-performance-data-classes"></a>使用格式化的效能資料類別

下列 VBScript 程式碼範例會取得有關記憶體、磁碟分割和伺服器工作佇列的效能資料。 腳本接著會判斷值是否在可接受的範圍內。

腳本會使用下列 WMI 提供者物件和腳本物件：

-   預先安裝的 WMI 效能計數器類別。
-   複習物件， [**SWbemRefresher**](swbemrefresher.md)。
-   要新增至複習容器的專案， [ **SWbemRefreshableItem**](swbemrefreshableitem.md)


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



## <a name="using-raw-performance-data-classes"></a>使用原始效能資料類別

下列 VBScript 程式碼範例會取得本機電腦上原始的目前百分比處理器時間，並將其轉換為百分比。 此範例會示範如何從 [**Win32 \_ PerfRawData \_ PerfOS \_ Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)類別的 **PercentProcessorTime** 屬性取得原始效能資料。

若要計算 percent processor time 值，您必須尋找公式。 在 **CounterType** 限定詞中查詢 [**CounterType 限定詞**](countertype-qualifier.md)資料表中 **PercentProcessorTime** 屬性的值，以取得常數名稱。 找出 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) 中的常數名稱，以取得公式。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI](using-wmi.md)
</dt> </dl>

 

 
