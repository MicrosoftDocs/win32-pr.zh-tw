---
description: 佇列長度演算法計數器會依適當的 frequency 屬性所指定的每個取樣間隔，遞增佇列中的專案數&\# 8212;Frequency \_ PerfTime 等等。
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: 佇列長度演算法計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192088"
---
# <a name="queue-length-algorithm-counter-types"></a><span data-ttu-id="d6546-103">佇列長度演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="d6546-103">Queue-length Algorithm Counter Types</span></span>

<span data-ttu-id="d6546-104">佇列長度的演算法計數器類型會依照適當的 frequency 屬性頻率 PerfTime 所指定的間隔，遞增佇列中的專案數 \_ ，依此類推。</span><span class="sxs-lookup"><span data-stu-id="d6546-104">Queue-length algorithm counter types increment the number of items in a queue at each sample interval as specified by the appropriate frequency property Frequency\_PerfTime, and so on.</span></span> <span data-ttu-id="d6546-105">處理後結果會除以樣本數，以產生平均佇列長度。</span><span class="sxs-lookup"><span data-stu-id="d6546-105">The cooked result divides by the number of samples to produce the average queue length.</span></span>

<span data-ttu-id="d6546-106">例如， [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)中使用性能 \_ 計數器 \_ 100ns \_ QUEUELEN \_ type 計數器類型的 >avgdiskqueuelength 屬性。</span><span class="sxs-lookup"><span data-stu-id="d6546-106">An example is the **AvgDiskQueueLength** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) that uses the PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE counter type.</span></span>



| <span data-ttu-id="d6546-107">CounterType 常數</span><span class="sxs-lookup"><span data-stu-id="d6546-107">CounterType Constant</span></span>                                                                                                 | <span data-ttu-id="d6546-108">Description</span><span class="sxs-lookup"><span data-stu-id="d6546-108">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6546-109">[效能 \_計數器 \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span><span class="sxs-lookup"><span data-stu-id="d6546-109">[PERF\_COUNTER\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span></span><br/>            | <span data-ttu-id="d6546-110">一段時間內的資源佇列平均長度。</span><span class="sxs-lookup"><span data-stu-id="d6546-110">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="d6546-111">它會顯示在最新的兩個樣本間隔期間，所觀察佇列長度之間的差異值，再除以間隔的持續時間。</span><span class="sxs-lookup"><span data-stu-id="d6546-111">It shows the difference between the queue lengths observed during the last two sample intervals divided by the duration of the interval.</span></span>                       |
| <span data-ttu-id="d6546-112">[效能 \_計數器 \_ 大型 \_ QUEUELEN \_ 類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span><span class="sxs-lookup"><span data-stu-id="d6546-112">[PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span></span><br/>     | <span data-ttu-id="d6546-113">一段時間內的資源佇列平均長度。</span><span class="sxs-lookup"><span data-stu-id="d6546-113">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="d6546-114">這個型別的計數器會顯示在最新的兩個樣本間隔期間，所觀察佇列長度之間的差異值，再除以間隔的持續時間。</span><span class="sxs-lookup"><span data-stu-id="d6546-114">Counters of this type display the difference between the queue lengths observed during the last two sample intervals, divided by the duration of the interval.</span></span> |
| <span data-ttu-id="d6546-115">[效能 \_計數器 \_ 100ns \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span><span class="sxs-lookup"><span data-stu-id="d6546-115">[PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span></span><br/>     | <span data-ttu-id="d6546-116">一段時間內的資源佇列平均長度，以100毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="d6546-116">Average length of a queue to a resource over time in 100 nanosecond units.</span></span>                                                                                                                                        |
| <span data-ttu-id="d6546-117">[效能 \_計數器 \_ OBJ \_ TIME \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span><span class="sxs-lookup"><span data-stu-id="d6546-117">[PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span></span><br/> | <span data-ttu-id="d6546-118">物件在佇列中的時間。</span><span class="sxs-lookup"><span data-stu-id="d6546-118">Time an object is in a queue.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="d6546-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6546-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6546-120">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="d6546-120">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

