---
description: 限制要設定或傳回之資料的旗標。
title: 'SRRF (Shlwapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026904"
---
# <a name="srrf"></a><span data-ttu-id="69d87-103">SRRF</span><span class="sxs-lookup"><span data-stu-id="69d87-103">SRRF</span></span>

<span data-ttu-id="69d87-104">限制要設定或傳回之資料的旗標。</span><span class="sxs-lookup"><span data-stu-id="69d87-104">Flags that restrict the data to be set or returned.</span></span>



| <span data-ttu-id="69d87-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="69d87-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="69d87-106">Description</span><span class="sxs-lookup"><span data-stu-id="69d87-106">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <span data-ttu-id="69d87-107"><dt>**SRRF \_RT \_ REG \_ NONE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-107"><dt>**SRRF\_RT\_REG\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="69d87-108">輸入 REG \_ NONE。</span><span class="sxs-lookup"><span data-stu-id="69d87-108">Type REG\_NONE.</span></span><br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <span data-ttu-id="69d87-109"><dt>**SRRF \_RT \_ REG \_ SZ**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-109"><dt>**SRRF\_RT\_REG\_SZ**</dt> <dt>0x00000002</dt></span></span> </dl>                       | <span data-ttu-id="69d87-110">輸入 REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="69d87-110">Type REG\_SZ.</span></span> <span data-ttu-id="69d87-111">\_ \_ \_ 除非指定了 SRRF NOEXPAND 旗標，否則 REG EXPAND sz 類型會自動轉換為 REG SZ \_ 。</span><span class="sxs-lookup"><span data-stu-id="69d87-111">REG\_EXPAND\_SZ types are automatically converted to REG\_SZ unless the SRRF\_NOEXPAND flag is specified.</span></span><br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <span data-ttu-id="69d87-112"><dt>**SRRF \_RT \_ REG \_ EXPAND \_ SZ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-112"><dt>**SRRF\_RT\_REG\_EXPAND\_SZ**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="69d87-113">輸入 REG \_ EXPAND \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="69d87-113">Type REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="69d87-114">如果要取得值，您也必須取得 SRRF \_ NOEXPAND 旗標，否則 [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) 會失敗，並出現錯誤 \_ \_ 參數無效。</span><span class="sxs-lookup"><span data-stu-id="69d87-114">If retrieving a value, you must also get the SRRF\_NOEXPAND flag, or [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) fails with ERROR\_INVALID\_PARAMETER.</span></span><br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <span data-ttu-id="69d87-115"><dt>**SRRF \_RT \_ REG \_ BINARY**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-115"><dt>**SRRF\_RT\_REG\_BINARY**</dt> <dt>0x00000008</dt></span></span> </dl>           | <span data-ttu-id="69d87-116">輸入 REG \_ BINARY。</span><span class="sxs-lookup"><span data-stu-id="69d87-116">Type REG\_BINARY.</span></span><br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <span data-ttu-id="69d87-117"><dt>**SRRF \_RT \_ REG \_ DWORD**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-117"><dt>**SRRF\_RT\_REG\_DWORD**</dt> <dt>0x00000010</dt></span></span> </dl>              | <span data-ttu-id="69d87-118">輸入 REG \_ DWORD。</span><span class="sxs-lookup"><span data-stu-id="69d87-118">Type REG\_DWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <span data-ttu-id="69d87-119"><dt>**SRRF \_RT \_ REG \_ 多重 \_ SZ**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-119"><dt>**SRRF\_RT\_REG\_MULTI\_SZ**</dt> <dt>0x00000020</dt></span></span> </dl>    | <span data-ttu-id="69d87-120">輸入 REG \_ 多重 \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="69d87-120">Type REG\_MULTI\_SZ.</span></span><br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <span data-ttu-id="69d87-121"><dt>**SRRF \_RT \_ REG \_ QWORD**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-121"><dt>**SRRF\_RT\_REG\_QWORD**</dt> <dt>0x00000040</dt></span></span> </dl>              | <span data-ttu-id="69d87-122">輸入 REG \_ QWORD。</span><span class="sxs-lookup"><span data-stu-id="69d87-122">Type REG\_QWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <span data-ttu-id="69d87-123"><dt>**SRRF \_RT \_ DWORD**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-123"><dt>**SRRF\_RT\_DWORD**</dt> <dt>0x00000018</dt></span></span> </dl>                           | <span data-ttu-id="69d87-124">REG \_ DWORD 和32位 reg \_ 二進位類型。</span><span class="sxs-lookup"><span data-stu-id="69d87-124">REG\_DWORD and 32-bit REG\_BINARY types.</span></span> <span data-ttu-id="69d87-125">這相當於 SRRF \_ rt \_ reg \_ BINARY \| SRRF \_ rt \_ reg \_ DWORD。</span><span class="sxs-lookup"><span data-stu-id="69d87-125">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_DWORD.</span></span> <span data-ttu-id="69d87-126">如果要抓取值，如果值的二進位資料大於32位，則不會傳回。</span><span class="sxs-lookup"><span data-stu-id="69d87-126">If retrieving a value, if the value's binary data is larger than 32 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <span data-ttu-id="69d87-127"><dt>**SRRF \_RT \_ QWORD**</dt> <dt>0x00000048</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-127"><dt>**SRRF\_RT\_QWORD**</dt> <dt>0x00000048</dt></span></span> </dl>                           | <span data-ttu-id="69d87-128">REG \_ QWORD 和64位 reg \_ 二進位類型。</span><span class="sxs-lookup"><span data-stu-id="69d87-128">REG\_QWORD and 64-bit REG\_BINARY types.</span></span> <span data-ttu-id="69d87-129">這相當於 SRRF \_ rt \_ reg \_ BINARY \| SRRF \_ rt \_ reg \_ 。</span><span class="sxs-lookup"><span data-stu-id="69d87-129">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_QWORD.</span></span> <span data-ttu-id="69d87-130">如果要抓取值，如果值的二進位資料大於64位，則不會傳回。</span><span class="sxs-lookup"><span data-stu-id="69d87-130">If retrieving a value, if the value's binary data is larger than 64 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <span data-ttu-id="69d87-131"><dt>**SRRF \_RT \_ 任何**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-131"><dt>**SRRF\_RT\_ANY**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                                 | <span data-ttu-id="69d87-132">所有類型。</span><span class="sxs-lookup"><span data-stu-id="69d87-132">All types.</span></span> <span data-ttu-id="69d87-133">如果未設定其他 SRRF RT 值，請設定此旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="69d87-133">Set this flag if no other SRRF\_RT value is set.</span></span><br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <span data-ttu-id="69d87-134"><dt>**SRRF \_RM \_ 任何**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-134"><dt>**SRRF\_RM\_ANY**</dt> <dt>0x00000000</dt></span></span> </dl>                                 | <span data-ttu-id="69d87-135">無模式限制。</span><span class="sxs-lookup"><span data-stu-id="69d87-135">No mode restriction.</span></span> <span data-ttu-id="69d87-136">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="69d87-136">This is the default value.</span></span><br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <span data-ttu-id="69d87-137"><dt>**SRRF \_RM \_ 一般**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-137"><dt>**SRRF\_RM\_NORMAL**</dt> <dt>0x00010000</dt></span></span> </dl>                        | <span data-ttu-id="69d87-138">將系統啟動模式限制為「正常開機」。</span><span class="sxs-lookup"><span data-stu-id="69d87-138">Restrict system startup mode to "normal boot".</span></span><br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <span data-ttu-id="69d87-139"><dt>**SRRF \_RM \_ SAFE**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-139"><dt>**SRRF\_RM\_SAFE**</dt> <dt>0x00020000</dt></span></span> </dl>                              | <span data-ttu-id="69d87-140">將系統啟動模式限制為「安全模式」。</span><span class="sxs-lookup"><span data-stu-id="69d87-140">Restrict system startup mode to "safe mode".</span></span><br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <span data-ttu-id="69d87-141"><dt>**SRRF \_RM \_ SAFENETWORK**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-141"><dt>**SRRF\_RM\_SAFENETWORK**</dt> <dt>0x00040000</dt></span></span> </dl>         | <span data-ttu-id="69d87-142">將系統啟動模式限制為「具有網路功能的安全模式」。</span><span class="sxs-lookup"><span data-stu-id="69d87-142">Restrict system startup mode to "safe mode with networking".</span></span><br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <span data-ttu-id="69d87-143"><dt>**SRRF \_NOEXPAND**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-143"><dt>**SRRF\_NOEXPAND**</dt> <dt>0x10000000</dt></span></span> </dl>                            | <span data-ttu-id="69d87-144">不要自動展開 REG \_ expand \_ SZ 環境字串。</span><span class="sxs-lookup"><span data-stu-id="69d87-144">Do not automatically expand REG\_EXPAND\_SZ environment strings.</span></span><br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <span data-ttu-id="69d87-145"><dt>**SRRF \_ZEROONFAILURE**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-145"><dt>**SRRF\_ZEROONFAILURE**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="69d87-146">如果要取出值，如果 *pvData* 不是 **Null**，請將 *pvData* 緩衝區的內容設定為失敗時的所有零。</span><span class="sxs-lookup"><span data-stu-id="69d87-146">If retrieving a value, if *pvData* is not **NULL**, set the contents of the *pvData* buffer to all zeros on failure.</span></span><br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <span data-ttu-id="69d87-147"><dt>**SRRF \_NOVIRT**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-147"><dt>**SRRF\_NOVIRT**</dt> <dt>0x40000000</dt></span></span> </dl>                                  | <span data-ttu-id="69d87-148">在抓取值時，如果要求的金鑰已虛擬化，將會失敗並 \_ \_ 找不到錯誤檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="69d87-148">When retrieving a value, if the requested key is virtualized, fail with ERROR\_FILE\_NOT\_FOUND.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="69d87-149">備註</span><span class="sxs-lookup"><span data-stu-id="69d87-149">Remarks</span></span>

<span data-ttu-id="69d87-150">這些值定義于 Shlwapi 中。</span><span class="sxs-lookup"><span data-stu-id="69d87-150">These values are defined in Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d87-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="69d87-151">Requirements</span></span>



| <span data-ttu-id="69d87-152">需求</span><span class="sxs-lookup"><span data-stu-id="69d87-152">Requirement</span></span> | <span data-ttu-id="69d87-153">值</span><span class="sxs-lookup"><span data-stu-id="69d87-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="69d87-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69d87-154">Minimum supported client</span></span><br/> | <span data-ttu-id="69d87-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69d87-155">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="69d87-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69d87-156">Minimum supported server</span></span><br/> | <span data-ttu-id="69d87-157">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69d87-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="69d87-158">標頭</span><span class="sxs-lookup"><span data-stu-id="69d87-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d87-159"><dt>Shlwapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="69d87-159"><dt>Shlwapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d87-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69d87-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d87-161">**SHRegSetValue**</span><span class="sxs-lookup"><span data-stu-id="69d87-161">**SHRegSetValue**</span></span>](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[<span data-ttu-id="69d87-162">**SHRegGetValue**</span><span class="sxs-lookup"><span data-stu-id="69d87-162">**SHRegGetValue**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




