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
ms.openlocfilehash: 65892608e642b675440d81127ef9afa0badd1d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111960"
---
# <a name="obtaining-statistical-performance-data"></a><span data-ttu-id="8c78e-104">取得統計效能資料</span><span class="sxs-lookup"><span data-stu-id="8c78e-104">Obtaining Statistical Performance Data</span></span>

<span data-ttu-id="8c78e-105">在 WMI 中，您可以根據衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)之格式化效能類別中的資料，來定義統計效能資料。</span><span class="sxs-lookup"><span data-stu-id="8c78e-105">In WMI, you can define statistical performance data based on data in formatted performance classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="8c78e-106">可用的統計資料為 [統計計數器類型](statistical-counter-types.md)中所定義的平均、最小值、最大值、範圍和變異數。</span><span class="sxs-lookup"><span data-stu-id="8c78e-106">The available statistics are average, minimum, maximum, range, and variance, as defined in [Statistical Counter Types](statistical-counter-types.md).</span></span>

<span data-ttu-id="8c78e-107">下列清單包含特殊的統計計數器類型：</span><span class="sxs-lookup"><span data-stu-id="8c78e-107">The following list includes the special statistical counter types:</span></span>

-   [<span data-ttu-id="8c78e-108">COOKER \_ 平均</span><span class="sxs-lookup"><span data-stu-id="8c78e-108">COOKER\_AVERAGE</span></span>](cooker-average.md)
-   [<span data-ttu-id="8c78e-109">COOKER \_ 分鐘</span><span class="sxs-lookup"><span data-stu-id="8c78e-109">COOKER\_MIN</span></span>](cooker-min.md)
-   [<span data-ttu-id="8c78e-110">COOKER \_ MAX</span><span class="sxs-lookup"><span data-stu-id="8c78e-110">COOKER\_MAX</span></span>](cooker-max.md)
-   [<span data-ttu-id="8c78e-111">COOKER \_ 範圍</span><span class="sxs-lookup"><span data-stu-id="8c78e-111">COOKER\_RANGE</span></span>](cooker-range.md)
-   [<span data-ttu-id="8c78e-112">COOKER \_ 變異數</span><span class="sxs-lookup"><span data-stu-id="8c78e-112">COOKER\_VARIANCE</span></span>](cooker-variance.md)

<span data-ttu-id="8c78e-113">下列範例示範如何：</span><span class="sxs-lookup"><span data-stu-id="8c78e-113">The following examples show how to:</span></span>

-   <span data-ttu-id="8c78e-114">建立定義計算資料類別的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="8c78e-114">Create a MOF file that defines a class of calculated data.</span></span>
-   <span data-ttu-id="8c78e-115">撰寫腳本來建立類別的實例，並定期以重新計算的統計值重新整理實例中的資料。</span><span class="sxs-lookup"><span data-stu-id="8c78e-115">Write a script that creates an instance of the class, and periodically refreshes the data in the instance with the recalculated statistical values.</span></span>

## <a name="mof-file"></a><span data-ttu-id="8c78e-116">MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="8c78e-116">MOF File</span></span>

