---
description: KEYSVC \_ BLOB 結構會定義金鑰服務 blob。 RKeyPFXInstall 函數會使用這個結構。
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: 'KEYSVC_BLOB 結構 (Rkeysvcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992184"
---
# <a name="keysvc_blob-structure"></a>KEYSVC \_ BLOB 結構

**KEYSVC \_ BLOB** 結構會定義金鑰服務 blob。 [**RKeyPFXInstall**](rkeypfxinstall.md)函數會使用這個結構。

## <a name="syntax"></a>語法


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>成員

<dl> <dt>

**Cb**
</dt> <dd>

指定大小（以位元組為單位）的 **ULONG** 值（以 **位元組為單位）。**

</dd> <dt>

**鉛**
</dt> <dd>

包含 BLOB 的 **位元組** 指標，採用 [*PKCS \# 12*](../secgloss/p-gly.md) 格式。

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

[**KEYSVC \_ UNICODE \_ 字串**](keysvc-unicode-string.md)
</dt> </dl>

 

 
