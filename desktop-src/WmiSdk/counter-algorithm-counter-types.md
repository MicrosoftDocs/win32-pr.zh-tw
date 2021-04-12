---
description: 計數器演算法計數器類型可能會計算取樣的速率或平均位元組數，或針對特定作業的時間長度。
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: 計數器演算法計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319675"
---
# <a name="counter-algorithm-counter-types"></a><span data-ttu-id="b3192-103">計數器演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="b3192-103">Counter Algorithm Counter Types</span></span>

<span data-ttu-id="b3192-104">計數器演算法計數器類型可能會計算取樣的速率或平均位元組數，或針對特定作業的時間長度。</span><span class="sxs-lookup"><span data-stu-id="b3192-104">Counter algorithm counter types may calculate rates or averages bytes for a sample or over a time period for a particular operation.</span></span>

<span data-ttu-id="b3192-105">[**Win32 \_ PerfRawData \_ PerfDisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85))類別中的 **AvgDiskBytesPerTransfer** 屬性會使用效能 \_ 平均 \_ 大量 countertype。</span><span class="sxs-lookup"><span data-stu-id="b3192-105">The **AvgDiskBytesPerTransfer** property in the [**Win32\_PerfRawData\_PerfDisk\_PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) class uses the PERF\_AVERAGE\_BULK countertype.</span></span> <span data-ttu-id="b3192-106">在此情況下，傳輸是作業，而傳送的位元組累積數目是計數器資料。</span><span class="sxs-lookup"><span data-stu-id="b3192-106">In this case, the transfer is the operation, and the accumulating number of bytes that are sent is the counter data.</span></span> <span data-ttu-id="b3192-107">針對任何兩個範例，將累積的位元組差異除以累積傳輸中的差異，將會產生範例之間每次傳輸的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="b3192-107">For any two samples, dividing the difference of accumulated bytes by the difference in accumulating transfers will produce the average number of bytes per transfer during the period between the samples.</span></span>

<span data-ttu-id="b3192-108">提供下列計數器演算法：</span><span class="sxs-lookup"><span data-stu-id="b3192-108">The following counter algorithms are provided:</span></span>



| <span data-ttu-id="b3192-109">CounterType</span><span class="sxs-lookup"><span data-stu-id="b3192-109">CounterType</span></span>                                                                                              | <span data-ttu-id="b3192-110">Description</span><span class="sxs-lookup"><span data-stu-id="b3192-110">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3192-111">[效能 \_平均 \_ 大量](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073874176</span><span class="sxs-lookup"><span data-stu-id="b3192-111">[PERF\_AVERAGE\_BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176</span></span><br/>       | <span data-ttu-id="b3192-112">在作業期間，平均處理的專案數。</span><span class="sxs-lookup"><span data-stu-id="b3192-112">Number of items processed, on average, during an operation.</span></span> <span data-ttu-id="b3192-113">此計數器類型會顯示已處理之專案的比率 (例如傳送的位元組數) 至已完成的作業數，而且需要具有效能平均基底的基底屬性 \_ \_ 做為計數器類型。</span><span class="sxs-lookup"><span data-stu-id="b3192-113">This counter type displays a ratio of the items processed (such as bytes sent) to the number of operations completed, and requires a base property with PERF\_AVERAGE\_BASE as the counter type.</span></span> |
| <span data-ttu-id="b3192-114">[效能 \_計數器 \_ 計數器](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320</span><span class="sxs-lookup"><span data-stu-id="b3192-114">[PERF\_COUNTER\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320</span></span><br/>     | <span data-ttu-id="b3192-115">取樣間隔的每秒完成的平均作業數。</span><span class="sxs-lookup"><span data-stu-id="b3192-115">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="b3192-116">.</span><span class="sxs-lookup"><span data-stu-id="b3192-116">.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="b3192-117">[效能 \_範例 \_ 計數器](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span><span class="sxs-lookup"><span data-stu-id="b3192-117">[PERF\_SAMPLE\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span></span><br/>        | <span data-ttu-id="b3192-118">每秒完成的平均作業數。</span><span class="sxs-lookup"><span data-stu-id="b3192-118">Average number of operations completed in one second.</span></span> <span data-ttu-id="b3192-119">此計數器類型需要具有性能 \_ 範例基底計數器類型的基底屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3192-119">This counter type requires a base property with the counter type PERF\_SAMPLE\_BASE.</span></span>                                                                                                                   |
| <span data-ttu-id="b3192-120">[效能 \_計數器 \_ BULK \_ COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576</span><span class="sxs-lookup"><span data-stu-id="b3192-120">[PERF\_COUNTER\_BULK\_COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576</span></span><br/> | <span data-ttu-id="b3192-121">取樣間隔的每秒完成的平均作業數。</span><span class="sxs-lookup"><span data-stu-id="b3192-121">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="b3192-122">此計數器類型與性能 \_ 計數器 \_ 計數器類型相同，但是使用較大的欄位來容納較大的值。</span><span class="sxs-lookup"><span data-stu-id="b3192-122">This counter type is the same as the PERF\_COUNTER\_COUNTER type, but it uses larger fields to accommodate larger values.</span></span>                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="b3192-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3192-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3192-124">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="b3192-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

