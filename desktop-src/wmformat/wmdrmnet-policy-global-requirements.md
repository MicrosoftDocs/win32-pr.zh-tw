---
title: 'WMDRMNET_POLICY_GLOBAL_REQUIREMENTS 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則的 \_ 全域 \_ 需求結構具有適用于網路裝置之 Windows Media DRM 的全域需求。
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf13c881c9696d970a00ac902f3f8d08f13c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000695"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>WMDRMNET \_ 原則的 \_ 全域 \_ 需求結構

**WMDRMNET \_ 原則的 \_ 全域 \_ 需求** 結構具有適用于網路裝置之 Windows Media DRM 的全域需求。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**MinimumEnvironment**
</dt> <dd>

[**WMDRMNET \_原則 \_ 最小 \_ 環境**](wmdrmnet-policy-minimum-environment.md) 結構，其中包含網路裝置的 Windows Media DRM 的最低安全性需求。

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

 

 





