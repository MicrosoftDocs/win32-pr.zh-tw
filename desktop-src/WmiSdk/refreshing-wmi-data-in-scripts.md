---
description: 在監視腳本中，您可以使用 SWbemRefresher 物件來避免後續呼叫 GetObject。 SWbemRefresher 物件是一個容器，可保存數個 WMI 物件，其資料可在單一呼叫中重新整理。
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: 更新腳本中的 WMI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969a97c6300ac256e08c79e4f4aaeaa8d05bda072a2c310812ce3b2061c791fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050446"
---
# <a name="refreshing-wmi-data-in-scripts"></a>更新腳本中的 WMI 資料

在監視腳本中，您可以使用 [**SWbemRefresher**](swbemrefresher.md)物件來避免後續呼叫 **GetObject** 。 **SWbemRefresher** 物件是一個容器，可保存數個 WMI 物件，其資料可在單一呼叫中重新整理。

需要使用 [**SWbemRefresher**](swbemrefresher.md) 物件才能從 WMI 效能類別取得精確的資料，例如 [**win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) 或衍生自 win32 效能的其他預 [**安裝 \_**](/windows/desktop/CIMWin32Prov/win32-perf)類別。

下列程式描述如何在腳本中重新整理資料。

**若要在腳本中重新整理資料**

1.  呼叫 **CreateObject** 來建立 [**SWbemRefresher**](swbemrefresher.md) 重新整理程式物件。

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  連線至 WMI 命名空間。 若要使用預先安裝的 [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-perf) 效能效能等級，請連接到 **根 \\ cimv2**。

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  新增單一物件 (呼叫 [**SWbemRefresher。新增**](swbemrefresher-add.md)) 或集合 (呼叫 [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) 至複習。

    使用衍生自 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的預先計算資料類別，例如 [**win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) ，而不是 [**win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)。 否則，您必須計算簡單計數器以外的所有屬性值。

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  重新整理資料一次，以取得初始效能資料。

    請呼叫 [**SWbemRefresher**](swbemrefresher-refresh.md)方法或泛型 [**SWbemObjectEx \_**](swbemobjectex-refresh-.md)方法。

    ```VB
    objRefresher.Refresh
    ```

    

5.  如果您正在監視效能，並且在重新整理器物件中有集合，請在集合物件中執行迴圈。

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  藉由呼叫 [**SWbemRefresher DeleteAll**](swbemrefresher-deleteall.md) ，或藉由呼叫 [**SWbemRefresher**](swbemrefresher-remove.md)來移除特定專案，以清除重新整理程式中的專案。

下列 VBScript 程式碼範例顯示如何重新整理本機電腦上的單一物件。 腳本會建立重新整理程式容器，並加入 [**Win32 \_ PerfFormattedData \_ perfproc.dll \_ 進程**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 實例的枚舉器實例。 重新 [**整理呼叫會**](swbemrefresher-refresh.md) 進行三次，以針對使用超過一% 處理器時間的處理常式，示範 **PercentProcessorTime** 屬性中的變更。


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



傳回之 [**SWbemRefreshableItem**](swbemrefreshableitem.md)的 [**index**](swbemrefreshableitem-index.md)屬性代表重新整理程式集合中的物件索引。 您可以呼叫 [**SWbemRefreshableItem IsSet**](swbemrefreshableitem-isset.md) 屬性，以判斷重新整理程式中的某個專案是單一專案或集合。 若要存取單一專案，請使用 [**SWbemRefreshableItem 物件**](swbemrefreshableitem-object.md) 屬性。 如果您未對 **SWbemRefreshableItem** 進行呼叫，則腳本會在您嘗試存取物件時失敗。 若要存取集合，請使用 [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[存取腳本中的效能資料](accessing-performance-data-in-script.md)
</dt> <dt>

[WMI 工作：效能監視](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> </dl>

 

 
