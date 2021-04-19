---
description: CounterType 限定詞包含 Win32 PerfRawData 類別中屬性之屬性計數器類型的整數值 \_ 。 CookingType 包含 Win32 PerfFormattedData 類別中屬性公式類型的常數 \_ 。
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: CounterType 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982353"
---
# <a name="countertype-qualifier"></a><span data-ttu-id="a581e-104">CounterType 辨識符號</span><span class="sxs-lookup"><span data-stu-id="a581e-104">CounterType Qualifier</span></span>

<span data-ttu-id="a581e-105">**CounterType** 限定詞包含 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中屬性之屬性計數器類型的整數值。</span><span class="sxs-lookup"><span data-stu-id="a581e-105">The **CounterType** qualifier contains the integer value for the property counter type for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span> <span data-ttu-id="a581e-106">**CookingType** 包含 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別中屬性公式類型的常數。</span><span class="sxs-lookup"><span data-stu-id="a581e-106">The **CookingType** contains the constants for property formula types in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="a581e-107">如需詳細資訊和依函數的計數器類型細目，請參閱 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="a581e-107">For more information and a breakdown of counter types by function, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>



| <span data-ttu-id="a581e-108">CounterType</span><span class="sxs-lookup"><span data-stu-id="a581e-108">CounterType</span></span> | <span data-ttu-id="a581e-109">CookingType</span><span class="sxs-lookup"><span data-stu-id="a581e-109">CookingType</span></span>                              |
|-------------|------------------------------------------|
| <span data-ttu-id="a581e-110">0</span><span class="sxs-lookup"><span data-stu-id="a581e-110">0</span></span>           | <span data-ttu-id="a581e-111">性能 \_ 計數器 \_ RAWCOUNT \_ HEX</span><span class="sxs-lookup"><span data-stu-id="a581e-111">PERF\_COUNTER\_RAWCOUNT\_HEX</span></span>             |
| <span data-ttu-id="a581e-112">256</span><span class="sxs-lookup"><span data-stu-id="a581e-112">256</span></span>         | <span data-ttu-id="a581e-113">性能 \_ 計數器 \_ 大型 \_ RAWCOUNT \_ HEX</span><span class="sxs-lookup"><span data-stu-id="a581e-113">PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX</span></span>      |
| <span data-ttu-id="a581e-114">2816</span><span class="sxs-lookup"><span data-stu-id="a581e-114">2816</span></span>        | <span data-ttu-id="a581e-115">性能 \_ 計數器 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="a581e-115">PERF\_COUNTER\_TEXT</span></span>                      |
| <span data-ttu-id="a581e-116">65536</span><span class="sxs-lookup"><span data-stu-id="a581e-116">65536</span></span>       | <span data-ttu-id="a581e-117">性能 \_ 計數器 \_ RAWCOUNT</span><span class="sxs-lookup"><span data-stu-id="a581e-117">PERF\_COUNTER\_RAWCOUNT</span></span>                  |
| <span data-ttu-id="a581e-118">65792</span><span class="sxs-lookup"><span data-stu-id="a581e-118">65792</span></span>       | <span data-ttu-id="a581e-119">性能 \_ 計數器 \_ 大型 \_ RAWCOUNT</span><span class="sxs-lookup"><span data-stu-id="a581e-119">PERF\_COUNTER\_LARGE\_RAWCOUNT</span></span>           |
| <span data-ttu-id="a581e-120">73728</span><span class="sxs-lookup"><span data-stu-id="a581e-120">73728</span></span>       | <span data-ttu-id="a581e-121">效能 \_ 雙重 \_ 原始</span><span class="sxs-lookup"><span data-stu-id="a581e-121">PERF\_DOUBLE\_RAW</span></span>                        |
| <span data-ttu-id="a581e-122">4195328</span><span class="sxs-lookup"><span data-stu-id="a581e-122">4195328</span></span>     | <span data-ttu-id="a581e-123">性能 \_ 計數器 \_ DELTA</span><span class="sxs-lookup"><span data-stu-id="a581e-123">PERF\_COUNTER\_DELTA</span></span>                     |
| <span data-ttu-id="a581e-124">4195584</span><span class="sxs-lookup"><span data-stu-id="a581e-124">4195584</span></span>     | <span data-ttu-id="a581e-125">性能 \_ 計數器 \_ 大型 \_ 差異</span><span class="sxs-lookup"><span data-stu-id="a581e-125">PERF\_COUNTER\_LARGE\_DELTA</span></span>              |
| <span data-ttu-id="a581e-126">4260864</span><span class="sxs-lookup"><span data-stu-id="a581e-126">4260864</span></span>     | <span data-ttu-id="a581e-127">效能 \_ 範例 \_ 計數器</span><span class="sxs-lookup"><span data-stu-id="a581e-127">PERF\_SAMPLE\_COUNTER</span></span>                    |
| <span data-ttu-id="a581e-128">4523008</span><span class="sxs-lookup"><span data-stu-id="a581e-128">4523008</span></span>     | <span data-ttu-id="a581e-129">性能 \_ 計數器 \_ QUEUELEN \_ 類型</span><span class="sxs-lookup"><span data-stu-id="a581e-129">PERF\_COUNTER\_QUEUELEN\_TYPE</span></span>            |
| <span data-ttu-id="a581e-130">4523264</span><span class="sxs-lookup"><span data-stu-id="a581e-130">4523264</span></span>     | <span data-ttu-id="a581e-131">性能 \_ 計數器 \_ 大型 \_ QUEUELEN \_ 類型</span><span class="sxs-lookup"><span data-stu-id="a581e-131">PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="a581e-132">5571840</span><span class="sxs-lookup"><span data-stu-id="a581e-132">5571840</span></span>     | <span data-ttu-id="a581e-133">性能 \_ 計數器 \_ 100ns \_ QUEUELEN \_ 類型</span><span class="sxs-lookup"><span data-stu-id="a581e-133">PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="a581e-134">6620416</span><span class="sxs-lookup"><span data-stu-id="a581e-134">6620416</span></span>     | <span data-ttu-id="a581e-135">性能 \_ 計數器 \_ OBJ \_ TIME \_ QUEUELEN \_ 類型</span><span class="sxs-lookup"><span data-stu-id="a581e-135">PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE</span></span> |
| <span data-ttu-id="a581e-136">272696320</span><span class="sxs-lookup"><span data-stu-id="a581e-136">272696320</span></span>   | <span data-ttu-id="a581e-137">性能 \_ 計數器 \_ 計數器</span><span class="sxs-lookup"><span data-stu-id="a581e-137">PERF\_COUNTER\_COUNTER</span></span>                   |
| <span data-ttu-id="a581e-138">272696576</span><span class="sxs-lookup"><span data-stu-id="a581e-138">272696576</span></span>   | <span data-ttu-id="a581e-139">性能 \_ 計數器 \_ 大量 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="a581e-139">PERF\_COUNTER\_BULK\_COUNT</span></span>               |
| <span data-ttu-id="a581e-140">537003008</span><span class="sxs-lookup"><span data-stu-id="a581e-140">537003008</span></span>   | <span data-ttu-id="a581e-141">效能 \_ 原始 \_ 分數</span><span class="sxs-lookup"><span data-stu-id="a581e-141">PERF\_RAW\_FRACTION</span></span>                      |
| <span data-ttu-id="a581e-142">541132032</span><span class="sxs-lookup"><span data-stu-id="a581e-142">541132032</span></span>   | <span data-ttu-id="a581e-143">性能 \_ 計數器 \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-143">PERF\_COUNTER\_TIMER</span></span>                     |
| <span data-ttu-id="a581e-144">541525248</span><span class="sxs-lookup"><span data-stu-id="a581e-144">541525248</span></span>   | <span data-ttu-id="a581e-145">效能 \_ 精確度 \_ 系統 \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-145">PERF\_PRECISION\_SYSTEM\_TIMER</span></span>           |
| <span data-ttu-id="a581e-146">542180608</span><span class="sxs-lookup"><span data-stu-id="a581e-146">542180608</span></span>   | <span data-ttu-id="a581e-147">效能 \_ 100NSEC \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-147">PERF\_100NSEC\_TIMER</span></span>                     |
| <span data-ttu-id="a581e-148">542573824</span><span class="sxs-lookup"><span data-stu-id="a581e-148">542573824</span></span>   | <span data-ttu-id="a581e-149">效能 \_ 精確度 \_ 100ns \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-149">PERF\_PRECISION\_100NS\_TIMER</span></span>            |
| <span data-ttu-id="a581e-150">543229184</span><span class="sxs-lookup"><span data-stu-id="a581e-150">543229184</span></span>   | <span data-ttu-id="a581e-151">效能 \_ OBJ \_ 時間 \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-151">PERF\_OBJ\_TIME\_TIMER</span></span>                   |
| <span data-ttu-id="a581e-152">543622400</span><span class="sxs-lookup"><span data-stu-id="a581e-152">543622400</span></span>   | <span data-ttu-id="a581e-153">效能 \_ 精確度 \_ 物件 \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-153">PERF\_PRECISION\_OBJECT\_TIMER</span></span>           |
| <span data-ttu-id="a581e-154">549585920</span><span class="sxs-lookup"><span data-stu-id="a581e-154">549585920</span></span>   | <span data-ttu-id="a581e-155">效能 \_ 範例 \_ 分數</span><span class="sxs-lookup"><span data-stu-id="a581e-155">PERF\_SAMPLE\_FRACTION</span></span>                   |
| <span data-ttu-id="a581e-156">557909248</span><span class="sxs-lookup"><span data-stu-id="a581e-156">557909248</span></span>   | <span data-ttu-id="a581e-157">性能 \_ 計數器 \_ 計時器 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="a581e-157">PERF\_COUNTER\_TIMER\_INV</span></span>                |
| <span data-ttu-id="a581e-158">558957824</span><span class="sxs-lookup"><span data-stu-id="a581e-158">558957824</span></span>   | <span data-ttu-id="a581e-159">效能 \_ 100NSEC \_ 計時器 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="a581e-159">PERF\_100NSEC\_TIMER\_INV</span></span>                |
| <span data-ttu-id="a581e-160">574686464</span><span class="sxs-lookup"><span data-stu-id="a581e-160">574686464</span></span>   | <span data-ttu-id="a581e-161">性能 \_ 計數器 \_ 多重 \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-161">PERF\_COUNTER\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="a581e-162">575735040</span><span class="sxs-lookup"><span data-stu-id="a581e-162">575735040</span></span>   | <span data-ttu-id="a581e-163">效能 \_ 100NSEC \_ 多重 \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-163">PERF\_100NSEC\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="a581e-164">591463680</span><span class="sxs-lookup"><span data-stu-id="a581e-164">591463680</span></span>   | <span data-ttu-id="a581e-165">性能 \_ 計數器 \_ 多重 \_ 計時器 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="a581e-165">PERF\_COUNTER\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="a581e-166">592512256</span><span class="sxs-lookup"><span data-stu-id="a581e-166">592512256</span></span>   | <span data-ttu-id="a581e-167">效能 \_ 100NSEC \_ 多重 \_ 計時器 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="a581e-167">PERF\_100NSEC\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="a581e-168">805438464</span><span class="sxs-lookup"><span data-stu-id="a581e-168">805438464</span></span>   | <span data-ttu-id="a581e-169">效能 \_ 平均 \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="a581e-169">PERF\_AVERAGE\_TIMER</span></span>                     |
| <span data-ttu-id="a581e-170">807666944</span><span class="sxs-lookup"><span data-stu-id="a581e-170">807666944</span></span>   | <span data-ttu-id="a581e-171">效能 \_ 經過 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="a581e-171">PERF\_ELAPSED\_TIME</span></span>                      |
| <span data-ttu-id="a581e-172">1073742336</span><span class="sxs-lookup"><span data-stu-id="a581e-172">1073742336</span></span>  | <span data-ttu-id="a581e-173">性能 \_ 計數器 \_ NODATA</span><span class="sxs-lookup"><span data-stu-id="a581e-173">PERF\_COUNTER\_NODATA</span></span>                    |
| <span data-ttu-id="a581e-174">1073874176</span><span class="sxs-lookup"><span data-stu-id="a581e-174">1073874176</span></span>  | <span data-ttu-id="a581e-175">效能 \_ 平均 \_ 大量</span><span class="sxs-lookup"><span data-stu-id="a581e-175">PERF\_AVERAGE\_BULK</span></span>                      |
| <span data-ttu-id="a581e-176">1073939457</span><span class="sxs-lookup"><span data-stu-id="a581e-176">1073939457</span></span>  | <span data-ttu-id="a581e-177">效能 \_ 範例 \_ 基底</span><span class="sxs-lookup"><span data-stu-id="a581e-177">PERF\_SAMPLE\_BASE</span></span>                       |
| <span data-ttu-id="a581e-178">1073939458</span><span class="sxs-lookup"><span data-stu-id="a581e-178">1073939458</span></span>  | <span data-ttu-id="a581e-179">效能 \_ 平均 \_ 基底</span><span class="sxs-lookup"><span data-stu-id="a581e-179">PERF\_AVERAGE\_BASE</span></span>                      |
| <span data-ttu-id="a581e-180">1073939459</span><span class="sxs-lookup"><span data-stu-id="a581e-180">1073939459</span></span>  | <span data-ttu-id="a581e-181">性能 \_ 原始 \_ 基底</span><span class="sxs-lookup"><span data-stu-id="a581e-181">PERF\_RAW\_BASE</span></span>                          |
| <span data-ttu-id="a581e-182">1073939712</span><span class="sxs-lookup"><span data-stu-id="a581e-182">1073939712</span></span>  | <span data-ttu-id="a581e-183">效能 \_ 精確度 \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="a581e-183">PERF\_PRECISION\_TIMESTAMP</span></span>               |
| <span data-ttu-id="a581e-184">1073939715</span><span class="sxs-lookup"><span data-stu-id="a581e-184">1073939715</span></span>  | <span data-ttu-id="a581e-185">效能 \_ 大型 \_ 原始 \_ 基底</span><span class="sxs-lookup"><span data-stu-id="a581e-185">PERF\_LARGE\_RAW\_BASE</span></span>                   |
| <span data-ttu-id="a581e-186">1107494144</span><span class="sxs-lookup"><span data-stu-id="a581e-186">1107494144</span></span>  | <span data-ttu-id="a581e-187">性能 \_ 計數器 \_ 多個 \_ 基底</span><span class="sxs-lookup"><span data-stu-id="a581e-187">PERF\_COUNTER\_MULTI\_BASE</span></span>               |
| <span data-ttu-id="a581e-188">2147483648</span><span class="sxs-lookup"><span data-stu-id="a581e-188">2147483648</span></span>  | <span data-ttu-id="a581e-189">性能 \_ 計數器 \_ 長條圖 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="a581e-189">PERF\_COUNTER\_HISTOGRAM\_TYPE</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="a581e-190">規格需求</span><span class="sxs-lookup"><span data-stu-id="a581e-190">Requirements</span></span>



| <span data-ttu-id="a581e-191">需求</span><span class="sxs-lookup"><span data-stu-id="a581e-191">Requirement</span></span> | <span data-ttu-id="a581e-192">值</span><span class="sxs-lookup"><span data-stu-id="a581e-192">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a581e-193">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a581e-193">Minimum supported client</span></span><br/> | <span data-ttu-id="a581e-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a581e-194">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a581e-195">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a581e-195">Minimum supported server</span></span><br/> | <span data-ttu-id="a581e-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a581e-196">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a581e-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a581e-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a581e-198">WMI 效能類別專用的限定詞</span><span class="sxs-lookup"><span data-stu-id="a581e-198">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

