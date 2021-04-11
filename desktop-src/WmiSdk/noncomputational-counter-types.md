---
description: Noncomputational 計數器類型沒有相關聯的公式。 原始值直接有意義。
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Noncomputational 計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193641"
---
# <a name="noncomputational-counter-types"></a><span data-ttu-id="febc1-104">Noncomputational 計數器類型</span><span class="sxs-lookup"><span data-stu-id="febc1-104">Noncomputational Counter Types</span></span>

<span data-ttu-id="febc1-105">Noncomputational 計數器類型沒有相關聯的公式。</span><span class="sxs-lookup"><span data-stu-id="febc1-105">Noncomputational counter types do not have an associated formula.</span></span> <span data-ttu-id="febc1-106">原始值直接有意義。</span><span class="sxs-lookup"><span data-stu-id="febc1-106">The raw value is directly meaningful.</span></span>

<span data-ttu-id="febc1-107">[**Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)類別中的 **FilesToBeIndexed** 屬性是 **性能 \_ 計數器 \_ RAWCOUNT** 計數器類型的範例。</span><span class="sxs-lookup"><span data-stu-id="febc1-107">The **FilesToBeIndexed** property in the [**Win32\_PerfRawData\_ContentIndex\_IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class is an example of the **PERF\_COUNTER\_RAWCOUNT** counter type.</span></span> <span data-ttu-id="febc1-108">它包含尚未編制索引的檔案計數。</span><span class="sxs-lookup"><span data-stu-id="febc1-108">It contains a count of files that have not been indexed.</span></span>

<span data-ttu-id="febc1-109">計數器類型是由 Winperf 中定義的常數（位於 Microsoft Windows 軟體開發套件 (SDK) ）所指定。</span><span class="sxs-lookup"><span data-stu-id="febc1-109">Counter types are designated by the constant defined in Winperf.h located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="febc1-110">下表列出所提供的 noncomputational 計數器類型。</span><span class="sxs-lookup"><span data-stu-id="febc1-110">The following table lists the noncomputational counter types that are provided.</span></span>



| <span data-ttu-id="febc1-111">CounterType</span><span class="sxs-lookup"><span data-stu-id="febc1-111">CounterType</span></span>                                                                                                 | <span data-ttu-id="febc1-112">Description</span><span class="sxs-lookup"><span data-stu-id="febc1-112">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="febc1-113">[效能 \_計數器 \_ TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span><span class="sxs-lookup"><span data-stu-id="febc1-113">[PERF\_COUNTER\_TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span></span><br/>                | <span data-ttu-id="febc1-114">此計數器類型會以 Unicode 顯示可變長度的文字字串。</span><span class="sxs-lookup"><span data-stu-id="febc1-114">This counter type shows a variable-length text string in Unicode.</span></span> <span data-ttu-id="febc1-115">它不會顯示計算的值。</span><span class="sxs-lookup"><span data-stu-id="febc1-115">It does not display calculated values.</span></span>               |
| <span data-ttu-id="febc1-116">[效能 \_\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536 的計數器</span><span class="sxs-lookup"><span data-stu-id="febc1-116">[PERF\_COUNTER\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536</span></span><br/>           | <span data-ttu-id="febc1-117">不需要計算的原始計數器值，且代表只是最後觀察到之值的一個樣本。</span><span class="sxs-lookup"><span data-stu-id="febc1-117">Raw counter value that does not require calculations, and represents one sample which is the last observed value only.</span></span> |
| <span data-ttu-id="febc1-118">[效能 \_計數器 \_ 大型 \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span><span class="sxs-lookup"><span data-stu-id="febc1-118">[PERF\_COUNTER\_LARGE\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span></span><br/>    | <span data-ttu-id="febc1-119">與 **性能 \_ 計數器 \_ RAWCOUNT** 相同，但較大的值是64位表示。</span><span class="sxs-lookup"><span data-stu-id="febc1-119">Same as **PERF\_COUNTER\_RAWCOUNT**, but a 64-bit representation for larger values.</span></span>                                    |
| <span data-ttu-id="febc1-120">[效能 \_計數器 \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span><span class="sxs-lookup"><span data-stu-id="febc1-120">[PERF\_COUNTER\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span></span><br/>                  | <span data-ttu-id="febc1-121">最近觀察到的十六進位格式值。</span><span class="sxs-lookup"><span data-stu-id="febc1-121">Most recently observed value in hexadecimal format.</span></span> <span data-ttu-id="febc1-122">但不會顯示平均值 </span><span class="sxs-lookup"><span data-stu-id="febc1-122">It does not display an average.</span></span>                                    |
| <span data-ttu-id="febc1-123">[效能 \_計數器 \_ 大型 \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span><span class="sxs-lookup"><span data-stu-id="febc1-123">[PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span></span><br/> | <span data-ttu-id="febc1-124">與 **性能 \_ 計數器 \_ RAWCOUNT \_ HEX** 相同，但十六進位中的64位標記法與大型值搭配使用。</span><span class="sxs-lookup"><span data-stu-id="febc1-124">Same as **PERF\_COUNTER\_RAWCOUNT\_HEX**, but a 64-bit representation in hexadecimal for use with large values.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="febc1-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="febc1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="febc1-126">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="febc1-126">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

