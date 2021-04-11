---
title: 'MPCALLBACK_DATA 結構 (MpClient .h) '
description: 傳遞至回呼函數的資料。
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA 結構舊版 Windows 環境功能
- PMPCALLBACK_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094516"
---
# <a name="mpcallback_data-structure"></a><span data-ttu-id="ba0e6-105">MPCALLBACK \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="ba0e6-105">MPCALLBACK\_DATA structure</span></span>

<span data-ttu-id="ba0e6-106">傳遞至回呼函數的資料。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-106">Data passed to the callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0e6-107">語法</span><span class="sxs-lookup"><span data-stu-id="ba0e6-107">Syntax</span></span>


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a><span data-ttu-id="ba0e6-108">成員</span><span class="sxs-lookup"><span data-stu-id="ba0e6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba0e6-109">**通知**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-109">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-110">類型： **[ **MPNOTIFY**](mpnotify.md)**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-110">Type: **[**MPNOTIFY**](mpnotify.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-111">將通知變更為 [報表]。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-111">Change notification to report.</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-112">**hResult**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-114">如果發生內部失敗，則為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-114">Error code, in case of an internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-115">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-115">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-116">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-116">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-117">目前的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-117">Current timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-118">**型別**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-118">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-119">類型： **[ **MPCALLBACK \_ 類型**](mpcallback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-119">Type: **[**MPCALLBACK\_TYPE**](mpcallback-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-120">回呼特殊資料類型。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-120">Callback special data type.</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-121">**資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-121">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-122">回呼特殊資料。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-122">Callback special data.</span></span> <span data-ttu-id="ba0e6-123">適當結構的指標取決於 **類型** 的值。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-123">The pointer to the appropriate structure depends on the value of **Type**.</span></span>

<dl> <dt>

<span data-ttu-id="ba0e6-124">**pStatusData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-124">**pStatusData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-125">類型： **PMPSTATUS \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-125">Type: **PMPSTATUS\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-126">當 **輸入**  ==  **MPCALLBACK \_ 狀態** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-126">When **Type** == **MPCALLBACK\_STATUS**.</span></span> <span data-ttu-id="ba0e6-127">請參閱 [**MPSTATUS \_ 資料**](mpstatus-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-127">See [**MPSTATUS\_DATA**](mpstatus-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-128">**pScanData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-128">**pScanData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-129">類型： **PMPSCAN \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-129">Type: **PMPSCAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-130">當 **輸入**  ==  **MPCALLBACK \_ SCAN** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-130">When **Type** == **MPCALLBACK\_SCAN**.</span></span> <span data-ttu-id="ba0e6-131">請參閱 [**MPSCAN \_ 資料**](mpscan-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-131">See [**MPSCAN\_DATA**](mpscan-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-132">**pCleanData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-132">**pCleanData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-133">類型： **PMPCLEAN \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-133">Type: **PMPCLEAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-134">當 **輸入**  ==  **MPCALLBACK \_ CLEAN** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-134">When **Type** == **MPCALLBACK\_CLEAN**.</span></span> <span data-ttu-id="ba0e6-135">請參閱 [**MPCLEAN \_ 資料**](mpclean-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-135">See [**MPCLEAN\_DATA**](mpclean-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-136">**pPrecheckData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-136">**pPrecheckData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-137">類型： **PMPCLEAN 前置檢查 \_ \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-137">Type: **PMPCLEAN\_PRECHECK\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-138">當 **輸入**  ==  **MPCALLBACK \_** 前置檢查時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-138">When **Type** == **MPCALLBACK\_PRECHECK**.</span></span> <span data-ttu-id="ba0e6-139">請參閱 MPCLEAN 前置檢查 [**\_ \_ 資料**](mpclean-precheck-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-139">See [**MPCLEAN\_PRECHECK\_DATA**](mpclean-precheck-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-140">**pThreatData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-140">**pThreatData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-141">類型： **PMPTHREAT \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-141">Type: **PMPTHREAT\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-142">當 **類型**  ==  **MPCALLBACK \_ 威脅** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-142">When **Type** == **MPCALLBACK\_THREAT**.</span></span> <span data-ttu-id="ba0e6-143">請參閱 [**MPTHREAT \_ 資料**](mpthreat-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-143">See [**MPTHREAT\_DATA**](mpthreat-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-144">**pSigUpdateData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-144">**pSigUpdateData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-145">類型： **PMPSIGUPDATE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-145">Type: **PMPSIGUPDATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-146">當 **輸入**  ==  **MPCALLBACK \_ SIGUPDATE** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-146">When **Type** == **MPCALLBACK\_SIGUPDATE**.</span></span> <span data-ttu-id="ba0e6-147">請參閱 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-147">See [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-148">**pSampleData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-148">**pSampleData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-149">類型： **PMPSAMPLE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-149">Type: **PMPSAMPLE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-150">當 **類型**  ==  **MPCALLBACK \_ 範例** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-150">When **Type** == **MPCALLBACK\_SAMPLE**.</span></span> <span data-ttu-id="ba0e6-151">請參閱 [**MPSAMPLE \_ 資料**](mpsample-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-151">See [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-152">**pReservedData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-152">**pReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-153">類型： **PMPRESERVED \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-153">Type: **PMPRESERVED\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-154">當 **類型**  ==  **MPCALLBACK \_ 保留** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-154">When **Type** == **MPCALLBACK\_RESERVED**.</span></span> <span data-ttu-id="ba0e6-155">請參閱 [**MPRESERVED \_ 資料**](mpreserved-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-155">See [**MPRESERVED\_DATA**](mpreserved-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-156">**pConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-156">**pConfigurationData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-157">類型： **PMPCONFIGURATION \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-157">Type: **PMPCONFIGURATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-158">當 **輸入**  ==  **MPCALLBACK \_ 設定 \_ 通知** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-158">When **Type** == **MPCALLBACK\_CONFIGURATION\_NOTIFICATION**.</span></span> <span data-ttu-id="ba0e6-159">請參閱 [**MPCONFIGURATION \_ 資料**](mpconfiguration-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-159">See [**MPCONFIGURATION\_DATA**](mpconfiguration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-160">**pFastPathData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-160">**pFastPathData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-161">類型： **PMPFASTPATH \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-161">Type: **PMPFASTPATH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-162">當 **輸入**  ==  **MPCALLBACK \_ FASTPATH** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-162">When **Type** == **MPCALLBACK\_FASTPATH**.</span></span> <span data-ttu-id="ba0e6-163">請參閱 [**MPFASTPATH \_ 資料**](mpfastpath-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-163">See [**MPFASTPATH\_DATA**](mpfastpath-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-164">**pExpirationData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-164">**pExpirationData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-165">類型： **PMPEXPIRATION \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-165">Type: **PMPEXPIRATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-166">當 **類型**  ==  **MPCALLBACK \_ 產品 \_ 到期** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-166">When **Type** == **MPCALLBACK\_PRODUCT\_EXPIRATION**.</span></span> <span data-ttu-id="ba0e6-167">請參閱 [**MPEXPIRATION \_ 資料**](mpexpiration-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-167">See [**MPEXPIRATION\_DATA**](mpexpiration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-168">**pNISPrivateData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-168">**pNISPrivateData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-169">類型： **PMPNIS \_ 私用 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-169">Type: **PMPNIS\_PRIVATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-170">當 **輸入**  ==  **MPCALLBACK \_ NIS \_ 私** 用時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-170">When **Type** == **MPCALLBACK\_NIS\_PRIVATE**.</span></span> <span data-ttu-id="ba0e6-171">請參閱 [**MPNIS \_ 私用 \_ 資料**](mpnis-private-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-171">See [**MPNIS\_PRIVATE\_DATA**](mpnis-private-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-172">**pHealthData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-172">**pHealthData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-173">類型： **PMPHEALTH \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-173">Type: **PMPHEALTH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-174">當 **輸入**  ==  **MPCALLBACK \_ HEALTH** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-174">When **Type** == **MPCALLBACK\_HEALTH**.</span></span> <span data-ttu-id="ba0e6-175">請參閱 [**MPHEALTH \_ 資料**](mphealth-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-175">See [**MPHEALTH\_DATA**](mphealth-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-176">**pEndOfLifeData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-176">**pEndOfLifeData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-177">類型： **PMPENDOFLIFE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-177">Type: **PMPENDOFLIFE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-178">當 **輸入**  ==  **MPCALLBACK \_ ENDOFLIFE** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-178">When **Type** == **MPCALLBACK\_ENDOFLIFE**.</span></span> <span data-ttu-id="ba0e6-179">請參閱 [**MPENDOFLIFE \_ 資料**](mpendoflife-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-179">See [**MPENDOFLIFE\_DATA**](mpendoflife-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0e6-180">**pMalwareToastData**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-180">**pMalwareToastData**</span></span>
</dt> <dd>

<span data-ttu-id="ba0e6-181">類型： **PMPMALWARETOAST \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-181">Type: **PMPMALWARETOAST\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="ba0e6-182">當 **輸入**  ==  **MPCALLBACK \_ MALWARETOAST** 時。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-182">When **Type** == **MPCALLBACK\_MALWARETOAST**.</span></span> <span data-ttu-id="ba0e6-183">請參閱 [**MPMALWARETOAST \_ 資料**](mpmalwaretoast-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ba0e6-183">See [**MPMALWARETOAST\_DATA**](mpmalwaretoast-data.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba0e6-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba0e6-184">Requirements</span></span>



| <span data-ttu-id="ba0e6-185">需求</span><span class="sxs-lookup"><span data-stu-id="ba0e6-185">Requirement</span></span> | <span data-ttu-id="ba0e6-186">值</span><span class="sxs-lookup"><span data-stu-id="ba0e6-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0e6-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba0e6-187">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0e6-188">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba0e6-188">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ba0e6-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba0e6-189">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0e6-190">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba0e6-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba0e6-191">標頭</span><span class="sxs-lookup"><span data-stu-id="ba0e6-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba0e6-192"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba0e6-192"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0e6-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba0e6-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0e6-194">**MPCALLBACK \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-194">**MPCALLBACK\_TYPE**</span></span>](mpcallback-type.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-195">**MPCLEAN \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-195">**MPCLEAN\_DATA**</span></span>](mpclean-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-196">**MPCLEAN 前置檢查 \_ \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-196">**MPCLEAN\_PRECHECK\_DATA**</span></span>](mpclean-precheck-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-197">**MPCONFIGURATION \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-197">**MPCONFIGURATION\_DATA**</span></span>](mpconfiguration-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-198">**MPENDOFLIFE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-198">**MPENDOFLIFE\_DATA**</span></span>](mpendoflife-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-199">**MPEXPIRATION \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-199">**MPEXPIRATION\_DATA**</span></span>](mpexpiration-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-200">**MPFASTPATH \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-200">**MPFASTPATH\_DATA**</span></span>](mpfastpath-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-201">**MPHEALTH \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-201">**MPHEALTH\_DATA**</span></span>](mphealth-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-202">**MPMALWARETOAST \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-202">**MPMALWARETOAST\_DATA**</span></span>](mpmalwaretoast-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-203">**MPNIS \_ 私用 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-203">**MPNIS\_PRIVATE\_DATA**</span></span>](mpnis-private-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-204">**MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-204">**MPNOTIFY**</span></span>](mpnotify.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-205">**MPRESERVED \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-205">**MPRESERVED\_DATA**</span></span>](mpreserved-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-206">**MPSAMPLE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-206">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-207">**MPSCAN \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-207">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-208">**MPSIGUPDATE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-208">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-209">**MPSTATUS \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-209">**MPSTATUS\_DATA**</span></span>](mpstatus-data.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-210">**MPTHREAT \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-210">**MPTHREAT\_DATA**</span></span>](mpthreat-data.md)
</dt> </dl>

 

 





