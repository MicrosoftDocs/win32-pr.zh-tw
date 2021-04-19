---
description: VarLenSmallIntToDword 函式會將可變長度的小整數轉換成 DWORD。
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: 'VarLenSmallIntToDword 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974404"
---
# <a name="varlensmallinttodword-function"></a>VarLenSmallIntToDword 函式

**VarLenSmallIntToDword** 函式會將可變長度的小整數轉換成 **DWORD**。

## <a name="syntax"></a>語法


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pValue* 
</dt> <dd>

變數長度、小整數的指標。

</dd> <dt>

*ValueLen* 
</dt> <dd>

長度 (（以位元組為單位）) 可變長度、小整數。

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

指出變數長度小整數是否為位元組交換的旗標。

</dd> <dt>

*lpDword* 
</dt> <dd>

整數轉換成的 **DWORD** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **DWORD** 的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




