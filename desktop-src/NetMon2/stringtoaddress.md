---
description: StringToAddress 函式會將字串轉換成位址。
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: 'StringToAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbac01f5df9d32a65fe5afb1c1437064f6dd0d4480c95dacd0fe8f7d58e2fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676688"
---
# <a name="stringtoaddress-function"></a>StringToAddress 函式

**StringToAddress** 函式會將字串轉換成位址。

## <a name="syntax"></a>語法


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpAddress* \[擴展\]
</dt> <dd>

字串轉換成的位址指標。

</dd> <dt>

*字串* \[在\]
</dt> <dd>

轉換成位址的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是轉換後字串的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




