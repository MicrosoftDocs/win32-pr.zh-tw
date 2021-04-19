---
description: 表示一段時間內樣本之間的差異，而且通常會使用基底值進行計算。
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: 基本演算法計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979979"
---
# <a name="basic-algorithm-counter-types"></a><span data-ttu-id="30b3d-103">基本演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="30b3d-103">Basic Algorithm Counter Types</span></span>

<span data-ttu-id="30b3d-104">基本演算法計數器類型通常代表一段時間內樣本之間的差異，而且通常會使用基底值進行計算。</span><span class="sxs-lookup"><span data-stu-id="30b3d-104">Basic algorithm counter types generally represent differences between samples over time, and often use a base value for the calculation.</span></span> <span data-ttu-id="30b3d-105">例如， [**Win32 \_ PerfFormattedData \_ PerfDisk \_ PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)類別的 **PercentFreeSpace** 屬性代表實體磁片單元上可用空間的比率，以及所選實體磁片磁碟機所提供的總可用空間。</span><span class="sxs-lookup"><span data-stu-id="30b3d-105">For example, the **PercentFreeSpace** property of the [**Win32\_PerfFormattedData\_PerfDisk\_PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class represents the ratio of the free space available on the physical disk unit to the total usable space provided by the selected physical disk drive.</span></span> <span data-ttu-id="30b3d-106">這個類別也包含基底值 **PercentFreeSpace \_ base**。</span><span class="sxs-lookup"><span data-stu-id="30b3d-106">This class also contains the base value, **PercentFreeSpace\_Base**.</span></span> <span data-ttu-id="30b3d-107">將 **PercentFreeSpace** 除以 **PercentFreeSpace \_ Base** 並乘以100%，可取得可用磁碟空間的百分比。</span><span class="sxs-lookup"><span data-stu-id="30b3d-107">The percentage of free disk space is obtained by dividing **PercentFreeSpace** by **PercentFreeSpace\_Base** and multiplying by 100%.</span></span>

<span data-ttu-id="30b3d-108">提供下表中的基本演算法。</span><span class="sxs-lookup"><span data-stu-id="30b3d-108">The basic algorithms in the following table are provided.</span></span>



| <span data-ttu-id="30b3d-109">CounterType 常數</span><span class="sxs-lookup"><span data-stu-id="30b3d-109">CounterType Constant</span></span>                                                                                    | <span data-ttu-id="30b3d-110">Description</span><span class="sxs-lookup"><span data-stu-id="30b3d-110">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b3d-111">[效能 \_原始 \_ 分數](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))小數537003008</span><span class="sxs-lookup"><span data-stu-id="30b3d-111">[PERF\_RAW\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 537003008</span></span><br/>       | <span data-ttu-id="30b3d-112">子集與其集合的比率（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="30b3d-112">Ratio of a subset to its set as a percentage.</span></span> <span data-ttu-id="30b3d-113">此計數器類型只會顯示目前的百分比，而不會顯示一段時間的平均值。</span><span class="sxs-lookup"><span data-stu-id="30b3d-113">This counter type displays the current percentage only, not an average over time.</span></span>                                    |
| <span data-ttu-id="30b3d-114">[效能 \_樣本 \_ 分數](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))小數549585920</span><span class="sxs-lookup"><span data-stu-id="30b3d-114">[PERF\_SAMPLE\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 549585920</span></span><br/>    | <span data-ttu-id="30b3d-115">最後兩個取樣間隔期間，對所有作業的平均點擊率。</span><span class="sxs-lookup"><span data-stu-id="30b3d-115">Average ratio of hits to all operations during the last two sample intervals.</span></span> <span data-ttu-id="30b3d-116">此計數器類型需要具有效能 \_ 範例 \_ 基底計數器類型的基底屬性。</span><span class="sxs-lookup"><span data-stu-id="30b3d-116">This counter type requires a base property with the PERF\_SAMPLE\_BASE counter type.</span></span> |
| <span data-ttu-id="30b3d-117">[效能 \_計數器 \_ DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span><span class="sxs-lookup"><span data-stu-id="30b3d-117">[PERF\_COUNTER\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span></span><br/>        | <span data-ttu-id="30b3d-118">此計數器型別顯示最近兩次取樣間隔間之測量屬性 (Attribute) 的變更 </span><span class="sxs-lookup"><span data-stu-id="30b3d-118">This counter type shows the change in the measured attribute between the two most recent sample intervals.</span></span>                                                         |
| <span data-ttu-id="30b3d-119">[效能 \_計數器 \_ 大型 \_ DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584</span><span class="sxs-lookup"><span data-stu-id="30b3d-119">[PERF\_COUNTER\_LARGE\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584</span></span><br/> | <span data-ttu-id="30b3d-120">與性能 \_ 計數器 DELTA 相同， \_ 但針對較大的值是64位表示。</span><span class="sxs-lookup"><span data-stu-id="30b3d-120">Same as PERF\_COUNTER\_DELTA but a 64-bit representation for larger values.</span></span>                                                                                        |
| <span data-ttu-id="30b3d-121">[效能 \_經過 \_ 時間](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位807666944</span><span class="sxs-lookup"><span data-stu-id="30b3d-121">[PERF\_ELAPSED\_TIME](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944</span></span><br/>       | <span data-ttu-id="30b3d-122">進程開始的時間與計算此值的時間之間的總時間。</span><span class="sxs-lookup"><span data-stu-id="30b3d-122">Total time between when the process started and the time when this value is calculated.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="30b3d-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="30b3d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30b3d-124">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="30b3d-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

