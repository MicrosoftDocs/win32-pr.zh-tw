---
description: GetCaptureTotalFrames 函式會傳回捕捉中的總畫面數。
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: 'GetCaptureTotalFrames 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2a7cae78dd95521fa80dfd9b9637b332c72ed1c82b90ba1f6c932824181ef565
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910778"
---
# <a name="getcapturetotalframes-function"></a>GetCaptureTotalFrames 函式

**GetCaptureTotalFrames** 函式會傳回捕捉中的總畫面數。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCapture* \[在\]
</dt> <dd>

捕捉的控制碼。 如需取得 capture 控制碼的詳細資訊，請參閱本 **GetCaptureTotalFrames** 主題的「備註」一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是捕捉中的框架總數。

如果函式不成功，則傳回值為0。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureTotalFrames** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




