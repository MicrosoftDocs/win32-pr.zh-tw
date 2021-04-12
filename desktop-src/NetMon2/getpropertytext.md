---
description: GetPropertyText 函式會傳回屬性文字的指標。
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: 'GetPropertyText 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318076"
---
# <a name="getpropertytext-function"></a>GetPropertyText 函式

**GetPropertyText** 函式會傳回屬性文字的指標。

## <a name="syntax"></a>語法


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

框架的控制碼。

</dd> <dt>

*lpPI* \[在\]
</dt> <dd>

屬性實例的指標。

</dd> <dt>

*szBuffer* \[在\]
</dt> <dd>

屬性文字字串的指標。

</dd> <dt>

*BufferSize* \[在\]
</dt> <dd>

文字字串緩衝區的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為屬性文字的指標。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetPropertyText** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




