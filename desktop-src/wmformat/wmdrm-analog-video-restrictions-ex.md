---
title: 'WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 類比 \_ 影片 \_ 限制 \_ EX 結構會保存有關將內容播放為類比影片之限制的延伸資訊。
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9cbacff2d330c869c35eb7a3d1ca46ae6c80a030495ffec42eabc3726436c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006538"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>WMDRM \_ 類比 \_ 影片 \_ 限制 \_ EX 結構

**WMDRM \_ 類比 \_ 影片 \_ 限制 \_ EX** 結構會保存有關將內容播放為類比影片之限制的延伸資訊。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

版本號碼。

</dd> <dt>

**guidRestrictionID**
</dt> <dd>

限制識別碼。

</dd> <dt>

**cbRestrictionData**
</dt> <dd>

限制資料的大小（以位元組為單位）。

</dd> <dt>

**pbRestrictionData**
</dt> <dd>

限制資料。

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

[**WMDRM \_ 類比 \_ 影片 \_ 限制**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





