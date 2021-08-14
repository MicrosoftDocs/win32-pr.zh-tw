---
description: CCHeapFree 函式會釋放 CCHeapAlloc 函數所配置的記憶體。
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: 'CCHeapFree 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b29d57c3d56136103fb1948340472343f56727c2df0268a5036dc148fdd0493a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796338"
---
# <a name="ccheapfree-function"></a>CCHeapFree 函式

**CCHeapFree** 函式會釋放 **CCHeapAlloc** 函數所配置的記憶體。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpMem* 
</dt> <dd>

此函式所釋放之記憶體的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 **CCHeapFree** 函數成功，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

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

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




