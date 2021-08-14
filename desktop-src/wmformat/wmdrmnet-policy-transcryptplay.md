---
title: 'WMDRMNET_POLICY_TRANSCRYPTPLAY 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ policy \_ TRANSCRYPTPLAY 結構包含使用網路裝置 Windows 媒體 DRM 播放內容的原則資訊。
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fe64c796a1f2f15e4733e7dd3d82e918306fb95d78c61fb85ad2d813d946d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195503"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>WMDRMNET \_ 原則 \_ TRANSCRYPTPLAY 結構

**WMDRMNET \_ policy \_ TRANSCRYPTPLAY** 結構包含使用網路裝置 Windows 媒體 DRM 播放內容的原則資訊。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**globals**
</dt> <dd>

全域原則結構。

</dd> <dt>

**playOPLs**
</dt> <dd>

輸出保護層級以供播放。 **WMDRMNET \_原則 \_ 播放 \_ OPL** 是定義為 [**DRM \_ PLAY \_ OPL \_**](drm-play-opl-ex.md)的類型，例如

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

 

 





