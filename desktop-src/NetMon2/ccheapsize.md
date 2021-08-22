---
description: CCHeapSize 函式會傳回 CCHeapAlloc 函數所配置的記憶體大小。
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: 'CCHeapSize 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b086777b571af417662bd60a582fbc53a07c49300d21d2c59b6a36d2247b9d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012304"
---
# <a name="ccheapsize-function"></a>CCHeapSize 函式

**CCHeapSize** 函式會傳回 **CCHeapAlloc** 函數所配置的記憶體大小。

## <a name="syntax"></a>語法


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpMem* 
</dt> <dd>

配置的記憶體之指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為要求的記憶體區塊大小（以位元組為單位）。

如果函式不成功，則傳回值為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SetCCInstPtr](setccinstptr.md)
</dt> <dt>

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> </dl>

 

 




