---
description: KEYSVC \_ unicode \_ 字串結構會定義 unicode 字串和字串的最大長度。 RKeyPFXInstall 函數會使用這個結構。
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: 'KEYSVC_UNICODE_STRING 結構 (Rkeysvcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975337"
---
# <a name="keysvc_unicode_string-structure"></a>KEYSVC \_ UNICODE \_ 字串結構

**KEYSVC \_ unicode \_ 字串** 結構會定義 [*unicode*](../secgloss/u-gly.md)字串和字串的最大長度。 [**RKeyPFXInstall**](rkeypfxinstall.md)函數會使用這個結構。

## <a name="syntax"></a>語法


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a>成員

<dl> <dt>

**長度**
</dt> <dd>

**USHORT** 值，指定用於 **緩衝區** 的長度（以位元組為單位）。

</dd> <dt>

**MaximumLength**
</dt> <dd>

**USHORT** 值，指定 **緩衝區** 允許的最大長度（以位元組為單位）。

</dd> <dt>

**Buffer**
</dt> <dd>

表示 Unicode 字串的 **USHORT** 指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Rkeysvcc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**KEYSVC \_ BLOB**](keysvc-blob.md)
</dt> </dl>

 

 
