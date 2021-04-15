---
title: 'DRM_LICENSE_STATE_CATEGORY 列舉 (Drmexternals .h) '
description: DRM \_ 授權 \_ 狀態 \_ 類別列舉型別會定義向使用者顯示的 drm 授權字串類別。
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- DRM_LICENSE_STATE_CATEGORY 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40763ec7f610073784e3bd1516d4c955abcd65b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466125"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a><span data-ttu-id="851af-105">DRM_LICENSE_STATE_CATEGORY 列舉 (Drmexternals .h) </span><span class="sxs-lookup"><span data-stu-id="851af-105">DRM_LICENSE_STATE_CATEGORY enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="851af-106">**Drm \_ 授權 \_ 狀態 \_ 類別** 列舉型別會定義向使用者顯示的 drm [*授權*](wmformat-glossary.md)字串類別。</span><span class="sxs-lookup"><span data-stu-id="851af-106">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type defines the categories for DRM [*license*](wmformat-glossary.md) strings that are displayed to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="851af-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="851af-107">Syntax</span></span>


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
} ;
```



## <a name="constants"></a><span data-ttu-id="851af-108">常數</span><span class="sxs-lookup"><span data-stu-id="851af-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="851af-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ NORIGHT**</span><span class="sxs-lookup"><span data-stu-id="851af-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="851af-110">指出字串將採用「不允許播放」的形式。</span><span class="sxs-lookup"><span data-stu-id="851af-110">Indicates the string will take the form "Playback not permitted."</span></span>

</dd> <dt>

<span data-ttu-id="851af-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ UNLIM**</span><span class="sxs-lookup"><span data-stu-id="851af-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="851af-112">指出字串將採用「無限制播放」的形式。</span><span class="sxs-lookup"><span data-stu-id="851af-112">Indicates the string will take the form "Playback unlimited."</span></span>

</dd> <dt>

<span data-ttu-id="851af-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="851af-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="851af-114">指出字串的格式為「播放有效的5次」。</span><span class="sxs-lookup"><span data-stu-id="851af-114">Indicates the string will take the form "Playback valid 5 times."</span></span>

</dd> <dt>

<span data-ttu-id="851af-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_的 WM DRM \_ 授權 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="851af-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="851af-116">表示字串將採用「從7/12/00 播放有效的播放」格式。</span><span class="sxs-lookup"><span data-stu-id="851af-116">Indicates the string will take the form "Playback valid from 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="851af-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 到**</span><span class="sxs-lookup"><span data-stu-id="851af-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="851af-118">指出字串的格式會是「播放有效到7/12/00。」</span><span class="sxs-lookup"><span data-stu-id="851af-118">Indicates the string will take the form "Playback valid until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="851af-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ \_ 從 \_ 到到的 WM DRM 授權狀態**</span><span class="sxs-lookup"><span data-stu-id="851af-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="851af-120">表示字串將採用「從5/12 到9/12 的有效播放」形式。</span><span class="sxs-lookup"><span data-stu-id="851af-120">Indicates the string will take the form "Playback valid from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="851af-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_的 WM DRM \_ 授權 \_ 狀態 \_ 計數 \_**</span><span class="sxs-lookup"><span data-stu-id="851af-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="851af-122">指出字串的格式會是「從5/12 到9/12 的播放有效5次」。</span><span class="sxs-lookup"><span data-stu-id="851af-122">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="851af-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 計數 \_ 到**</span><span class="sxs-lookup"><span data-stu-id="851af-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="851af-124">指出字串的格式為「播放有效的5次到7/12/00。」</span><span class="sxs-lookup"><span data-stu-id="851af-124">Indicates the string will take the form "Playback valid 5 times until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="851af-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ \_ \_ 從 \_ 到到的 WM DRM 授權狀態計數**</span><span class="sxs-lookup"><span data-stu-id="851af-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="851af-126">指出字串的格式會是「從5/12 到9/12 的播放有效5次」。</span><span class="sxs-lookup"><span data-stu-id="851af-126">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="851af-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_FIRSTUSE 之後的 WM DRM \_ 授權 \_ 狀態 \_ 到期 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="851af-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="851af-128">指出字串的格式為「從第一次使用時，播放有效24小時。」</span><span class="sxs-lookup"><span data-stu-id="851af-128">Indicates the string will take the form "Playback valid for 24 hours from first use."</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="851af-129">備註</span><span class="sxs-lookup"><span data-stu-id="851af-129">Remarks</span></span>

<span data-ttu-id="851af-130">此列舉會指出要顯示之每個可能輸出字串的分類。</span><span class="sxs-lookup"><span data-stu-id="851af-130">This enumeration indicates the category for each possible output string to be displayed.</span></span> <span data-ttu-id="851af-131">它是 [**DRM \_ 授權 \_ 狀態 \_ 資料**](drm-license-state-data.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="851af-131">It is a member of the [**DRM\_LICENSE\_STATE\_DATA**](drm-license-state-data.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="851af-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="851af-132">Requirements</span></span>



| <span data-ttu-id="851af-133">需求</span><span class="sxs-lookup"><span data-stu-id="851af-133">Requirement</span></span> | <span data-ttu-id="851af-134">值</span><span class="sxs-lookup"><span data-stu-id="851af-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="851af-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="851af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="851af-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="851af-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="851af-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="851af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="851af-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="851af-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="851af-139">版本</span><span class="sxs-lookup"><span data-stu-id="851af-139">Version</span></span><br/>                  | <span data-ttu-id="851af-140">Windows Media Format 7 SDK 或更新版本的 SDK</span><span class="sxs-lookup"><span data-stu-id="851af-140">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="851af-141">標頭</span><span class="sxs-lookup"><span data-stu-id="851af-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="851af-142"><dt>Drmexternals。h</dt></span><span class="sxs-lookup"><span data-stu-id="851af-142"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="851af-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="851af-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="851af-144">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="851af-144">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





