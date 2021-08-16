---
title: 'WMDRMNET_POLICY_MINIMUM_ENVIRONMENT 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則的 \_ 最小 \_ 環境結構包含網路裝置 Windows 媒體 DRM 的最低安全性需求。
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
ms.openlocfilehash: 26c11cf02d7cfcd2e3ab62c4e6b110e2c20b77cf6f79251a23f642b38d4df553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027459"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>WMDRMNET \_ 原則的 \_ 最小 \_ 環境結構

**WMDRMNET \_ 原則的 \_ 最小 \_ 環境** 結構包含網路裝置 Windows 媒體 DRM 的最低安全性需求。

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

 

 





