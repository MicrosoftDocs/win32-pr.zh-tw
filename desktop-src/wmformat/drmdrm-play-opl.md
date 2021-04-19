---
title: 'DRM_PLAY_OPL 結構 (Wmdrmsdk .h) '
description: DRM \_ play \_ OPL 結構會保存輸出保護層級的相關資訊， (OPLs) 在播放動作的授權中指定。
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995100"
---
# <a name="drm_play_opl-structure"></a>DRM \_ PLAY \_ OPL 結構

**DRM \_ play \_ OPL** 結構會保存輸出保護層級的相關資訊， (OPLs) 在播放動作的授權中指定。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**minOPL**
</dt> <dd>

[**DRM \_最小 \_ 輸出 \_ 保護 \_ 層級**](drmdrm-minimum-output-protection-levels.md) 結構，包含以不同格式播放內容所需的最小 OPL。

</dd> <dt>

**oplIdReserved**
</dt> <dd>

保留供未來使用。

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_影片 \_ 輸出 \_ 保護 \_**](drmdrm-video-output-protection-ids.md) 識別碼結構，其中包含適用于播放內容的影片輸出保護識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM \_ 複製 \_ OPL**](drmdrm-copy-opl.md)
</dt> <dt>

[**DRM \_ PLAY \_ OPL \_ 例如**](drm-play-opl-ex.md)
</dt> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





