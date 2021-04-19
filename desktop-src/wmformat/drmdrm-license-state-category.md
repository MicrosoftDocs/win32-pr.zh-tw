---
title: 'DRM_LICENSE_STATE_CATEGORY 列舉 (Wmdrmsdk .h) '
description: DRM \_ 授權 \_ 狀態 \_ 類別列舉型別會指定由 drm \_ 授權 \_ 狀態資料結構所描述的授許可權制類型 \_ 。
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- DRM_LICENSE_STATE_CATEGORY 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e928a95a71d9636f88bc3c79ac36168072527040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978434"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a><span data-ttu-id="e206e-104">DRM_LICENSE_STATE_CATEGORY 列舉 (Wmdrmsdk .h) </span><span class="sxs-lookup"><span data-stu-id="e206e-104">DRM_LICENSE_STATE_CATEGORY enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="e206e-105">**Drm \_ 授權 \_ 狀態 \_ 類別** 列舉型別會指定由 [**drm \_ 授權 \_ 狀態 \_ 資料**](drmdrm-license-state-data.md)結構所描述的授許可權制類型。</span><span class="sxs-lookup"><span data-stu-id="e206e-105">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e206e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e206e-106">Syntax</span></span>


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a><span data-ttu-id="e206e-107">常數</span><span class="sxs-lookup"><span data-stu-id="e206e-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e206e-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ NORIGHT**</span><span class="sxs-lookup"><span data-stu-id="e206e-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-109">指定不允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。</span><span class="sxs-lookup"><span data-stu-id="e206e-109">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ UNLIM**</span><span class="sxs-lookup"><span data-stu-id="e206e-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-111">指定允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，而不受限制。</span><span class="sxs-lookup"><span data-stu-id="e206e-111">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="e206e-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-113">指定允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，但只允許設定的次數。</span><span class="sxs-lookup"><span data-stu-id="e206e-113">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_的 WM DRM \_ 授權 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="e206e-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-115">指定在設定日期之後，允許接收其 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。</span><span class="sxs-lookup"><span data-stu-id="e206e-115">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 到**</span><span class="sxs-lookup"><span data-stu-id="e206e-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-117">指定在設定的日期之前，允許接收其 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。</span><span class="sxs-lookup"><span data-stu-id="e206e-117">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ \_ 從 \_ 到到的 WM DRM 授權狀態**</span><span class="sxs-lookup"><span data-stu-id="e206e-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-119">指定在兩個設定的日期之間允許收到已接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。</span><span class="sxs-lookup"><span data-stu-id="e206e-119">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_的 WM DRM \_ 授權 \_ 狀態 \_ 計數 \_**</span><span class="sxs-lookup"><span data-stu-id="e206e-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-121">指定允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，但在設定日期之後只能有設定的次數。</span><span class="sxs-lookup"><span data-stu-id="e206e-121">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 計數 \_ 到**</span><span class="sxs-lookup"><span data-stu-id="e206e-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-123">指定允許已接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，但在設定的日期之前只有設定的次數。</span><span class="sxs-lookup"><span data-stu-id="e206e-123">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ \_ \_ 從 \_ 到到的 WM DRM 授權狀態計數**</span><span class="sxs-lookup"><span data-stu-id="e206e-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-125">指定允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，但在兩個設定的日期之間只能有設定的次數。</span><span class="sxs-lookup"><span data-stu-id="e206e-125">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="e206e-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_FIRSTUSE 之後的 WM DRM \_ 授權 \_ 狀態 \_ 到期 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e206e-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="e206e-127">指定從第一次使用動作開始，可允許已接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。</span><span class="sxs-lookup"><span data-stu-id="e206e-127">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed for a set amount of time beginning with the first use of the action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e206e-128">備註</span><span class="sxs-lookup"><span data-stu-id="e206e-128">Remarks</span></span>

<span data-ttu-id="e206e-129">無。</span><span class="sxs-lookup"><span data-stu-id="e206e-129">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e206e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e206e-130">Requirements</span></span>



| <span data-ttu-id="e206e-131">需求</span><span class="sxs-lookup"><span data-stu-id="e206e-131">Requirement</span></span> | <span data-ttu-id="e206e-132">值</span><span class="sxs-lookup"><span data-stu-id="e206e-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e206e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="e206e-133">Header</span></span><br/> | <dl> <span data-ttu-id="e206e-134"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="e206e-134"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e206e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e206e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e206e-136">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="e206e-136">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





