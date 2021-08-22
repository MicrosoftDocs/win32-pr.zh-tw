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
ms.openlocfilehash: f02c9cda80acdd42d0687502834a9b2e66f1cf773d02b88eadabdd346850061e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072702"
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

 

 




