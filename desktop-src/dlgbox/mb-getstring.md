---
title: 'MB_GetString 函數 (User .h) '
description: 傳回標準訊息方塊按鈕的字串。
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- MB_GetString 函式對話方塊
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd984a2f65ab8c2eed8a77fffa56af1d94633c828196428a674c9eee78c3ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985358"
---
# <a name="mb_getstring-function"></a>MB \_ GetString 函式

傳回標準訊息方塊按鈕的字串。

## <a name="syntax"></a>語法


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wBtn* 
</dt> <dd>

要傳回的字串識別碼。 這些是由 winuser 中所列的對話方塊命令識別碼值所識別。

</dd> </dl>

## <a name="return-value"></a>傳回值

字串，如果找不到則為 Null。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>使用者。h</dt> </dl>     |
| 程式庫<br/> | <dl> <dt>User32</dt> </dl> |
| DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





