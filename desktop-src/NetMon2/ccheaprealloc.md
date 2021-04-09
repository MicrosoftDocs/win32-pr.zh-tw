---
description: CCHeapReAlloc 函式會重新配置 CCHeapAlloc 函數所配置的記憶體。
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: 'CCHeapReAlloc 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692943"
---
# <a name="ccheaprealloc-function"></a>CCHeapReAlloc 函式

**CCHeapReAlloc** 函式會重新配置 **CCHeapAlloc** 函數所配置的記憶體。

## <a name="syntax"></a>語法


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpMem* 
</dt> <dd>

原始配置記憶體的指標。

</dd> <dt>

*dwBytes* 
</dt> <dd>

重新配置的記憶體大小，以位元組為單位。

</dd> <dt>

*bZeroInit* 
</dt> <dd>

是否已初始化重新配置記憶體的指標。 如果參數值為 **TRUE**，則新重新配置的記憶體會初始化為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是重新配置記憶體的指標。

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

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




