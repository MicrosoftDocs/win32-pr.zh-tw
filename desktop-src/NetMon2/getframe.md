---
description: GetFrame 函式會將控制碼傳回給捕捉內的指定框架。
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: 'GetFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5f6f992c0c61978e2de6f90755852c9e29d6ac51d7ae7f2405ef981ed695c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779248"
---
# <a name="getframe-function"></a>GetFrame 函式

**GetFrame** 函式會將控制碼傳回給捕捉內的指定框架。

## <a name="syntax"></a>語法


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCapture* \[在\]
</dt> <dd>

捕捉的控制碼。 若要取得 capture 控制碼，請呼叫 [GetFrameCaptureHandle](getframecapturehandle.md) 函數。

</dd> <dt>

*FrameNumber* \[在\]
</dt> <dd>

以零為基底的框架)  (數目。 捕捉中第一個框架的數目為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是框架的控制碼。

如果函式不成功 (也就是說，如果 *hCapture* 無效，或框架編號超出範圍) ，則傳回值為 **Null**。

## <a name="remarks"></a>備註

您可以使用 **GetFrame** 函式來取得尋找屬性實例時所需的框架控制碼。 用來尋找屬性實例的函式是 [FindPropertyInstance](findpropertyinstance.md) ，它會找出第一個實例，而 [FindPropertyInstanceRestart](findpropertyinstancerestart.md) 則會尋找下一個實例。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrame** 函數。

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

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




