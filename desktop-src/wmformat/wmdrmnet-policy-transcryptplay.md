---
title: 'WMDRMNET_POLICY_TRANSCRYPTPLAY 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY 結構包含使用 WINDOWS Media DRM 為網路裝置播放內容的原則資訊。
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
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982915"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>WMDRMNET \_ 原則 \_ TRANSCRYPTPLAY 結構

**WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY** 結構包含使用 Windows Media DRM 為網路裝置播放內容的原則資訊。

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

 

 





