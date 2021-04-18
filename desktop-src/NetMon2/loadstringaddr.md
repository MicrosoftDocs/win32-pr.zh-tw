---
description: LoadStringAddr 函式會轉換字串 (例如 &\# 0034; 157.54.32.45&\# 0034; ) 並建立 DWORD 位址。
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: 'LoadStringAddr 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971247"
---
# <a name="loadstringaddr-function"></a>LoadStringAddr 函式

**LoadStringAddr** 函式會轉換字串 (例如 "157.54.32.45" ) 並建立 **DWORD** 位址。

## <a name="syntax"></a>語法


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAddress* 
</dt> <dd>

**DWORD** 的指標。

</dd> <dt>

*str* 
</dt> <dd>

字元字串的指標，其中包含 IP 位址的 x.x.x.x 表示 (例如 127.0.0.1) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 () 中找到位址名稱;傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




