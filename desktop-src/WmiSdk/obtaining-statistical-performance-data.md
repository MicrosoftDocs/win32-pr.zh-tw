---
description: 在 WMI 中，您可以根據衍生自 Win32 PerfFormattedData 之格式化效能類別中的資料，來定義統計效能資料 \_ 。 可用的統計資料為統計計數器類型中所定義的平均、最小值、最大值、範圍和變異數。
ms.assetid: 5552d5fc-df8c-4353-8593-c106ee19dc84
ms.tgt_platform: multiple
title: 取得統計效能資料
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0aad05ad1d61ee43deb713670391d8892393cdbdac45b7b80775bed59875bb19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923479"
---
# <a name="obtaining-statistical-performance-data"></a>取得統計效能資料

在 WMI 中，您可以根據衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)之格式化效能類別中的資料，來定義統計效能資料。 可用的統計資料為 [統計計數器類型](statistical-counter-types.md)中所定義的平均、最小值、最大值、範圍和變異數。

下列清單包含特殊的統計計數器類型：

-   [COOKER \_ 平均](cooker-average.md)
-   [COOKER \_ 分鐘](cooker-min.md)
-   [COOKER \_ MAX](cooker-max.md)
-   [COOKER \_ 範圍](cooker-range.md)
-   [COOKER \_ 變異數](cooker-variance.md)

下列範例示範如何：

-   建立定義計算資料類別的 MOF 檔案。
-   撰寫腳本來建立類別的實例，並定期以重新計算的統計值重新整理實例中的資料。

## <a name="mof-file"></a>MOF 檔案

下列 MOF 程式碼範例會建立名為 **Win32 \_ PerfFormattedData \_ AvailableMBytes** 的新計算資料類別。 這個類別包含原始類別 [**Win32 \_ PerfRawData \_ PerfOS \_ 記憶體**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)的 **AvailableMBytes** 屬性資料。 **Win32 \_ PerfFormattedData \_ AvailableBytes** 類別會定義 **平均**、**最小** 值、**最大值**、**範圍** 和變異數的 **屬性。**

MOF 檔案使用 [**格式化效能計數器類別的屬性限定詞**](property-qualifiers-for-performance-counter-classes.md) 來定義屬性資料來源和計算公式。

-   **Average** 屬性會從 [**Win32 \_ PerfRawData \_ PerfOS \_ 記憶體**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)取得原始資料。**AvailableMBytes** 屬性。
-   **Average** 屬性的計數器辨識 **符號** 會指定原始資料來源。
-   **CookingType** 限定詞會指定計算資料的公式 [COOKER \_ MIN](cooker-min.md) 。
-   **SampleWindow** 限定詞會指定執行計算之前要執行的樣本數。


```mof
// Store the new Win32_PerfFormattedData_MemoryStatistics
//     class in the Root\Cimv2 namespace
#pragma autorecover
#pragma namespace("\\\\.\\Root\\CimV2")

qualifier vendor:ToInstance;
qualifier guid:ToInstance;
qualifier displayname:ToInstance;
qualifier perfindex:ToInstance;
qualifier helpindex:ToInstance;
qualifier perfdetail:ToInstance;
qualifier countertype:ToInstance;
qualifier perfdefault:ToInstance;
qualifier defaultscale:ToInstance;

qualifier dynamic:ToInstance;
qualifier hiperf:ToInstance;
qualifier AutoCook:ToInstance;
qualifier AutoCook_RawClass:ToInstance;
qualifier CookingType:ToInstance;
qualifier Counter:ToInstance;


// Define the Win32_PerFormattedData_MemoryStatistics
//     class, derived from Win32_PerfFormattedData
[
  dynamic,
  // Name of formatted data provider: "WMIPerfInst" for Vista 
  //   and later
  provider("HiPerfCooker_v1"), 
  // Text that will identify new counter in Perfmon
  displayname("My Calculated Counter"),                            
  // A high performance class     
  Hiperf,
  // Contains calculated data 
  Cooked, 
  // Value must be 1 
  AutoCook(1), 
  // Raw performance class to get data for calculations
  AutoCook_RawClass("Win32_PerfRawData_PerfOS_Memory"),
  // Value must be 1        
  AutoCook_RawDefault(1),
  // Name of raw class property to use for timestamp in formulas 
  PerfSysTimeStamp("Timestamp_PerfTime"), 
  // Name of raw class property to use for frequency in formulas
  PerfSysTimeFreq("Frequency_PerfTime"), 
  // Name of raw class property to use for timestamp in formulas
  Perf100NSTimeStamp("Timestamp_Sys100NS"),
  // Name of raw class property to use for frequency in formulas
  Perf100NSTimeFreq("Frequency_Sys100NS"),
  // Name of raw class property to use for timestamp in formulas
  PerfObjTimeStamp("Timestamp_Object"),
  // Name of raw class property to use for frequency in formulas 
  PerfObjTimeFreq("Frequency_Object"),
  // Only one instance of class allowed in namespace
  singleton                                                   
]

class Win32_PerfFormattedData_MemoryStatistics
          : Win32_PerfFormattedData
{

// Define the properties for the class. 
// All the properties perform different
//     statistical operations on the same
//     property, AvailableMBytes, in the raw class

// Define the Average property,
//     which uses the "COOKER_AVERAGE" counter type and 
//     gets its data from the AvailableMBytes 
//     property in the raw class

    [
     CookingType("COOKER_AVERAGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Average = 0;

// Define the Min property, which uses
//     the "COOKER_MIN" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_MIN"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Min = 0;

// Define the Max property, which uses
//     the "COOKER_MAX" counter type and 
//     gets its data from the
//     AvailableMBytes property in the raw class

    [
     CookingType("COOKER_MAX"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Max = 0;

// Define the Range property, which uses
//     the "COOKER_RANGE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_RANGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Range = 0;

// Define the Variance property, which uses
//     the "COOKER_VARIANCE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_VARIANCE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Variance = 0;
};
```



