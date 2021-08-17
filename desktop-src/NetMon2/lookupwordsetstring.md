---
description: LookupWordSetString 函式會從已標記的集合傳回對應至所要求值的字串。
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: 'LookupWordSetString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 15b529076660eec093df370df47823fb21aa13e53cce61565fe82de7fbb7e017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364716"
---
# <a name="lookupwordsetstring-function"></a>LookupWordSetString 函式

**LookupWordSetString** 函式會從已標記的集合傳回對應至所要求值的字串。

## <a name="syntax"></a>語法


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpSet* 
</dt> <dd>

用來將值的標籤解壓縮的標記集合。

</dd> <dt>

*值* 
</dt> <dd>

已加上標籤之集合的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是對應至所要求值的字串。

如果函式不成功，則指定的值不在集合中，傳回值為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