<span data-ttu-id="8c78e-117">下列 MOF 程式碼範例會建立名為 **Win32 \_ PerfFormattedData \_ AvailableMBytes** 的新計算資料類別。</span><span class="sxs-lookup"><span data-stu-id="8c78e-117">The following MOF code example creates a new calculated data class named **Win32\_PerfFormattedData\_AvailableMBytes**.</span></span> <span data-ttu-id="8c78e-118">這個類別包含原始類別 [**Win32 \_ PerfRawData \_ PerfOS \_ 記憶體**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)的 **AvailableMBytes** 屬性資料。</span><span class="sxs-lookup"><span data-stu-id="8c78e-118">This class contains data from the **AvailableMBytes** property of the raw class [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span></span> <span data-ttu-id="8c78e-119">**Win32 \_ PerfFormattedData \_ AvailableBytes** 類別會定義 **平均**、**最小** 值、**最大值**、**範圍** 和變異數的 **屬性。**</span><span class="sxs-lookup"><span data-stu-id="8c78e-119">The **Win32\_PerfFormattedData\_AvailableBytes** class defines the properties **Average**, **Min**, **Max**, **Range**, and **Variance**.</span></span>

<span data-ttu-id="8c78e-120">MOF 檔案使用 [**格式化效能計數器類別的屬性限定詞**](property-qualifiers-for-performance-counter-classes.md) 來定義屬性資料來源和計算公式。</span><span class="sxs-lookup"><span data-stu-id="8c78e-120">The MOF file uses the [**Property Qualifiers for Formatted Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md) to define the property data source and the calculation formula.</span></span>

-   <span data-ttu-id="8c78e-121">**Average** 屬性會從 [**Win32 \_ PerfRawData \_ PerfOS \_ 記憶體**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)取得原始資料。**AvailableMBytes** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c78e-121">The **Average** property obtains raw data from the [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**AvailableMBytes** property.</span></span>
-   <span data-ttu-id="8c78e-122">**Average** 屬性的計數器辨識 **符號** 會指定原始資料來源。</span><span class="sxs-lookup"><span data-stu-id="8c78e-122">The Counter **qualifier** for the **Average** property specifies the raw data source.</span></span>
-   <span data-ttu-id="8c78e-123">**CookingType** 限定詞會指定計算資料的公式 [COOKER \_ MIN](cooker-min.md) 。</span><span class="sxs-lookup"><span data-stu-id="8c78e-123">The **CookingType** qualifier specifies the formula [COOKER\_MIN](cooker-min.md) for calculating the data.</span></span>
-   <span data-ttu-id="8c78e-124">**SampleWindow** 限定詞會指定執行計算之前要執行的樣本數。</span><span class="sxs-lookup"><span data-stu-id="8c78e-124">The **SampleWindow** qualifier specifies how many samples to take before performing the calculation.</span></span>


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



## <a name="script"></a><span data-ttu-id="8c78e-125">指令碼</span><span class="sxs-lookup"><span data-stu-id="8c78e-125">Script</span></span>

<span data-ttu-id="8c78e-126">下列腳本範例會使用先前建立的 MOF 來取得可用記憶體的相關統計資料（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c78e-126">The following script code example obtains statistics about available memory, in megabytes, using the MOF created previously.</span></span> <span data-ttu-id="8c78e-127">腳本會使用 [**SWbemRefresher**](swbemrefresher.md) 腳本物件來建立重新整理程式，其中包含 MOF 檔案所建立之 statistics 類別的一個實例，也就是 **Win32 \_ PerfFormattedData \_ MemoryStatistics**。</span><span class="sxs-lookup"><span data-stu-id="8c78e-127">The script uses the [**SWbemRefresher**](swbemrefresher.md) scripting object to create a refresher that contains one instance of the statistics class that the MOF file creates, which is **Win32\_PerfFormattedData\_MemoryStatistics**.</span></span> <span data-ttu-id="8c78e-128">如需使用腳本的詳細資訊，請參閱 [在腳本中重新整理 WMI 資料](refreshing-wmi-data-in-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="8c78e-128">For more information about using scripts, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span> <span data-ttu-id="8c78e-129">如果在 c + + 中工作，請參閱使用 [c + + 存取效能資料](accessing-performance-data-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="8c78e-129">If working in C++, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="8c78e-130">從 SWbemRefresher 的呼叫取得專案之後，必須呼叫 [**SWbemRefreshableItem。**](swbemrefreshableitem-object.md) [**加入**](swbemrefresher-add.md)或腳本將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8c78e-130">[**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) must be called after obtaining the item from the call to [**SWbemRefresher.Add**](swbemrefresher-add.md) or the script will fail.</span></span> <span data-ttu-id="8c78e-131">必須先呼叫 [**SWbemRefresher**](swbemrefresher-refresh.md) ，才能輸入迴圈來取得基準值，或在第一次傳遞時，統計屬性為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="8c78e-131">[**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) must be called before entering the loop to obtain baseline values, or the statistical properties is zero (0) on the first pass.</span></span>

 


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



## <a name="running-the-script"></a><span data-ttu-id="8c78e-132">執行腳本</span><span class="sxs-lookup"><span data-stu-id="8c78e-132">Running the Script</span></span>

<span data-ttu-id="8c78e-133">下列程式描述如何執行範例。</span><span class="sxs-lookup"><span data-stu-id="8c78e-133">The following procedure describes how to run the example.</span></span>

<span data-ttu-id="8c78e-134">**若要執行範例腳本**</span><span class="sxs-lookup"><span data-stu-id="8c78e-134">**To run the example script**</span></span>

1.  <span data-ttu-id="8c78e-135">將 MOF 程式碼和腳本複製到您電腦上的檔案中。</span><span class="sxs-lookup"><span data-stu-id="8c78e-135">Copy both the MOF code and script to files on your computer.</span></span>
2.  <span data-ttu-id="8c78e-136">將 mof 副檔名和腳本檔案命名為 .vbs 描述。</span><span class="sxs-lookup"><span data-stu-id="8c78e-136">Give the MOF file a .mof extension and the script file a .vbs description.</span></span>
3.  <span data-ttu-id="8c78e-137">在命令列上，切換至儲存檔案的目錄，並在 MOF 檔案上執行 [**mofcomp.exe**](mofcomp.md) 。</span><span class="sxs-lookup"><span data-stu-id="8c78e-137">On the command line, change to the directory where the files are stored, and run [**Mofcomp**](mofcomp.md) on the MOF file.</span></span> <span data-ttu-id="8c78e-138">例如，如果您將檔案命名為 *CalculatedData*，則命令為 **mofcomp.exe** *CalculatedData。*</span><span class="sxs-lookup"><span data-stu-id="8c78e-138">For example, if you name the file *CalculatedData.mof*, then the command is **Mofcomp** *CalculatedData.mof*</span></span>
4.  <span data-ttu-id="8c78e-139">執行指令碼。</span><span class="sxs-lookup"><span data-stu-id="8c78e-139">Run the script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c78e-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c78e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c78e-141">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="8c78e-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="8c78e-142">存取 WMI 預先安裝的效能類別</span><span class="sxs-lookup"><span data-stu-id="8c78e-142">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="8c78e-143">**格式化效能計數器類別的屬性限定詞**</span><span class="sxs-lookup"><span data-stu-id="8c78e-143">**Property Qualifiers for Formatted Performance Counter Classes**</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="8c78e-144">統計計數器類型</span><span class="sxs-lookup"><span data-stu-id="8c78e-144">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> </dl>

 

 
