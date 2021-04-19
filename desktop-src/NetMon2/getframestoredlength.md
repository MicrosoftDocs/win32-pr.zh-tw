---
description: GetFrameStoredLength 函式會傳回框架的長度。
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: 'GetFrameStoredLength 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985261"
---
# <a name="getframestoredlength-function"></a>GetFrameStoredLength 函式

**GetFrameStoredLength** 函式會傳回框架的長度。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetFrameStoredLength(
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

如果函式成功，則傳回值會是所儲存之框架的長度。

如果函式不成功，則傳回值為零。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameStoredLength** 函數。

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

[GetFrameLength](getframelength.md)
</dt> </dl>

 

 




