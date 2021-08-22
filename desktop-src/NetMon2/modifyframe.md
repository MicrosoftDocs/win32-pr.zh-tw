---
description: ModifyFrame 函式會使用新的資料來改變現有的框架。
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: 'ModifyFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 04bc22af11d83078ecf98d0386b061b520fbf9a8dcab6f6beb360c45b1c6fe96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555818"
---
# <a name="modifyframe-function"></a>ModifyFrame 函式

**ModifyFrame** 函式會使用新的資料來改變現有的框架。

## <a name="syntax"></a>語法


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCapture* \[在\]
</dt> <dd>

捕捉的控制碼。 如需取得 capture 控制碼的詳細資訊，請參閱本 **ModifyFrame** 主題的「備註」一節。

</dd> <dt>

*FrameNumber* \[在\]
</dt> <dd>

框架索引編號。

</dd> <dt>

*FrameData* \[在\]
</dt> <dd>

位元組陣列的指標，其中包含新的框架資料。

</dd> <dt>

*FrameLength* \[在\]
</dt> <dd>

新資料的長度（以位元組為單位）。

</dd> <dt>

*時間戳記* \[擴展\]
</dt> <dd>

指出框架何時修改的時間戳記。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是新框架的控制碼。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

如果呼叫成功， **ModifyFrame** 函式會終結原始框架。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **ModifyFrame** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




