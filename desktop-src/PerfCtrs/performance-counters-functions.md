---
description: 使用下列函數來取用和提供效能資料。
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: 效能計數器函式
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969360"
---
# <a name="performance-counters-functions"></a><span data-ttu-id="12426-103">效能計數器函式</span><span class="sxs-lookup"><span data-stu-id="12426-103">Performance Counters Functions</span></span>

<span data-ttu-id="12426-104">使用下列函數來取用和提供效能資料。</span><span class="sxs-lookup"><span data-stu-id="12426-104">Use the following functions to consume and provide performance data.</span></span>

## <a name="consumer-functions"></a><span data-ttu-id="12426-105">取用者函式</span><span class="sxs-lookup"><span data-stu-id="12426-105">Consumer functions</span></span>

### <a name="performance-data-helper-pdh-functions"></a><span data-ttu-id="12426-106">效能資料協助程式 (PDH) 函數</span><span class="sxs-lookup"><span data-stu-id="12426-106">Performance Data Helper (PDH) functions</span></span>

<span data-ttu-id="12426-107">使用效能資料協助程式 (PDH) 函式來取用 V1 和 V2 效能資料提供者的效能資料。</span><span class="sxs-lookup"><span data-stu-id="12426-107">Use the Performance Data Helper (PDH) functions to consume performance data from both V1 and V2 performance data providers.</span></span>

