---
title: 'DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX 結構 (Wmdrmsdk .h) '
description: DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼 \_ EX 結構包含 drm \_ 影片 \_ 輸出保護結構的陣列 \_ 。
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985536"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼 \_ EX 結構

**Drm \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼 \_ EX** 結構包含 **drm \_ 影片 \_ 輸出 \_ 保護** 結構的陣列。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

版本號碼。

</dd> <dt>

**cEntries**
</dt> <dd>

**RgVop** 所參考之陣列中的元素數目。

</dd> <dt>

**rgVop**
</dt> <dd>

**DRM \_ 影片 \_ 輸出 \_ 保護 \_** 的陣列位址，例如結構。 **DRM \_影片 \_ 輸出 \_ 保護 \_** 範例是定義為 [**DRM \_ 輸出 \_ 保護 \_**](drm-output-protection-ex.md)的類型，例如

</dd> </dl>

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼， \_ 例如**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





