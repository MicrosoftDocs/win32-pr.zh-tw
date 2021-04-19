---
title: 'WMDRMNET_POLICY_TYPE 列舉 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則 \_ 類型列舉類型會列出可用於網路裝置作業之 WINDOWS Media DRM 的原則類型。
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993458"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>WMDRMNET \_ 原則 \_ 類型列舉

**WMDRMNET \_ 原則 \_ 類型** 列舉類型會列出可用於網路裝置作業之 Windows Media DRM 的原則類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET \_ 原則 \_ 類型 \_ 未定義**
</dt> <dd>

不支援未定義的原則類型。

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET \_ 原則 \_ 類型 \_ TRANSCRYPTPLAY**
</dt> <dd>

此原則可讓您將受 Windows Media DRM 保護的內容轉換為網路裝置資料的受保護 Windows Media DRM，並在網路裝置上播放。

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
</dt> <dt>

[**WMDRMNET \_ 原則**](wmdrmnet-policy.md)
</dt> </dl>

 

 





