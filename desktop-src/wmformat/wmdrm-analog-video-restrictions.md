---
title: 'WMDRM_ANALOG_VIDEO_RESTRICTIONS 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 類比 \_ 影片 \_ 限制結構會保存將內容播放為類比影片之限制的相關資訊。
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8221fe325983387107f4e0c03f5672a6762502d8865e1d5895a9e48e96b99d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928808"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>WMDRM \_ 類比 \_ 影片 \_ 限制結構

**WMDRM \_ 類比 \_ 影片 \_ 限制** 結構會保存將內容播放為類比影片之限制的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**guidRestrictionID**
</dt> <dd>

限制識別碼。

</dd> <dt>

**dwRestrictionData**
</dt> <dd>

限制資料。

</dd> </dl>

## <a name="remarks"></a>備註

當您呼叫 [**IWMDRMLicense：： GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md)時，會收到此結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> <dt>

[**WMDRM \_ 類比 \_ 影片 \_ 限制， \_ 例如**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





