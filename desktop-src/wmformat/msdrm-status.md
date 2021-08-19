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
ms.openlocfilehash: 0c4c1f9b37f237b1ae2399849ef3100e3d6fdbc12c7ee3bc1d169420e38bb85a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654572"
---
# <a name="msdrm_status-enumeration"></a>MSDRM \_ 狀態列舉

**MSDRM \_ 狀態** 列舉類型會定義 DRM 子系統的狀態條件。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM \_ 錯誤**
</dt> <dd>

指定發生錯誤。

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM \_ 資訊**
</dt> <dd>

指定有其他狀態資訊。

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM \_ BACKUPRESTORE \_ 開始**
</dt> <dd>

指定已開始授權備份或還原作業。

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM \_ BACKUPRESTORE \_ END**
</dt> <dd>

指定授權備份或還原作業已結束。

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM \_ BACKUPRESTORE \_ 連接**
</dt> <dd>

指定授權備份或還原作業正在進行中，且用戶端電腦已與備份伺服器連接。

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM \_ BACKUPRESTORE \_ 中斷連線**
</dt> <dd>

指定授權備份或還原作業正在進行中，且用戶端電腦正在與備份伺服器中斷連線。

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM \_ 錯誤 \_ WITHURL**
</dt> <dd>

指定 DRM 作業遇到不正確的 URL。

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_受 DRM 限制的 \_ 授權**
</dt> <dd>

指定 DRM 作業無法繼續，因為用戶端電腦上沒有授與所需許可權的授權。

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ 需要具有 \_ 個人化**
</dt> <dd>

指定 DRM 作業無法繼續，因為 DRM 子系統需要個人化。

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM \_ PLAY \_ OPL \_ 通知**
</dt> <dd>

指定因為未符合輸出保護層級需求，所以無法完成播放操作。

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM \_ 複製 \_ OPL \_ 通知**
</dt> <dd>

指定因為未符合輸出保護層級需求，所以無法完成複製作業。

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM \_ REFRESHCRL \_ 完成**
</dt> <dd>

指定對 [**IWMDRMSecurity：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) 的呼叫已完成撤銷清單的重新整理。

</dd> </dl>

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](drm-enumeration-types.md)
</dt> </dl>

 

 





