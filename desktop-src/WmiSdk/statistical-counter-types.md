---
description: WMI 高效能格式化的效能 Data Provider 會計算指定之原始計數器資料樣本數目的統計計數器類型。
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: 統計計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027075"
---
# <a name="statistical-counter-types"></a><span data-ttu-id="357a8-103">統計計數器類型</span><span class="sxs-lookup"><span data-stu-id="357a8-103">Statistical Counter Types</span></span>

<span data-ttu-id="357a8-104">WMI 高效能格式化的 [效能 Data Provider](formatted-performance-data-provider.md) 會計算指定之原始計數器資料樣本數目的統計計數器類型。</span><span class="sxs-lookup"><span data-stu-id="357a8-104">The WMI high-performance [Formatted Performance Data Provider](formatted-performance-data-provider.md) calculates the statistical counter types on a specified number of raw counter data samples.</span></span> <span data-ttu-id="357a8-105">計數器類型的演算法不需要繼承 timestamp 或 frequency 屬性 (例如 **timestamp \_ PerfTime** 或其他計數器類型所需的 **frequency \_ PerfTime**) 。</span><span class="sxs-lookup"><span data-stu-id="357a8-105">The algorithms for the counter types do not require inherited timestamp or frequency properties (such as **TimeStamp\_PerfTime** or **Frequency\_PerfTime**) that other counter types require.</span></span>

<span data-ttu-id="357a8-106">相反地，統計計數器類型支援識別要使用之樣本數的辨識 **符號** 。</span><span class="sxs-lookup"><span data-stu-id="357a8-106">Instead, the statistical counter types support a **qualifier** that identifies how many samples to use.</span></span> <span data-ttu-id="357a8-107">針對效能物件呼叫 [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 方法時，會收集範例。</span><span class="sxs-lookup"><span data-stu-id="357a8-107">A sample is collected when the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method is called for the performance object.</span></span> <span data-ttu-id="357a8-108">針對腳本，請使用 [**SWbemRefresher**](swbemrefresher-refresh.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="357a8-108">For scripts use the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method.</span></span> <span data-ttu-id="357a8-109">計算的資料包含從原始資料屬性對樣本 **SampleWindow** 數目執行的計算結果。</span><span class="sxs-lookup"><span data-stu-id="357a8-109">The calculated data contains the result of the calculation performed on the **SampleWindow** number of samples from the raw data property.</span></span> <span data-ttu-id="357a8-110">計算的原始資料會 keyfromnode.frm 在 **計數器** 辨識符號中指定的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="357a8-110">The raw data for the calculation comes frm the property name specified in the **Counter** qualifier.</span></span>

<span data-ttu-id="357a8-111">如需詳細資訊，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md) 和 [存取 WMI 預先安裝的效能類別](accessing-wmi-preinstalled-performance-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="357a8-111">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>



| <span data-ttu-id="357a8-112">CounterType 常數</span><span class="sxs-lookup"><span data-stu-id="357a8-112">CounterType Constant</span></span>                    | <span data-ttu-id="357a8-113">Description</span><span class="sxs-lookup"><span data-stu-id="357a8-113">Description</span></span>                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="357a8-114">COOKER \_ 平均</span><span class="sxs-lookup"><span data-stu-id="357a8-114">COOKER\_AVERAGE</span></span>](cooker-average.md)   | <span data-ttu-id="357a8-115">加總 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別中某個屬性的重複觀察，並將總和除以觀察數目。</span><span class="sxs-lookup"><span data-stu-id="357a8-115">Sums repeated observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and divides the sum by the number of observations.</span></span>                              |
| [<span data-ttu-id="357a8-116">COOKER \_ MAX</span><span class="sxs-lookup"><span data-stu-id="357a8-116">COOKER\_MAX</span></span>](cooker-max.md)           | <span data-ttu-id="357a8-117">[**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中某一組屬性觀察值的最大值。</span><span class="sxs-lookup"><span data-stu-id="357a8-117">Largest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                    |
| [<span data-ttu-id="357a8-118">COOKER \_ 分鐘</span><span class="sxs-lookup"><span data-stu-id="357a8-118">COOKER\_MIN</span></span>](cooker-min.md)           | <span data-ttu-id="357a8-119">[**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中，屬性的一組觀察值的最小值。</span><span class="sxs-lookup"><span data-stu-id="357a8-119">Smallest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                   |
| [<span data-ttu-id="357a8-120">COOKER \_ 範圍</span><span class="sxs-lookup"><span data-stu-id="357a8-120">COOKER\_RANGE</span></span>](cooker-range.md)       | <span data-ttu-id="357a8-121">[**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中，屬性的一組原始觀察值的 [最小](cooker-min.md)值與 [最大](cooker-max.md)值之間的差異。</span><span class="sxs-lookup"><span data-stu-id="357a8-121">Difference between the [Min](cooker-min.md) and [Max](cooker-max.md) values for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span> |
| [<span data-ttu-id="357a8-122">COOKER \_ 變異數</span><span class="sxs-lookup"><span data-stu-id="357a8-122">COOKER\_VARIANCE</span></span>](cooker-variance.md) | <span data-ttu-id="357a8-123">變異數的量值，可以用來表示在 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別中，屬性的一組原始觀察值的散佈。</span><span class="sxs-lookup"><span data-stu-id="357a8-123">Measure of variability that can be used to characterize dispersion for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="357a8-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="357a8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="357a8-125">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="357a8-125">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="357a8-126">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="357a8-126">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="357a8-127">更新腳本中的 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="357a8-127">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="357a8-128">存取腳本中的效能資料</span><span class="sxs-lookup"><span data-stu-id="357a8-128">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="357a8-129">存取 c + + 中的效能資料</span><span class="sxs-lookup"><span data-stu-id="357a8-129">Accessing Performance Data in C++</span></span>](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
