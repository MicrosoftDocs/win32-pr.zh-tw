---
description: BERGetString 函式會將 BER 編碼的字串解碼。
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: 'BERGetString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849134"
---
# <a name="bergetstring-function"></a>BERGetString 函式

**BERGetString** 函式會將 BER 編碼的字串解碼。

## <a name="syntax"></a>語法


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

已解碼之字串的指標。

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

已解碼之字串指標的指標。

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

傳回之標頭長度的指標。

</dd> <dt>

*pDataLength* 
</dt> <dd>

字串長度的指標。

</dd> <dt>

*ppNext* 
</dt> <dd>

下一個 BER 專案指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (也就是，如果有效的 BER 編碼字串) 解碼，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




