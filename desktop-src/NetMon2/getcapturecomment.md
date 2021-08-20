---
description: 傳回捕捉批註的指標。
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: 'GetCaptureComment 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 91f533e92d94329705cb92d876e9ac51a32eb0128000227341b11f6038263ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795771"
---
# <a name="getcapturecomment-function"></a>GetCaptureComment 函式

**GetCaptureComment** 函式會傳回捕捉批註的指標。

## <a name="syntax"></a>語法


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCapture* \[在\]
</dt> <dd>

捕捉的控制碼。 如需取得 capture 控制碼的詳細資訊，請參閱「備註」一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (也就是，如果捕捉包含批註) ，則傳回值會是批註字串的指標。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

請勿變更傳回的批註字串，這是載入的捕獲中的實際批註字串。 任何變更可能會損毀捕捉。 嘗試修改字串會導致存取違規。

您可以透過數種方式取得 capture 的控制碼，視呼叫是由專家或剖析器進行。 對於專家而言，控制碼是在 [EXPERTSTARTUPINFO](expertstartupinfo.md)結構的 **hCapture** 成員中指定的。 若為剖析器，可以藉由呼叫 [GetFrameCaptureHandle](getframecapturehandle.md) 函數來取得 capture 控制碼。

若要從其 capture 檔案取出 capture 的批註，請呼叫 [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) 函數。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureComment** 函數。

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

[EXPERTSTARTUPINFO](expertstartupinfo.md)
</dt> <dt>

[GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)
</dt> <dt>

[GetFrameCaptureHandle](getframecapturehandle.md)
</dt> </dl>

 

 