> [!Note]
> <span data-ttu-id="12426-108">Windows OneCore 的應用程式無法使用 PDH 函數。</span><span class="sxs-lookup"><span data-stu-id="12426-108">Windows OneCore apps cannot use the PDH functions.</span></span> <span data-ttu-id="12426-109">如果您正在撰寫 Windows OneCore 的應用程式，請使用 [PerfLib V2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式。</span><span class="sxs-lookup"><span data-stu-id="12426-109">If you are writing Windows OneCore apps, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

- [<span data-ttu-id="12426-110">*CounterPathCallBack*</span><span class="sxs-lookup"><span data-stu-id="12426-110">*CounterPathCallBack*</span></span>](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [<span data-ttu-id="12426-111">**PdhAddCounter**</span><span class="sxs-lookup"><span data-stu-id="12426-111">**PdhAddCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [<span data-ttu-id="12426-112">**PdhAddEnglishCounter**</span><span class="sxs-lookup"><span data-stu-id="12426-112">**PdhAddEnglishCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [<span data-ttu-id="12426-113">**PdhBindInputDataSource**</span><span class="sxs-lookup"><span data-stu-id="12426-113">**PdhBindInputDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [<span data-ttu-id="12426-114">**PdhBrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="12426-114">**PdhBrowseCounters**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [<span data-ttu-id="12426-115">**PdhBrowseCountersH**</span><span class="sxs-lookup"><span data-stu-id="12426-115">**PdhBrowseCountersH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [<span data-ttu-id="12426-116">**PdhCalculateCounterFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="12426-116">**PdhCalculateCounterFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [<span data-ttu-id="12426-117">**PdhCloseLog**</span><span class="sxs-lookup"><span data-stu-id="12426-117">**PdhCloseLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [<span data-ttu-id="12426-118">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="12426-118">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="12426-119">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="12426-119">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="12426-120">**PdhCollectQueryDataEx**</span><span class="sxs-lookup"><span data-stu-id="12426-120">**PdhCollectQueryDataEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [<span data-ttu-id="12426-121">**PdhCollectQueryDataWithTime**</span><span class="sxs-lookup"><span data-stu-id="12426-121">**PdhCollectQueryDataWithTime**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [<span data-ttu-id="12426-122">**PdhComputeCounterStatistics**</span><span class="sxs-lookup"><span data-stu-id="12426-122">**PdhComputeCounterStatistics**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [<span data-ttu-id="12426-123">**PdhConnectMachine**</span><span class="sxs-lookup"><span data-stu-id="12426-123">**PdhConnectMachine**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [<span data-ttu-id="12426-124">**PdhEnumLogSetNames**</span><span class="sxs-lookup"><span data-stu-id="12426-124">**PdhEnumLogSetNames**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [<span data-ttu-id="12426-125">**PdhEnumMachines**</span><span class="sxs-lookup"><span data-stu-id="12426-125">**PdhEnumMachines**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [<span data-ttu-id="12426-126">**PdhEnumMachinesH**</span><span class="sxs-lookup"><span data-stu-id="12426-126">**PdhEnumMachinesH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [<span data-ttu-id="12426-127">**PdhEnumObjectItems**</span><span class="sxs-lookup"><span data-stu-id="12426-127">**PdhEnumObjectItems**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [<span data-ttu-id="12426-128">**PdhEnumObjectItemsH**</span><span class="sxs-lookup"><span data-stu-id="12426-128">**PdhEnumObjectItemsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [<span data-ttu-id="12426-129">**PdhEnumObjects**</span><span class="sxs-lookup"><span data-stu-id="12426-129">**PdhEnumObjects**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [<span data-ttu-id="12426-130">**PdhEnumObjectsH**</span><span class="sxs-lookup"><span data-stu-id="12426-130">**PdhEnumObjectsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [<span data-ttu-id="12426-131">**PdhExpandCounterPath**</span><span class="sxs-lookup"><span data-stu-id="12426-131">**PdhExpandCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [<span data-ttu-id="12426-132">**PdhExpandWildCardPath**</span><span class="sxs-lookup"><span data-stu-id="12426-132">**PdhExpandWildCardPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [<span data-ttu-id="12426-133">**PdhExpandWildCardPathH**</span><span class="sxs-lookup"><span data-stu-id="12426-133">**PdhExpandWildCardPathH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [<span data-ttu-id="12426-134">**PdhFormatFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="12426-134">**PdhFormatFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [<span data-ttu-id="12426-135">**PdhGetCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="12426-135">**PdhGetCounterInfo**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [<span data-ttu-id="12426-136">**PdhGetCounterTimeBase**</span><span class="sxs-lookup"><span data-stu-id="12426-136">**PdhGetCounterTimeBase**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [<span data-ttu-id="12426-137">**PdhGetDataSourceTimeRange**</span><span class="sxs-lookup"><span data-stu-id="12426-137">**PdhGetDataSourceTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [<span data-ttu-id="12426-138">**PdhGetDataSourceTimeRangeH**</span><span class="sxs-lookup"><span data-stu-id="12426-138">**PdhGetDataSourceTimeRangeH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [<span data-ttu-id="12426-139">**PdhGetDefaultPerfCounter**</span><span class="sxs-lookup"><span data-stu-id="12426-139">**PdhGetDefaultPerfCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [<span data-ttu-id="12426-140">**PdhGetDefaultPerfCounterH**</span><span class="sxs-lookup"><span data-stu-id="12426-140">**PdhGetDefaultPerfCounterH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [<span data-ttu-id="12426-141">**PdhGetDefaultPerfObject**</span><span class="sxs-lookup"><span data-stu-id="12426-141">**PdhGetDefaultPerfObject**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [<span data-ttu-id="12426-142">**PdhGetDefaultPerfObjectH**</span><span class="sxs-lookup"><span data-stu-id="12426-142">**PdhGetDefaultPerfObjectH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [<span data-ttu-id="12426-143">**PdhGetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="12426-143">**PdhGetDllVersion**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [<span data-ttu-id="12426-144">**PdhGetFormattedCounterArray**</span><span class="sxs-lookup"><span data-stu-id="12426-144">**PdhGetFormattedCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [<span data-ttu-id="12426-145">**PdhGetFormattedCounterValue**</span><span class="sxs-lookup"><span data-stu-id="12426-145">**PdhGetFormattedCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [<span data-ttu-id="12426-146">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="12426-146">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [<span data-ttu-id="12426-147">**PdhGetRawCounterArray**</span><span class="sxs-lookup"><span data-stu-id="12426-147">**PdhGetRawCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [<span data-ttu-id="12426-148">**PdhGetRawCounterValue**</span><span class="sxs-lookup"><span data-stu-id="12426-148">**PdhGetRawCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [<span data-ttu-id="12426-149">**PdhIsRealTimeQuery**</span><span class="sxs-lookup"><span data-stu-id="12426-149">**PdhIsRealTimeQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [<span data-ttu-id="12426-150">**PdhLookupPerfIndexByName**</span><span class="sxs-lookup"><span data-stu-id="12426-150">**PdhLookupPerfIndexByName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [<span data-ttu-id="12426-151">**PdhLookupPerfNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="12426-151">**PdhLookupPerfNameByIndex**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [<span data-ttu-id="12426-152">**PdhMakeCounterPath**</span><span class="sxs-lookup"><span data-stu-id="12426-152">**PdhMakeCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [<span data-ttu-id="12426-153">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="12426-153">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [<span data-ttu-id="12426-154">**PdhOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="12426-154">**PdhOpenQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [<span data-ttu-id="12426-155">**PdhOpenQueryH**</span><span class="sxs-lookup"><span data-stu-id="12426-155">**PdhOpenQueryH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [<span data-ttu-id="12426-156">**PdhParseCounterPath**</span><span class="sxs-lookup"><span data-stu-id="12426-156">**PdhParseCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [<span data-ttu-id="12426-157">**PdhParseInstanceName**</span><span class="sxs-lookup"><span data-stu-id="12426-157">**PdhParseInstanceName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [<span data-ttu-id="12426-158">**PdhReadRawLogRecord**</span><span class="sxs-lookup"><span data-stu-id="12426-158">**PdhReadRawLogRecord**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [<span data-ttu-id="12426-159">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="12426-159">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="12426-160">**PdhSelectDataSource**</span><span class="sxs-lookup"><span data-stu-id="12426-160">**PdhSelectDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [<span data-ttu-id="12426-161">**PdhSetCounterScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="12426-161">**PdhSetCounterScaleFactor**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [<span data-ttu-id="12426-162">**PdhSetDefaultRealTimeDataSource**</span><span class="sxs-lookup"><span data-stu-id="12426-162">**PdhSetDefaultRealTimeDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [<span data-ttu-id="12426-163">**PdhSetQueryTimeRange**</span><span class="sxs-lookup"><span data-stu-id="12426-163">**PdhSetQueryTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [<span data-ttu-id="12426-164">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="12426-164">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [<span data-ttu-id="12426-165">**PdhUpdateLogFileCatalog**</span><span class="sxs-lookup"><span data-stu-id="12426-165">**PdhUpdateLogFileCatalog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [<span data-ttu-id="12426-166">**PdhValidatePath**</span><span class="sxs-lookup"><span data-stu-id="12426-166">**PdhValidatePath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [<span data-ttu-id="12426-167">**PdhValidatePathEx**</span><span class="sxs-lookup"><span data-stu-id="12426-167">**PdhValidatePathEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a><span data-ttu-id="12426-168">PerfLib V2 取用者函式</span><span class="sxs-lookup"><span data-stu-id="12426-168">PerfLib V2 Consumer functions</span></span>

<span data-ttu-id="12426-169">如果您無法使用效能資料協助程式 (PDH) 函數，請使用 PerfLib V2 取用者函式來取用 V2 效能資料提供者的效能資料。</span><span class="sxs-lookup"><span data-stu-id="12426-169">Use the PerfLib V2 Consumer functions to consume performance data from V2 performance data providers if you cannot use the Performance Data Helper (PDH) functions.</span></span> <span data-ttu-id="12426-170">當您撰寫 OneCore 的應用程式來收集 V2 countersets，或當您需要以基本的相依性和額外負荷收集特定 V2 countersets 時，可能會使用這些函數。</span><span class="sxs-lookup"><span data-stu-id="12426-170">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect specific V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="12426-171">PerfLib V2 取用者函式比效能資料協助程式更難使用 (PDH) 函式，且僅支援從 V2 提供者收集資料。</span><span class="sxs-lookup"><span data-stu-id="12426-171">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="12426-172">大部分的應用程式都應該偏好 PDH 函數。</span><span class="sxs-lookup"><span data-stu-id="12426-172">The PDH functions should be preferred for most applications.</span></span>

- [<span data-ttu-id="12426-173">**PerfAddCounters**</span><span class="sxs-lookup"><span data-stu-id="12426-173">**PerfAddCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [<span data-ttu-id="12426-174">**PerfCloseQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="12426-174">**PerfCloseQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [<span data-ttu-id="12426-175">**PerfDeleteCounters**</span><span class="sxs-lookup"><span data-stu-id="12426-175">**PerfDeleteCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [<span data-ttu-id="12426-176">**PerfEnumerateCounterSet**</span><span class="sxs-lookup"><span data-stu-id="12426-176">**PerfEnumerateCounterSet**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [<span data-ttu-id="12426-177">**PerfEnumerateCounterSetInstances**</span><span class="sxs-lookup"><span data-stu-id="12426-177">**PerfEnumerateCounterSetInstances**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [<span data-ttu-id="12426-178">**PerfOpenQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="12426-178">**PerfOpenQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [<span data-ttu-id="12426-179">**PerfQueryCounterData**</span><span class="sxs-lookup"><span data-stu-id="12426-179">**PerfQueryCounterData**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [<span data-ttu-id="12426-180">**PerfQueryCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="12426-180">**PerfQueryCounterInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [<span data-ttu-id="12426-181">**PerfQueryCounterSetRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="12426-181">**PerfQueryCounterSetRegistrationInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a><span data-ttu-id="12426-182">提供者函式</span><span class="sxs-lookup"><span data-stu-id="12426-182">Provider functions</span></span>

### <a name="perflib-v2-provider-functions"></a><span data-ttu-id="12426-183">PerfLib V2 提供者函式</span><span class="sxs-lookup"><span data-stu-id="12426-183">PerfLib V2 Provider functions</span></span>

<span data-ttu-id="12426-184">[V2 效能資料提供者](providing-counter-data-using-version-2-0.md) 使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="12426-184">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following functions:</span></span>

- [<span data-ttu-id="12426-185">*AllocateMemory*</span><span class="sxs-lookup"><span data-stu-id="12426-185">*AllocateMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [<span data-ttu-id="12426-186">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="12426-186">*ControlCallback*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="12426-187">**CounterCleanup**</span><span class="sxs-lookup"><span data-stu-id="12426-187">**CounterCleanup**</span></span>](countercleanup.md)
- [<span data-ttu-id="12426-188">**CounterInitialize**</span><span class="sxs-lookup"><span data-stu-id="12426-188">**CounterInitialize**</span></span>](counterinitialize.md)
- [<span data-ttu-id="12426-189">*FreeMemory*</span><span class="sxs-lookup"><span data-stu-id="12426-189">*FreeMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [<span data-ttu-id="12426-190">**PerfCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="12426-190">**PerfCreateInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="12426-191">**PerfDecrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="12426-191">**PerfDecrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [<span data-ttu-id="12426-192">**PerfDecrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="12426-192">**PerfDecrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [<span data-ttu-id="12426-193">**PerfDeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="12426-193">**PerfDeleteInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="12426-194">**PerfIncrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="12426-194">**PerfIncrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [<span data-ttu-id="12426-195">**PerfIncrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="12426-195">**PerfIncrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [<span data-ttu-id="12426-196">**PerfQueryInstance**</span><span class="sxs-lookup"><span data-stu-id="12426-196">**PerfQueryInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="12426-197">**PerfSetCounterSetInfo**</span><span class="sxs-lookup"><span data-stu-id="12426-197">**PerfSetCounterSetInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="12426-198">**PerfSetULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="12426-198">**PerfSetULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="12426-199">**PerfSetULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="12426-199">**PerfSetULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="12426-200">**PerfSetCounterRefValue**</span><span class="sxs-lookup"><span data-stu-id="12426-200">**PerfSetCounterRefValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="12426-201">**PerfStartProvider**</span><span class="sxs-lookup"><span data-stu-id="12426-201">**PerfStartProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="12426-202">**PerfStartProviderEx**</span><span class="sxs-lookup"><span data-stu-id="12426-202">**PerfStartProviderEx**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [<span data-ttu-id="12426-203">**PerfStopProvider**</span><span class="sxs-lookup"><span data-stu-id="12426-203">**PerfStopProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> <span data-ttu-id="12426-204">若要安裝和卸載 V2 提供者，請使用 **lodctr** 和 **unlodctr** 工具。</span><span class="sxs-lookup"><span data-stu-id="12426-204">To install and uninstall V2 providers, use the **lodctr** and **unlodctr** tools.</span></span> <span data-ttu-id="12426-205">**LoadPerfCounterTextStrings** 和 **UnloadPerfCounterTextStrings** 函數不能用來安裝和卸載 V2 提供者。</span><span class="sxs-lookup"><span data-stu-id="12426-205">The **LoadPerfCounterTextStrings** and **UnloadPerfCounterTextStrings** functions cannot be used to install and uninstall V2 providers.</span></span>

### <a name="performance-dll-functions"></a><span data-ttu-id="12426-206">效能 DLL 函數</span><span class="sxs-lookup"><span data-stu-id="12426-206">Performance DLL functions</span></span>

<span data-ttu-id="12426-207">[V1 效能資料提供者](providing-counter-data-using-a-performance-dll.md) 會執行提供下列功能的 DLL：</span><span class="sxs-lookup"><span data-stu-id="12426-207">[V1 performance data providers](providing-counter-data-using-a-performance-dll.md) implement a DLL that provides the following functions:</span></span>

- [<span data-ttu-id="12426-208">*ClosePerformanceData*</span><span class="sxs-lookup"><span data-stu-id="12426-208">*ClosePerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [<span data-ttu-id="12426-209">*CollectPerformanceData*</span><span class="sxs-lookup"><span data-stu-id="12426-209">*CollectPerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- <span data-ttu-id="12426-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12426-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span></span>

> [!Note]
> <span data-ttu-id="12426-211">由於有顯著的效能和可靠性問題，因此 V1 效能資料提供者已被取代。</span><span class="sxs-lookup"><span data-stu-id="12426-211">Due to significant performance and reliability issues, V1 performance data providers are deprecated.</span></span> <span data-ttu-id="12426-212">雖然您仍然可以使用效能擴充 DLL 來提供計數器資料，但建議您改為 [建立 V2 提供者](providing-counter-data-using-version-2-0.md) 。</span><span class="sxs-lookup"><span data-stu-id="12426-212">Although you still can use a performance extension DLL to provide counter data, you are encouraged to [create a V2 provider](providing-counter-data-using-version-2-0.md) instead.</span></span> <span data-ttu-id="12426-213">您也鼓勵您將現有的 V1 提供者取代為 V2 提供者。</span><span class="sxs-lookup"><span data-stu-id="12426-213">You also are encouraged to replace existing V1 providers with V2 providers.</span></span>

<span data-ttu-id="12426-214">您可以使用 **lodctr** 和 **unlodctr** 工具，或藉由呼叫下列函式，來安裝和卸載 V1 提供者：</span><span class="sxs-lookup"><span data-stu-id="12426-214">V1 providers can be installed and uninstalled using the **lodctr** and **unlodctr** tools or by calling the following functions:</span></span>

- [<span data-ttu-id="12426-215">**LoadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="12426-215">**LoadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [<span data-ttu-id="12426-216">**UnloadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="12426-216">**UnloadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
