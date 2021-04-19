---
title: 'DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX 結構 (Wmdrmsdk .h) '
description: DRM \_ 音訊 \_ 輸出 \_ 保護 \_ \_ 識別碼 EX 結構包含音訊輸出保護識別碼的清單。 此結構會藉 \_ \_ \_ \_ 由新增版本號碼來擴充 DRM 音訊輸出保護識別碼。
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991346"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a>DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼 \_ EX 結構

**DRM \_ 音訊 \_ 輸出保護識別碼 \_ \_ \_ EX** 結構包含音訊輸出保護識別碼的清單。 此結構會藉由新增版本號碼來擴充 **DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼** 。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
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

**RgAop** 陣列中的專案數。

</dd> <dt>

**rgAop**
</dt> <dd>

**DRM \_ 音訊 \_ 輸出保護（ \_ \_ 例如** 結構）的陣列。 **DRM \_音訊 \_ 輸出 \_ 保護 \_** （例如）是定義為 [**DRM \_ 輸出 \_ 保護 \_**](drm-output-protection-ex.md)的類型，例如

</dd> </dl>

## <a name="remarks"></a>備註

無。

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

 

 





