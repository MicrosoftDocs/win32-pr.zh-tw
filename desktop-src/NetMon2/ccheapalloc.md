---
description: CCHeapAlloc 函式會依捕獲來配置記憶體。
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: 'CCHeapAlloc 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849131"
---
# <a name="ccheapalloc-function"></a>CCHeapAlloc 函式

**CCHeapAlloc** 函式會依捕獲來配置記憶體。

## <a name="syntax"></a>語法


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwBytes* 
</dt> <dd>

所配置的記憶體長度。

</dd> <dt>

*bZeroInit* 
</dt> <dd>

配置的記憶體是否已初始化的指標。 如果參數值為 **TRUE**，則配置的記憶體會初始化為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是所配置之記憶體的指標。 當您完成使用已配置的記憶體時，請呼叫 [**CCHeapFree**](ccheapfree.md) 函式來釋放記憶體。

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

[**SetCCInstPtr**](setccinstptr.md)
</dt> <dt>

[**GetCCInstPtr**](getccinstptr.md)
</dt> <dt>

[**CCHeapFree**](ccheapfree.md)
</dt> <dt>

[**CCHeapReAlloc**](ccheaprealloc.md)
</dt> <dt>

[**CCHeapSize**](ccheapsize.md)
</dt> </dl>

 

 




