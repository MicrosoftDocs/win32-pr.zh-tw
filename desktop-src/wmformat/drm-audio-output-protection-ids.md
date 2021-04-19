---
title: 'DRM_AUDIO_OUTPUT_PROTECTION_IDS 結構 (Wmdrmsdk .h) '
description: DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼結構包含音訊輸出保護識別碼的清單。
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999490"
---
# <a name="drm_audio_output_protection_ids-structure"></a>DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼結構

**DRM \_ 音訊 \_ 輸出 \_ 保護 \_** 識別碼結構包含音訊輸出保護識別碼的清單。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**cEntries**
</dt> <dd>

**RgAop** 陣列中的專案數。

</dd> <dt>

**rgAop**
</dt> <dd>

**DRM \_ 音訊 \_ 輸出 \_ 保護** 結構的陣列。 **DRM \_音訊 \_ 輸出 \_ 保護** 是定義為 [**DRM \_ 輸出 \_ 保護**](drm-output-protection.md)的型別。

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

 

 





