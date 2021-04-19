---
description: ParserTemporaryLockFrame 函式會在進入剖析器時鎖定框架，並在函式結束剖析器時將框架解除鎖定。
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: 'ParserTemporaryLockFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001424"
---
# <a name="parsertemporarylockframe-function"></a>ParserTemporaryLockFrame 函式

**ParserTemporaryLockFrame** 函式會在進入剖析器時鎖定框架，並在函式結束剖析器時將框架解除鎖定。

## <a name="syntax"></a>語法


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

剖析器所指向框架的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為框架中資料第一個位元組的指標。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

剖析器不應呼叫 **LockFrame** 函數。 如果剖析器接受鎖定，然後產生錯誤或傳回但未解除鎖定框架，則剖析器會讓系統處於無法變更通訊協定或剪下或複製畫面格的狀態。 剖析器應該使用 **ParserTemporaryLockFrame** 函式，此函式只會在函式專案的內容進入剖析器時授與鎖定。 從剖析器結束時，會釋放該框架的鎖定。 因此，只有在剖析器從呼叫 **AttachProperties** 或 **RecognizeFrame** 函式傳回之後，指標才會是有效的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




