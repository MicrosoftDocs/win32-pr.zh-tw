---
description: PROPERTYINSTEX 結構會定義一個自由格式的擴充屬性實例。
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: 'PROPERTYINSTEX 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533169a98d17c56a32df56f77c30d403d0dbb28c6a51159debc9692a505da52b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036968"
---
# <a name="propertyinstex-structure"></a>PROPERTYINSTEX 結構

**PROPERTYINSTEX** 結構會定義一個自由格式的擴充屬性實例。

## <a name="syntax"></a>語法


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a>成員

<dl> <dt>

**長度**
</dt> <dd>

資料的長度（以位元組為單位）。

</dd> <dt>

**LengthEx**
</dt> <dd>

擴充資料的長度。

</dd> <dt>

**lpData**
</dt> <dd>

擴充資料的指標。

</dd> <dt>

**位元組**
</dt> <dd>

**位元組** 資料的指標。

</dd> <dt>

**Word**
</dt> <dd>

**文字** 資料的指標。

</dd> <dt>

**Dword**
</dt> <dd>

**DWORD** 資料的指標。

</dd> <dt>

**LargeInt**
</dt> <dd>

**LARGEINT** 資料的指標。

</dd> <dt>

**SysTime**
</dt> <dd>

**SYSTEMTIME** 資料的指標。

</dd> <dt>

**TypedString**
</dt> <dd>

可能有擴充資料的具類型字串。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




