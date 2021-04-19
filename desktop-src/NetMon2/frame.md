---
description: 驅動程式實際的畫面格。
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: '畫面格結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970574"
---
# <a name="frame-structure"></a>框架結構

**框架** 結構是驅動程式的實際畫面。

## <a name="syntax"></a>語法


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a>成員

<dl> <dt>

**時間 戳**
</dt> <dd>

捕捉開始與捕獲框架時間之間的經過時間（以微秒為單位）。

</dd> <dt>

**FrameLength**
</dt> <dd>

MAC 框架長度。

</dd> <dt>

**nBytesAvail**
</dt> <dd>

複製實際的框架長度。

</dd> <dt>

**MacFrame**
</dt> <dd>

框架資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




