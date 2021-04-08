---
description: FRAMETABLE 結構（框架指標的圓形緩衝區）會傳回到附加至 NPP 之 ITRC 介面的應用程式。
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: 'FRAMETABLE 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112236"
---
# <a name="frametable-structure"></a>FRAMETABLE 結構

**FRAMETABLE** 結構（框架指標的圓形緩衝區）會傳回到附加至 NPP 之 **ITRC** 介面的應用程式。

## <a name="syntax"></a>語法


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**FrameTableLength**
</dt> <dd>

資料表的總長度。

</dd> <dt>

**StartIndex**
</dt> <dd>

資料表中的第一個索引。

</dd> <dt>

**EndIndex**
</dt> <dd>

資料表內的最後一個索引。

</dd> <dt>

**FrameCount**
</dt> <dd>

此資料表所描述的框架數目。

</dd> <dt>

**框架**
</dt> <dd>

實際的框架描述項陣列。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




