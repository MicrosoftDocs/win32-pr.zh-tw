---
title: 'MSDRM_STATUS 列舉 (Wmdrmsdk .h) '
description: MSDRM \_ 狀態列舉類型會定義 DRM 子系統的狀態條件。
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- MSDRM_STATUS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000761"
---
# <a name="msdrm_status-enumeration"></a><span data-ttu-id="914fd-105">MSDRM \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="914fd-105">MSDRM\_STATUS enumeration</span></span>

<span data-ttu-id="914fd-106">**MSDRM \_ 狀態** 列舉類型會定義 DRM 子系統的狀態條件。</span><span class="sxs-lookup"><span data-stu-id="914fd-106">The **MSDRM\_STATUS** enumeration type defines status conditions for the DRM subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="914fd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="914fd-107">Syntax</span></span>


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a><span data-ttu-id="914fd-108">常數</span><span class="sxs-lookup"><span data-stu-id="914fd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="914fd-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="914fd-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-110">指定發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="914fd-110">Specifies that an error has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="914fd-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM\_INFORMATION**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-112">指定有其他狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="914fd-112">Specifies that there is additional status information.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM \_ BACKUPRESTORE \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="914fd-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM\_BACKUPRESTORE\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-114">指定已開始授權備份或還原作業。</span><span class="sxs-lookup"><span data-stu-id="914fd-114">Specifies that a license backup or restore operation has begun.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM \_ BACKUPRESTORE \_ END**</span><span class="sxs-lookup"><span data-stu-id="914fd-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM\_BACKUPRESTORE\_END**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-116">指定授權備份或還原作業已結束。</span><span class="sxs-lookup"><span data-stu-id="914fd-116">Specifies that a license backup or restore operation has ended.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM \_ BACKUPRESTORE \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="914fd-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM\_BACKUPRESTORE\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-118">指定授權備份或還原作業正在進行中，且用戶端電腦已與備份伺服器連接。</span><span class="sxs-lookup"><span data-stu-id="914fd-118">Specifies that a license backup or restore operation is in progress and that the client computer is connecting with the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM \_ BACKUPRESTORE \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="914fd-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM\_BACKUPRESTORE\_DISCONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-120">指定授權備份或還原作業正在進行中，且用戶端電腦正在與備份伺服器中斷連線。</span><span class="sxs-lookup"><span data-stu-id="914fd-120">Specifies that a license backup or restore operation is in progress and that the client computer is disconnecting from the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM \_ 錯誤 \_ WITHURL**</span><span class="sxs-lookup"><span data-stu-id="914fd-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM\_ERROR\_WITHURL**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-122">指定 DRM 作業遇到不正確的 URL。</span><span class="sxs-lookup"><span data-stu-id="914fd-122">Specifies that the DRM operation has encountered a bad URL.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_受 DRM 限制的 \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="914fd-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**DRM\_RESTRICTED\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-124">指定 DRM 作業無法繼續，因為用戶端電腦上沒有授與所需許可權的授權。</span><span class="sxs-lookup"><span data-stu-id="914fd-124">Specifies that the DRM operation cannot continue because no license granting the required right exists on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ 需要具有 \_ 個人化**</span><span class="sxs-lookup"><span data-stu-id="914fd-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM\_NEEDS\_INDIVIDUALIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-126">指定 DRM 作業無法繼續，因為 DRM 子系統需要個人化。</span><span class="sxs-lookup"><span data-stu-id="914fd-126">Specifies that the DRM operation cannot continue because the DRM subsystem needs to be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM \_ PLAY \_ OPL \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="914fd-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM\_PLAY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-128">指定因為未符合輸出保護層級需求，所以無法完成播放操作。</span><span class="sxs-lookup"><span data-stu-id="914fd-128">Specifies that a playback operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM \_ 複製 \_ OPL \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="914fd-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM\_COPY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-130">指定因為未符合輸出保護層級需求，所以無法完成複製作業。</span><span class="sxs-lookup"><span data-stu-id="914fd-130">Specifies that a copy operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="914fd-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM \_ REFRESHCRL \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="914fd-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM\_REFRESHCRL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="914fd-132">指定對 [**IWMDRMSecurity：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) 的呼叫已完成撤銷清單的重新整理。</span><span class="sxs-lookup"><span data-stu-id="914fd-132">Specifies that a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) has completed refreshing a revocation list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="914fd-133">備註</span><span class="sxs-lookup"><span data-stu-id="914fd-133">Remarks</span></span>

<span data-ttu-id="914fd-134">無。</span><span class="sxs-lookup"><span data-stu-id="914fd-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="914fd-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="914fd-135">Requirements</span></span>



| <span data-ttu-id="914fd-136">需求</span><span class="sxs-lookup"><span data-stu-id="914fd-136">Requirement</span></span> | <span data-ttu-id="914fd-137">值</span><span class="sxs-lookup"><span data-stu-id="914fd-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="914fd-138">標頭</span><span class="sxs-lookup"><span data-stu-id="914fd-138">Header</span></span><br/> | <dl> <span data-ttu-id="914fd-139"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="914fd-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="914fd-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="914fd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="914fd-141">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="914fd-141">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





