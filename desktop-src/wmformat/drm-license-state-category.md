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
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>DRM_LICENSE_STATE_CATEGORY 列舉 (Drmexternals .h) 

**Drm \_ 授權 \_ 狀態 \_ 類別** 列舉型別會定義向使用者顯示的 drm [*授權*](wmformat-glossary.md)字串類別。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ NORIGHT**
</dt> <dd>

指出字串將採用「不允許播放」的形式。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ UNLIM**
</dt> <dd>

指出字串將採用「無限制播放」的形式。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 計數**
</dt> <dd>

指出字串的格式為「播放有效的5次」。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_的 WM DRM \_ 授權 \_ 狀態 \_**
</dt> <dd>

表示字串將採用「從7/12/00 播放有效的播放」格式。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 到**
</dt> <dd>

指出字串的格式會是「播放有效到7/12/00。」

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ \_ 從 \_ 到到的 WM DRM 授權狀態**
</dt> <dd>

表示字串將採用「從5/12 到9/12 的有效播放」形式。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_的 WM DRM \_ 授權 \_ 狀態 \_ 計數 \_**
</dt> <dd>

指出字串的格式會是「從5/12 到9/12 的播放有效5次」。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 計數 \_ 到**
</dt> <dd>

指出字串的格式為「播放有效的5次到7/12/00。」

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ \_ \_ 從 \_ 到到的 WM DRM 授權狀態計數**
</dt> <dd>

指出字串的格式會是「從5/12 到9/12 的播放有效5次」。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_FIRSTUSE 之後的 WM DRM \_ 授權 \_ 狀態 \_ 到期 \_ \_**
</dt> <dd>

指出字串的格式為「從第一次使用時，播放有效24小時。」

</dd> </dl>

## <a name="remarks"></a>備註

此列舉會指出要顯示之每個可能輸出字串的分類。 它是 [**DRM \_ 授權 \_ 狀態 \_ 資料**](drm-license-state-data.md) 結構的成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                      |
| 版本<br/>                  | Windows Media Format 7 SDK 或更新版本的 SDK<br/>                       |
| 標頭<br/>                   | <dl> <dt>Drmexternals。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](enumeration-types.md)
</dt> </dl>

 

 





