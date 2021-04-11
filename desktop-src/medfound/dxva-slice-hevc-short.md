---
description: 指定配量控制項資料。
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: 'DXVA_Slice_HEVC_Short 結構 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026039"
---
# <a name="dxva_slice_hevc_short-structure"></a>DXVA 配量 \_ \_ HEVC \_ 簡略結構

指定配量控制項資料。

## <a name="syntax"></a>語法


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a>成員

<dl> <dt>

**BSNALunitDataLocation**
</dt> <dd>

指定 NAL 單位的位置。

</dd> <dt>

**SliceBytesInBuffer**
</dt> <dd>

位流資料緩衝區中與這個配量控制項資料結構相關聯的位元組數目。

</dd> <dt>

**wBadSliceChopping**
</dt> <dd>

如果使用了非主機位流剖析，此值會指出錯誤的配量將切分成，並包含下列其中一個值：



| 需求 | 值 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 值 | 描述                                                                                                                                                                                                                                             |
| 0     | 配量的所有位都位於對應的位流資料緩衝區內。                                                                                                                                                                      |
| 1     | 位流資料緩衝區包含配量的開頭，而不是整個磁區，因為緩衝區已滿。                                                                                                                                        |
| 2     | 位流資料緩衝區包含配量的結尾。 它不會包含配量的起點，因為配量開頭是位於先前的位流資料緩衝區中。                                                                  |
| 3     | 位流資料緩衝區不包含配量的開頭，因為配量的開頭位於先前的位流資料緩衝區，而且不包含配量的結尾，因為目前的位流資料緩衝區也已滿。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**DXVA \_配量 \_ HEVC \_ Short** 包含配量控制項資料，此資料會從主機軟體解碼器傳遞給硬體加速器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎結構](media-foundation-structures.md)
</dt> </dl>

 

 




