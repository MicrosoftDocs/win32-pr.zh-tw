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
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>DRM_LICENSE_STATE_CATEGORY 列舉 (Wmdrmsdk .h) 

**Drm \_ 授權 \_ 狀態 \_ 類別** 列舉型別會指定由 [**drm \_ 授權 \_ 狀態 \_ 資料**](drmdrm-license-state-data.md)結構所描述的授許可權制類型。

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
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ NORIGHT**
</dt> <dd>

指定不允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ UNLIM**
</dt> <dd>

指定允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，而不受限制。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 計數**
</dt> <dd>

指定允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，但只允許設定的次數。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_的 WM DRM \_ 授權 \_ 狀態 \_**
</dt> <dd>

指定在設定日期之後，允許接收其 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 到**
</dt> <dd>

指定在設定的日期之前，允許接收其 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ \_ 從 \_ 到到的 WM DRM 授權狀態**
</dt> <dd>

指定在兩個設定的日期之間允許收到已接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_的 WM DRM \_ 授權 \_ 狀態 \_ 計數 \_**
</dt> <dd>

指定允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，但在設定日期之後只能有設定的次數。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM \_ DRM \_ 授權 \_ 狀態 \_ 計數 \_ 到**
</dt> <dd>

指定允許已接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，但在設定的日期之前只有設定的次數。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ \_ \_ 從 \_ 到到的 WM DRM 授權狀態計數**
</dt> <dd>

指定允許接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作，但在兩個設定的日期之間只能有設定的次數。

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_FIRSTUSE 之後的 WM DRM \_ 授權 \_ 狀態 \_ 到期 \_ \_**
</dt> <dd>

指定從第一次使用動作開始，可允許已接收 **DRM \_ 授權 \_ 狀態 \_ 資料** 的動作。

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

 

 





