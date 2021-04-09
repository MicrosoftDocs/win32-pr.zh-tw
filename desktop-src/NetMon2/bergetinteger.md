---
description: BERGetInteger 函式會解碼 BER 編碼的整數。
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: 'BERGetInteger 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850911"
---
# <a name="bergetinteger-function"></a>BERGetInteger 函式

**BERGetInteger** 函式會解碼 BER 編碼的整數。

## <a name="syntax"></a>語法


```C++
BOOL BERGetInteger(
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

已解碼之整數的指標。

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

傳回值指標的指標。

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

傳回之標頭長度的指標。

</dd> <dt>

*pDataLength* 
</dt> <dd>

資料長度的指標。

</dd> <dt>

*ppNext* 
</dt> <dd>

指向下一個 BER 專案之指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (也就是，如果找到有效的 BER 編碼整數並轉換) ，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




