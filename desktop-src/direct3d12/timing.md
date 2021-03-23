---
title: '執行時間 (Direct3D 12 圖形) '
description: 本節涵蓋查詢時間戳記，以及校準 GPU 和 CPU 時間戳計數器。
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/21/2020
ms.locfileid: "104548465"
---
# <a name="timing-direct3d-12-graphics"></a><span data-ttu-id="ad0a9-103">執行時間 (Direct3D 12 圖形) </span><span class="sxs-lookup"><span data-stu-id="ad0a9-103">Timing (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="ad0a9-104">本節涵蓋查詢時間戳記，以及校準 GPU 和 CPU 時間戳計數器。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-104">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span>

## <a name="timestamp-frequency"></a><span data-ttu-id="ad0a9-105">時間戳記頻率</span><span class="sxs-lookup"><span data-stu-id="ad0a9-105">Timestamp frequency</span></span>

<span data-ttu-id="ad0a9-106">您的應用程式可以根據每個命令佇列來查詢 GPU 時間戳記頻率 (請參閱 [**ID3D12CommandQueue：： GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-106">Your application can query the GPU timestamp frequency on a per-command queue basis (refer to the [**ID3D12CommandQueue::GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) method).</span></span>

<span data-ttu-id="ad0a9-107">傳回的頻率是以 Hz (滴答/秒) 來測量。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-107">The returned frequency is measured in Hz (ticks/sec).</span></span> <span data-ttu-id="ad0a9-108">如果指定的命令佇列不支援時間戳記 (請參閱 [ [查詢](queries.md) ] 區段中的表格) ，然後此 API 會失敗 (並傳回 **E_FAIL**) 。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-108">If the specified command queue doesn't support timestamps (see the table in the [Queries](queries.md) section), then this API fails (and returns **E_FAIL**).</span></span> <span data-ttu-id="ad0a9-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) 和 [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) 一律支援時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) always support timestamps.</span></span> <span data-ttu-id="ad0a9-110">如果 [**D3D12_FEATURE_DATA_D3D12_OPTIONS3：： CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3)成員為 **TRUE**， [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)選擇性地支援時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optionally supports timestamps if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

## <a name="timestamp-calibration"></a><span data-ttu-id="ad0a9-111">時間戳記校正</span><span class="sxs-lookup"><span data-stu-id="ad0a9-111">Timestamp calibration</span></span>

<span data-ttu-id="ad0a9-112">D3D12 可讓應用程式將從 timestamp 查詢取得的結果與從呼叫取得的結果相互關聯 `QueryPerformanceCounter` 。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-112">D3D12 enables applications to correlate results obtained from timestamp queries with results obtained from calling `QueryPerformanceCounter`.</span></span> <span data-ttu-id="ad0a9-113">這是由呼叫 [**ID3D12CommandQueue：： GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)啟用。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-113">This is enabled by the call [**ID3D12CommandQueue::GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span></span>

<span data-ttu-id="ad0a9-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) 會取樣指定命令佇列的 GPU timestamp 計數器，並透過 `QueryPerformanceCounter` 幾乎相同的時間取樣 CPU 計數器。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) samples the GPU timestamp counter for a given command queue and samples the CPU counter via `QueryPerformanceCounter` at nearly the same time.</span></span> <span data-ttu-id="ad0a9-115">同樣地，這個 API 會失敗 (傳回 E \_ 失敗) 如果指定的命令佇列不支援時間戳記 (請參閱 [查詢](queries.md) 主題中的表格) 。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-115">Again this API fails (returning E\_FAIL) if the specified command queue does not support timestamps (see the table in the [Queries](queries.md) topic).</span></span>

<span data-ttu-id="ad0a9-116">請注意，GPU 和 CPU 時間戳計數器不一定會與這些處理器的頻率速度直接相關，而是會從時間戳記的刻度進行工作。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-116">Note that GPU and CPU timestamp counters are not necessarily directly related to the clock speed of these processors, but instead work from timestamp ticks.</span></span>

## <a name="timestamp-queries"></a><span data-ttu-id="ad0a9-117">時間戳記查詢</span><span class="sxs-lookup"><span data-stu-id="ad0a9-117">Timestamp queries</span></span>

<span data-ttu-id="ad0a9-118">您可以取得時間戳記作為命令清單的一部分， (而不是透過時間戳記查詢) 命令佇列上的 CPU 端呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-118">You can obtain timestamps as part of a command list (rather than a CPU-side call on a command queue) via timestamp queries.</span></span> <span data-ttu-id="ad0a9-119"> (如 [需查詢的](queries.md) 詳細資訊，請參閱一般) 。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-119">(See [Queries](queries.md) for more information about queries in general).</span></span> 

<span data-ttu-id="ad0a9-120">所有時間戳記查詢都使用實際查詢的類型 [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) 。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-120">All timestamp queries use the type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) for the actual query.</span></span> <span data-ttu-id="ad0a9-121">不過，由於硬體限制的緣故， [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)和 [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)使用 [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)所使用的 D3D12_QUERY_HEAP_TYPE 不同的 [](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) 。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-121">However, due to hardware limitations, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) use a different [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) from the one that [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) uses.</span></span>

<span data-ttu-id="ad0a9-122">直接和計算佇列會使用 [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type)。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-122">Direct and compute queues use [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="ad0a9-123">複製佇列會使用 [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type)。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-123">Copy queues use [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="ad0a9-124">只有當 [**D3D12_FEATURE_DATA_D3D12_OPTIONS3：： CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) 成員為 **TRUE** 時，才支援複製佇列查詢。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-124">Copy queue queries are supported only if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

<span data-ttu-id="ad0a9-125">時間戳記查詢是透過 [**ID3D12GraphicsCommandList：： ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)解析的 UINT64，是代表刻度的 **UINT64** ，如 [**ID3D12CommandQueue：： GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)所傳回，因此必須除以佇列頻率，以秒為單位來取得長度。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-125">Timestamp queries, once resolved via [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), are a **UINT64** that represents ticks, as is returned by [**ID3D12CommandQueue::GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), and as such it must be divided by the queue frequency to get the length in seconds.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad0a9-126">為了精確度，請在計算時間戳記的第二個或毫秒間隔時使用浮點算術。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-126">For accuracy, use floating-point arithmetic when calculating second or millisecond intervals of timestamps.</span></span> <span data-ttu-id="ad0a9-127">例如，請使用 `queriedTicks / (double)Frequency`，而不要使用 `queriedTicks / Frequency`。</span><span class="sxs-lookup"><span data-stu-id="ad0a9-127">For example, use `queriedTicks / (double)Frequency` instead of `queriedTicks / Frequency`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad0a9-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad0a9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad0a9-129">計數器和查詢</span><span class="sxs-lookup"><span data-stu-id="ad0a9-129">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="ad0a9-130">**ID3D12Device::SetStablePowerState**</span><span class="sxs-lookup"><span data-stu-id="ad0a9-130">**ID3D12Device::SetStablePowerState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[<span data-ttu-id="ad0a9-131">**ID3D12Object：： SetName**</span><span class="sxs-lookup"><span data-stu-id="ad0a9-131">**ID3D12Object::SetName**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[<span data-ttu-id="ad0a9-132">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="ad0a9-132">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[<span data-ttu-id="ad0a9-133">效能測量</span><span class="sxs-lookup"><span data-stu-id="ad0a9-133">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>
