---
title: 'DRM_VIDEO_OUTPUT_PROTECTION_IDS 結構 (Wmdrmsdk .h) '
description: DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼結構會保存 drm \_ 影片 \_ 輸出 \_ 保護結構的陣列。
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981266"
---
# <a name="drm_video_output_protection_ids-structure"></a>DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼結構

**Drm \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼** 結構會保存 **drm \_ 影片 \_ 輸出 \_ 保護** 結構的陣列。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**cEntries**
</dt> <dd>

**RgVop** 所參考之陣列中的元素數目。

</dd> <dt>

**rgVop**
</dt> <dd>

**DRM \_ 影片 \_ 輸出 \_ 保護** 結構陣列的位址。 **DRM \_影片 \_ 輸出 \_ 保護** 是定義為 [**DRM \_ 輸出 \_ 保護**](drm-output-protection.md)的類型。

</dd> </dl>

## <a name="remarks"></a>備註

此結構會當做 [**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md) 結構的成員使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼， \_ 例如**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





