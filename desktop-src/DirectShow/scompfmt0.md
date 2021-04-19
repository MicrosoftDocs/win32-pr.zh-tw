---
description: 包含智慧 recompression 的格式資訊。
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: 'SCompFmt0 結構 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990628"
---
# <a name="scompfmt0-structure"></a>SCompFmt0 結構

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

包含智慧 recompression 的格式資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a>成員

<dl> <dt>

**nFormatId**
</dt> <dd>

保護必須為零。

</dd> <dt>

**MediaType**
</dt> <dd>

[**AM \_描述 \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) 壓縮格式的媒體類型結構。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineGroup::GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




