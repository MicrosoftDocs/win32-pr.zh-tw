---
description: GetFrameLength 函式會傳回框架的長度。
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: 'GetFrameLength 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2344f2401995af3bac2e8245f48824dfb992076113eb8c27dcb9eff0a54eae04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795700"
---
# <a name="getframelength-function"></a>GetFrameLength 函式

**GetFrameLength** 函式會傳回框架的長度。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetFrameLength(
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

如果函式成功，則傳回值為框架的長度（以位元組為單位）。

如果函式不成功，則傳回值為零。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameLength** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




