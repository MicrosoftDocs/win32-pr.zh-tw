---
title: 'DRM_PLAY_OPL_EX 結構 (Wmdrmsdk .h) '
description: DRM \_ play \_ OPL \_ EX 結構會保存輸出保護層級的相關資訊， (OPLs) 在播放動作的授權中指定。
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89ca0c6b1cf33a422265fb177e1b1432a52fbd12b3f9fda658125682f3888ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848437"
---
# <a name="drm_play_opl_ex-structure"></a>DRM \_ PLAY \_ OPL \_ EX 結構

**DRM \_ play \_ OPL \_ EX** 結構會保存輸出保護層級的相關資訊， (OPLs) 在播放動作的授權中指定。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

版本號碼。

</dd> <dt>

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

## <a name="remarks"></a>備註

此結構與 **DRM \_ PLAY \_ OPL** 結構相同，不同之處在于它包含版本號碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





