---
title: 'DRM_ACTION_ALLOWED_QUERY_RESULTS 列舉 (Wmdrmsdk .h) '
description: '\_ \_ \_ \_ IWMDRMLicenseQuery QUERYACTIONALLOWED 介面會使用 DRM 動作允許的查詢結果列舉類型來指定不允許動作的原因。'
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- DRM_ACTION_ALLOWED_QUERY_RESULTS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_ACTION_ALLOWED_QUERY_RESULTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e328acb915bd32547f3455e8556e4caba2360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999491"
---
# <a name="drm_action_allowed_query_results-enumeration"></a><span data-ttu-id="19511-105">DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 結果列舉</span><span class="sxs-lookup"><span data-stu-id="19511-105">DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS enumeration</span></span>

<span data-ttu-id="19511-106">[**IWMDRMLicenseQuery：： QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)介面會使用 **DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 結果** 列舉類型來指定不允許動作的原因。</span><span class="sxs-lookup"><span data-stu-id="19511-106">The **DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS** enumeration type is used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="19511-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="19511-107">Syntax</span></span>


```C++
typedef enum DRM_ACTION_ALLOWED_QUERY_RESULTS { 
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED                       = 0x00000001,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE            = 0x00000002,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT              = 0x00000004,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED             = 0x00000008,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED               = 0x00000010,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED           = 0x00000020,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW        = 0x00000040,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV             = 0x00000080,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW      = 0x00000100,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED     = 0x00000200,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT      = 0x00000400,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT   = 0x00000800,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH  = 0x00001000
} ;
```



## <a name="constants"></a><span data-ttu-id="19511-108">常數</span><span class="sxs-lookup"><span data-stu-id="19511-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="19511-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_ \_ \_ \_ 未 \_ 啟用 DRM 動作允許的查詢**</span><span class="sxs-lookup"><span data-stu-id="19511-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED**</span></span>
</dt> <dd>

<span data-ttu-id="19511-110">指定不允許查詢動作。</span><span class="sxs-lookup"><span data-stu-id="19511-110">Specifies that the queries action is not allowed.</span></span> <span data-ttu-id="19511-111">針對不允許的動作，傳回的值會使用位 OR 結合此列舉中的一或多個其他值，以結合此值。</span><span class="sxs-lookup"><span data-stu-id="19511-111">For actions that are not allowed, the returned value is this value combined by using a bitwise OR with one or more of the other values in this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="19511-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**\_ \_ 未啟用 DRM 動作允許的 \_ 查詢 \_ \_ \_ 沒有 \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="19511-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="19511-113">指定要求的內容不存在授權。</span><span class="sxs-lookup"><span data-stu-id="19511-113">Specifies that a license does not exist for the requested content.</span></span>

</dd> <dt>

<span data-ttu-id="19511-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**\_ \_ 未啟用 DRM 動作允許的 \_ 查詢 \_ \_ \_ 沒有 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="19511-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="19511-115">指定內容有授權，但不允許查詢的許可權。</span><span class="sxs-lookup"><span data-stu-id="19511-115">Specifies that a license exists for the content, but that the queried right is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="19511-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_ \_ 未啟用 DRM 動作允許的 \_ 查詢 \_ \_ 已 \_ 用盡**</span><span class="sxs-lookup"><span data-stu-id="19511-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXHAUSTED**</span></span>
</dt> <dd>

<span data-ttu-id="19511-117">指定查詢的許可權會受到計數限制，且不會再有其他用途。</span><span class="sxs-lookup"><span data-stu-id="19511-117">Specifies that the queried right is restricted by a count, and that no more uses remain.</span></span>

</dd> <dt>

<span data-ttu-id="19511-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未啟用- \_ 已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="19511-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="19511-119">指定使用早于目前日期的到期日來限制所查詢的許可權。</span><span class="sxs-lookup"><span data-stu-id="19511-119">Specifies that the queried right is restricted with an expiration date that is earlier than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="19511-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**未 \_ 啟用 DRM 動作 \_ 允許的 \_ 查詢未 \_ \_ \_ \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="19511-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NOT\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="19511-121">指定所查詢的許可權限制為晚于目前日期的開始日期。</span><span class="sxs-lookup"><span data-stu-id="19511-121">Specifies that the queried right is restricted with a start date that is later than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="19511-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未 \_ 啟用 \_ APPSEC \_ 太 \_ 低**</span><span class="sxs-lookup"><span data-stu-id="19511-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_APPSEC\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="19511-123">指定內容有授權，而且授權允許查詢許可權，但呼叫應用程式的安全性層級不夠高。</span><span class="sxs-lookup"><span data-stu-id="19511-123">Specifies that a license exists for the content and that the license allows the queried right, but that the security level of the calling application is not high enough.</span></span>

