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
# <a name="drm_action_allowed_query_results-enumeration"></a>DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 結果列舉

[**IWMDRMLicenseQuery：： QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)介面會使用 **DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 結果** 列舉類型來指定不允許動作的原因。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_ \_ \_ \_ 未 \_ 啟用 DRM 動作允許的查詢**
</dt> <dd>

指定不允許查詢動作。 針對不允許的動作，傳回的值會使用位 OR 結合此列舉中的一或多個其他值，以結合此值。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**\_ \_ 未啟用 DRM 動作允許的 \_ 查詢 \_ \_ \_ 沒有 \_ 授權**
</dt> <dd>

指定要求的內容不存在授權。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**\_ \_ 未啟用 DRM 動作允許的 \_ 查詢 \_ \_ \_ 沒有 \_ 許可權**
</dt> <dd>

指定內容有授權，但不允許查詢的許可權。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_ \_ 未啟用 DRM 動作允許的 \_ 查詢 \_ \_ 已 \_ 用盡**
</dt> <dd>

指定查詢的許可權會受到計數限制，且不會再有其他用途。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未啟用- \_ 已 \_ 過期**
</dt> <dd>

指定使用早于目前日期的到期日來限制所查詢的許可權。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**未 \_ 啟用 DRM 動作 \_ 允許的 \_ 查詢未 \_ \_ \_ \_ 啟動**
</dt> <dd>

指定所查詢的許可權限制為晚于目前日期的開始日期。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未 \_ 啟用 \_ APPSEC \_ 太 \_ 低**
</dt> <dd>

指定內容有授權，而且授權允許查詢許可權，但呼叫應用程式的安全性層級不夠高。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未 \_ 啟用 \_ 需求 \_ INDIV**
</dt> <dd>

指定內容有授權，而且授權允許查詢許可權，但 DRM 子系統必須是個人化的。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未啟用的 \_ \_ 複製 \_ OPL \_ 太 \_ 低**
</dt> <dd>

指定用戶端的輸出保護層級太低。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM \_ 動作 \_ 允許 \_ 的 \_ 查詢 \_ 未 \_ 啟用 \_ OPL \_ 排除的複製**
</dt> <dd>

指定用戶端的輸出保護層級是在排除清單上。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未啟用的 \_ \_ \_ 時鐘 \_ 支援**
</dt> <dd>

指定授權需要安全的時鐘支援，而且用戶端不提供。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM \_ 動作 \_ 允許 \_ 的 \_ 查詢 \_ 未 \_ 啟用 \_ 計量 \_ 支援**
</dt> <dd>

指定授權允許查詢的動作，但需要該計量，而且用戶端不支援計量。

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 未 \_ 啟用 \_ 鏈 \_ 深度 \_ 過 \_ 高**
</dt> <dd>

指定無法判斷所查詢之動作的許可權，因為內容是由連鎖授權所涵蓋，但缺少分葉授權。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉類型的值表示不允許動作。 值為零表示允許動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](drm-enumeration-types.md)
</dt> </dl>

 

 





