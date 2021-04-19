---
description: 指定未壓縮表面的參考。
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: 'DXVA_PicEntry_HEVC 結構 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966654"
---
# <a name="dxva_picentry_hevc-structure"></a>DXVA \_ PicEntry \_ HEVC 結構

指定未壓縮表面的參考。

## <a name="syntax"></a>語法


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a>成員

<dl> <dt>

**Index7Bits**
</dt> <dd>

識別未壓縮表面的索引。

</dd> <dt>

**AssociatedFlag** 
</dt> <dd>

與介面相關聯的選擇性1位旗標。 旗標的意義取決於內容。 例如，它可以指定參考框架是否為長期參考或短期參考。

</dd> <dt>

**bPicEntry**
</dt> <dd>

存取聯集的整個8位。

</dd> </dl>

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

 

 