</dd> <dt>

<span data-ttu-id="19511-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未 \_ 啟用 \_ 需求 \_ INDIV**</span><span class="sxs-lookup"><span data-stu-id="19511-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_REQ\_INDIV**</span></span>
</dt> <dd>

<span data-ttu-id="19511-125">指定內容有授權，而且授權允許查詢許可權，但 DRM 子系統必須是個人化的。</span><span class="sxs-lookup"><span data-stu-id="19511-125">Specifies that a license exists for the content and that the license allows the queried right, but that the DRM subsystem must be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="19511-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未啟用的 \_ \_ 複製 \_ OPL \_ 太 \_ 低**</span><span class="sxs-lookup"><span data-stu-id="19511-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="19511-127">指定用戶端的輸出保護層級太低。</span><span class="sxs-lookup"><span data-stu-id="19511-127">Specifies that the output protection level of the client is too low.</span></span>

</dd> <dt>

<span data-ttu-id="19511-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM \_ 動作 \_ 允許 \_ 的 \_ 查詢 \_ 未 \_ 啟用 \_ OPL \_ 排除的複製**</span><span class="sxs-lookup"><span data-stu-id="19511-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_EXCLUDED**</span></span>
</dt> <dd>

<span data-ttu-id="19511-129">指定用戶端的輸出保護層級是在排除清單上。</span><span class="sxs-lookup"><span data-stu-id="19511-129">Specifies that the output protection level of the client is on the exclusion list.</span></span>

</dd> <dt>

<span data-ttu-id="19511-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未啟用的 \_ \_ \_ 時鐘 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="19511-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_CLOCK\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="19511-131">指定授權需要安全的時鐘支援，而且用戶端不提供。</span><span class="sxs-lookup"><span data-stu-id="19511-131">Specifies that the license requires secure clock support and that the client does not provide it.</span></span>

</dd> <dt>

<span data-ttu-id="19511-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM \_ 動作 \_ 允許 \_ 的 \_ 查詢 \_ 未 \_ 啟用 \_ 計量 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="19511-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_METERING\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="19511-133">指定授權允許查詢的動作，但需要該計量，而且用戶端不支援計量。</span><span class="sxs-lookup"><span data-stu-id="19511-133">Specifies that the queried action is allowed by a license, but that metering is required and the client does not support metering.</span></span>

</dd> <dt>

<span data-ttu-id="19511-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未 \_ 啟用 \_ 鏈 \_ 深度 \_ 過 \_ 高**</span><span class="sxs-lookup"><span data-stu-id="19511-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_CHAIN\_DEPTH\_TOO\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="19511-135">指定無法判斷所查詢之動作的許可權，因為內容是由連鎖授權所涵蓋，但缺少分葉授權。</span><span class="sxs-lookup"><span data-stu-id="19511-135">Specifies that the rights for the queried action cannot be determined because the content is covered by a chained license and the leaf license is missing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19511-136">備註</span><span class="sxs-lookup"><span data-stu-id="19511-136">Remarks</span></span>

<span data-ttu-id="19511-137">此列舉類型的值表示不允許動作。</span><span class="sxs-lookup"><span data-stu-id="19511-137">The values of this enumeration type indicate that an action is not allowed.</span></span> <span data-ttu-id="19511-138">值為零表示允許動作。</span><span class="sxs-lookup"><span data-stu-id="19511-138">A value of zero indicates that the action is allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="19511-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="19511-139">Requirements</span></span>



| <span data-ttu-id="19511-140">需求</span><span class="sxs-lookup"><span data-stu-id="19511-140">Requirement</span></span> | <span data-ttu-id="19511-141">值</span><span class="sxs-lookup"><span data-stu-id="19511-141">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19511-142">標頭</span><span class="sxs-lookup"><span data-stu-id="19511-142">Header</span></span><br/> | <dl> <span data-ttu-id="19511-143"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="19511-143"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19511-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19511-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19511-145">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="19511-145">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





