---
title: 'WMDRMNET_POLICY 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則結構包含用於網路裝置作業之 Windows MEDIA DRM 的原則。
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986181"
---
# <a name="wmdrmnet_policy-structure"></a>WMDRMNET \_ 原則結構

**WMDRMNET \_ 原則** 結構包含用於網路裝置作業之 Windows Media DRM 的原則。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**ePolicyType**
</dt> <dd>

指定原則類型之 [**WMDRMNET \_ 原則 \_ 類型**](wmdrmnet-policy-type.md) 列舉的成員。

</dd> <dt>

**pbPolicy**
</dt> <dd>

包含原則的緩衝區。 目前唯一支援的原則類型是 **WMDRMNET \_ 原則 \_ 類型 \_ TRANSCRYPTPLAY**。 此成員是 **WMDRMNET \_ 原則 \_ TRANSCRYPTPLAY** 結構的指標。

</dd> </dl>

## <a name="remarks"></a>備註

此結構是用來做為 [**IWMDRMNetTransmitter：： GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) 方法的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> <dt>

[**WMDRMNET \_ 原則的 \_ 全域 \_ 需求**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**WMDRMNET \_ 原則的 \_ 最小 \_ 環境**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**WMDRMNET \_ 原則 \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**WMDRMNET \_ 原則 \_ 類型**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





