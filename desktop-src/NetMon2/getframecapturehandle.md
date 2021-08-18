---
description: GetFrameCaptureHandle 函式會根據指定的框架，傳回捕捉的控制碼。
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: 'GetFrameCaptureHandle 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9e7bf14cd7eae73ac1e5c8e21f8036574628932032a1545f8ac1c653dbbf8adb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910748"
---
# <a name="getframecapturehandle-function"></a>GetFrameCaptureHandle 函式

**GetFrameCaptureHandle** 函式會根據指定的框架，傳回捕捉的控制碼。

## <a name="syntax"></a>語法


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
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

如果函式成功，則傳回值會是捕捉的控制碼。

如果函式不成功，則傳回值為0。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameCaptureHandle** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




