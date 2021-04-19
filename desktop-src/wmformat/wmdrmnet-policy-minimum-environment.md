---
title: 'WMDRMNET_POLICY_MINIMUM_ENVIRONMENT 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則的 \_ 最小 \_ 環境結構包含網路裝置的 Windows Media DRM 的最低安全性需求。
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995398"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>WMDRMNET \_ 原則的 \_ 最小 \_ 環境結構

**WMDRMNET \_ 原則的 \_ 最小 \_ 環境** 結構包含網路裝置的 Windows Media DRM 的最低安全性需求。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**wMinimumSecurityLevel**
</dt> <dd>

需要的最小應用程式安全性層級。

</dd> <dt>

**dwMinimumAppRevocationListVersion**
</dt> <dd>

需要最基本的應用程式憑證撤銷清單版本。

</dd> <dt>

**dwMinimumDeviceRevocationListVersion**
</dt> <dd>

需要最小的裝置憑證撤銷清單。

</dd> </dl>

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> <dt>

[**WMDRMNET \_ 原則**](wmdrmnet-policy.md)
</dt> </dl>

 

 





