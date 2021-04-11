---
description: 使用效能資料時，您會使用下列結構。
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: 效能計數器結構
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944245"
---
# <a name="performance-counters-structures"></a><span data-ttu-id="1a5d5-103">效能計數器結構</span><span class="sxs-lookup"><span data-stu-id="1a5d5-103">Performance Counters Structures</span></span>

<span data-ttu-id="1a5d5-104">使用效能資料時，您會使用下列結構。</span><span class="sxs-lookup"><span data-stu-id="1a5d5-104">You use the following structures when working with performance data.</span></span>

<span data-ttu-id="1a5d5-105">如需有關使用效能計數器之函式的詳細資訊，請參閱 [效能計數器函數](performance-counters-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="1a5d5-105">For information about the functions that are available for working with performance counters, see [Performance Counters Functions](performance-counters-functions.md).</span></span>

## <a name="performance-data-helper-pdh-structures"></a><span data-ttu-id="1a5d5-106">效能資料協助程式 (PDH) 結構</span><span class="sxs-lookup"><span data-stu-id="1a5d5-106">Performance Data Helper (PDH) structures</span></span>

<span data-ttu-id="1a5d5-107">使用 [效能資料協助程式 (PDH) ](using-the-pdh-functions-to-consume-counter-data.md) 函數的取用者會使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="1a5d5-107">Consumers that use the [Performance Data Helper (PDH)](using-the-pdh-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="1a5d5-108">**PDH \_ 流覽 \_ DLG \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-108">**PDH\_BROWSE\_DLG\_CONFIG**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [<span data-ttu-id="1a5d5-109">**PDH \_ 流覽 \_ DLG \_ 設定 \_ H**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-109">**PDH\_BROWSE\_DLG\_CONFIG\_H**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [<span data-ttu-id="1a5d5-110">**PDH \_ 計數器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-110">**PDH\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [<span data-ttu-id="1a5d5-111">**PDH \_ 計數器 \_ 路徑 \_ 元素**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-111">**PDH\_COUNTER\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [<span data-ttu-id="1a5d5-112">**PDH \_ 資料項目 \_ \_ 路徑專案 \_**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-112">**PDH\_DATA\_ITEM\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [<span data-ttu-id="1a5d5-113">**PDH \_ BCP.FMT \_ COUNTERVALUE**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-113">**PDH\_FMT\_COUNTERVALUE**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [<span data-ttu-id="1a5d5-114">**PDH \_ BCP.FMT \_ COUNTERVALUE \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-114">**PDH\_FMT\_COUNTERVALUE\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [<span data-ttu-id="1a5d5-115">**PDH \_ 原始 \_ 計數器**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-115">**PDH\_RAW\_COUNTER**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [<span data-ttu-id="1a5d5-116">**PDH \_ 原始 \_ 計數器 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-116">**PDH\_RAW\_COUNTER\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [<span data-ttu-id="1a5d5-117">**PDH \_ 原始 \_ 記錄檔 \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-117">**PDH\_RAW\_LOG\_RECORD**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [<span data-ttu-id="1a5d5-118">**PDH \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-118">**PDH\_STATISTICS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [<span data-ttu-id="1a5d5-119">**PDH \_ 時間 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-119">**PDH\_TIME\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a><span data-ttu-id="1a5d5-120">PerfLib V2 取用者結構</span><span class="sxs-lookup"><span data-stu-id="1a5d5-120">PerfLib V2 Consumer structures</span></span>

<span data-ttu-id="1a5d5-121">使用 [PerfLib V2 取用者](using-the-perflib-functions-to-consume-counter-data.md) 函式的取用者會使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="1a5d5-121">Consumers that use the [PerfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="1a5d5-122">**性能 \_ 計數器 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-122">**PERF\_COUNTER\_DATA**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [<span data-ttu-id="1a5d5-123">**性能 \_ 計數器 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-123">**PERF\_COUNTER\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [<span data-ttu-id="1a5d5-124">**性能 \_ 計數器 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-124">**PERF\_COUNTER\_IDENTIFIER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [<span data-ttu-id="1a5d5-125">**性能 \_ 計數器 \_ REG \_ INFO**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-125">**PERF\_COUNTER\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [<span data-ttu-id="1a5d5-126">**效能 \_ COUNTERSET \_ REG \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-126">**PERF\_COUNTERSET\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [<span data-ttu-id="1a5d5-127">**效能 \_ 資料 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-127">**PERF\_DATA\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [<span data-ttu-id="1a5d5-128">**效能 \_ 實例 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-128">**PERF\_INSTANCE\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [<span data-ttu-id="1a5d5-129">**效能 \_ 多重 \_ 計數器**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-129">**PERF\_MULTI\_COUNTERS**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [<span data-ttu-id="1a5d5-130">**效能 \_ 多重 \_ 實例**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-130">**PERF\_MULTI\_INSTANCES**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [<span data-ttu-id="1a5d5-131">**效能 \_ 字串 \_ 緩衝區 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-131">**PERF\_STRING\_BUFFER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [<span data-ttu-id="1a5d5-132">**效能 \_ 字串 \_ 計數器 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-132">**PERF\_STRING\_COUNTER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a><span data-ttu-id="1a5d5-133">PerfLib V2 提供者結構</span><span class="sxs-lookup"><span data-stu-id="1a5d5-133">PerfLib V2 Provider structures</span></span>

<span data-ttu-id="1a5d5-134">[V2 效能資料提供者](providing-counter-data-using-version-2-0.md) 會使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="1a5d5-134">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following structures:</span></span>

- [<span data-ttu-id="1a5d5-135">**性能 \_ 計數器身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-135">**PERF\_COUNTER\_IDENTITY**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="1a5d5-136">**性能 \_ 計數器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-136">**PERF\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="1a5d5-137">**效能 \_ COUNTERSET \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-137">**PERF\_COUNTERSET\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="1a5d5-138">**效能 \_ COUNTERSET \_ 實例**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-138">**PERF\_COUNTERSET\_INSTANCE**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [<span data-ttu-id="1a5d5-139">**效能 \_ 提供者 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-139">**PERF\_PROVIDER\_CONTEXT**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a><span data-ttu-id="1a5d5-140">效能 DLL 結構</span><span class="sxs-lookup"><span data-stu-id="1a5d5-140">Performance DLL structures</span></span>

<span data-ttu-id="1a5d5-141">使用登錄函式[來取用計數器資料](using-the-registry-functions-to-consume-counter-data.md)的[效能擴充 DLL 提供](providing-counter-data-using-a-performance-dll.md)者和取用者會使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="1a5d5-141">[Performance extension DLL providers](providing-counter-data-using-a-performance-dll.md) and [consumers that use the registry functions to consume counter data](using-the-registry-functions-to-consume-counter-data.md) use the following structures:</span></span>

- [<span data-ttu-id="1a5d5-142">**性能 \_ 計數器 \_ 區塊**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-142">**PERF\_COUNTER\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [<span data-ttu-id="1a5d5-143">**性能 \_ 計數器 \_ 定義**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-143">**PERF\_COUNTER\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [<span data-ttu-id="1a5d5-144">**效能 \_ 資料 \_ 區塊**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-144">**PERF\_DATA\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [<span data-ttu-id="1a5d5-145">**效能 \_ 實例 \_ 定義**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-145">**PERF\_INSTANCE\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [<span data-ttu-id="1a5d5-146">**性能 \_ 物件 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="1a5d5-146">**PERF\_OBJECT\_TYPE**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
