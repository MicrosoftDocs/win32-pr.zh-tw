---
description: BERGetHeader 函式會解碼 choice 標頭。
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: 'BERGetHeader 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975076"
---
# <a name="bergetheader-function"></a>BERGetHeader 函式

**BERGetHeader** 函式會解碼 choice 標頭。

## <a name="syntax"></a>語法


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

選擇標頭的指標。

</dd> <dt>

*pTag* 
</dt> <dd>

傳回之標記的指標。

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

傳回之標頭長度的指標。

</dd> <dt>

*pDataLength* 
</dt> <dd>

所傳回資料長度的指標。

</dd> <dt>

*ppNext* 
</dt> <dd>

標頭內容的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (也就是，找到有效的 BER choice 標頭，) 傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




