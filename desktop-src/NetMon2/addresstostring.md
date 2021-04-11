---
description: AddressToString 函式會將位址轉換成字串。
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: 'AddressToString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115880"
---
# <a name="addresstostring-function"></a>AddressToString 函式

**AddressToString** 函式會將位址轉換成字串。

## <a name="syntax"></a>語法


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*字串* \[擴展\]
</dt> <dd>

位址轉換成的字串。

</dd> <dt>

*lpAddress* \[在\]
</dt> <dd>

列印的位址。

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



 

 