## <a name="script"></a>指令碼

下列腳本範例會使用先前建立的 MOF 來取得可用記憶體的相關統計資料（以 mb 為單位）。 腳本會使用 [**SWbemRefresher**](swbemrefresher.md) 腳本物件來建立重新整理程式，其中包含 MOF 檔案所建立之 statistics 類別的一個實例，也就是 **Win32 \_ PerfFormattedData \_ MemoryStatistics**。 如需使用腳本的詳細資訊，請參閱 [在腳本中重新整理 WMI 資料](refreshing-wmi-data-in-scripts.md)。 如果在 c + + 中工作，請參閱使用 [c + + 存取效能資料](accessing-performance-data-in-c--.md)。

> [!Note]  
> 從 SWbemRefresher 的呼叫取得專案之後，必須呼叫 [**SWbemRefreshableItem。**](swbemrefreshableitem-object.md) [**加入**](swbemrefresher-add.md)或腳本將會失敗。 必須先呼叫 [**SWbemRefresher**](swbemrefresher-refresh.md) ，才能輸入迴圈來取得基準值，或在第一次傳遞時，統計屬性為零 (0) 。

 


```VB
' Connect to the Root\Cimv2 namespace
strComputer = "."
Set objService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Create a refresher
Set Refresher = CreateObject("WbemScripting.SWbemRefresher")
If Err <> 0 Then
WScript.Echo Err
WScript.Quit
End If

' Add the single instance of the statistics
'    class to the refresher
Set obMemoryStatistics = Refresher.Add(objService, _
    "Win32_PerfFormattedData_MemoryStatistics=@").Object

' Refresh once to obtain base values for cooking calculations
Refresher.Refresh

Const REFRESH_INTERVAL = 10

' Refresh every REFRESH_INTERVAL seconds 
For I=1 to 3
  WScript.Sleep REFRESH_INTERVAL * 1000
  Refresher.Refresh

  WScript.Echo "System memory statistics" _
      & "(Available Megabytes) " _
      & "for the past 100 seconds - pass " & i 
  WScript.Echo "Average = " _
     & obMemoryStatistics.Average & VBNewLine & "Max = " _
     & obMemoryStatistics.Max & VBNewLine & "Min = " _
     & obMemoryStatistics.Min & VBNewLine & "Range = " _ 
     & obMemoryStatistics.Range & VBNewLine & "Variance = " _
     & obMemoryStatistics.Variance 
Next
```



## <a name="running-the-script"></a>執行腳本

下列程式描述如何執行範例。

**若要執行範例腳本**

1.  將 MOF 程式碼和腳本複製到您電腦上的檔案中。
2.  將 mof 副檔名和腳本檔案命名為 .vbs 描述。
3.  在命令列上，切換至儲存檔案的目錄，並在 MOF 檔案上執行 [**mofcomp.exe**](mofcomp.md) 。 例如，如果您將檔案命名為 *CalculatedData*，則命令為 **mofcomp.exe** *CalculatedData。*
4.  執行指令碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> <dt>

[存取 WMI 預先安裝的效能類別](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[**格式化效能計數器類別的屬性限定詞**](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[統計計數器類型](statistical-counter-types.md)
</dt> </dl>

 

 
