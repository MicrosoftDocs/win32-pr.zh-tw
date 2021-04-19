---
description: 框架 \_ 描述元結構提供有關原始框架的描述性資訊。
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: 'FRAME_DESCRIPTOR 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973419"
---
# <a name="frame_descriptor-structure"></a>框架 \_ 描述元結構

**框架 \_ 描述** 元結構提供有關原始框架的描述性資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a>成員

<dl> <dt>

**FramePointer**
</dt> <dd>

框架資料的指標。

</dd> <dt>

**時間 戳**
</dt> <dd>

畫面格的系統時間（以微秒為單位）。 這段時間通常用來判斷兩個畫面格之間的間隔時間。

</dd> <dt>

**FrameLength**
</dt> <dd>

框架的長度。

</dd> <dt>

**nBytesAvail**
</dt> <dd>

複製實際的框架長度。

</dd> <dt>

**Etype**
</dt> <dd>

Etype 名稱。

</dd> <dt>

**Sap**
</dt> <dd>

SAP 值。

</dd> <dt>

**LowProtocol**
</dt> <dd>

找到的通訊協定索引。

</dd> <dt>

**LowProtocolOffset**
</dt> <dd>

從 **LowProtocol** 取得的通訊協定資料的位移。

</dd> <dt>

**HighPort**
</dt> <dd>

在 **LowProtocol** 中識別的高通訊協定埠。

</dd> <dt>

**HighProtocolOffset**
</dt> <dd>

從 **HighPort** 取得的通訊協定資料的位移。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




