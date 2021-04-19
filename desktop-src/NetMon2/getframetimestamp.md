---
description: GetFrameTimeStamp 函式會傳回指定框架的時間戳記。
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: 'GetFrameTimeStamp 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982456"
---
# <a name="getframetimestamp-function"></a>GetFrameTimeStamp 函式

**GetFrameTimeStamp** 函式會傳回指定框架的時間戳記。

## <a name="syntax"></a>語法


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

框架的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為框架的時間戳記（以微秒為單位）。

如果函式不成功，則傳回值為減去 1 (-1) 。

## <a name="remarks"></a>備註

**GetFrameTimeStamp** 函式會傳回時間戳記，以顯示捕捉程式開始與框架錄製之間經過的時間。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameTimeStamp** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




