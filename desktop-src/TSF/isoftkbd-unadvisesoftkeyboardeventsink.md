---
title: 'ISoftKbd UnadviseSoftKeyboardEventSink 方法 (Softkbdc .h) '
description: ISoftKbd UnadviseSoftKeyboardEventSink 方法會移除軟鍵盤事件接收器。
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- UnadviseSoftKeyboardEventSink 方法文字服務架構
- UnadviseSoftKeyboardEventSink 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，UnadviseSoftKeyboardEventSink 方法
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90552c09e47d8a51f413f0588b12c8da5d44e665a6a5a51a79dc31717c6d56c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877108"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>ISoftKbd：： UnadviseSoftKeyboardEventSink 方法

**ISoftKbd：： UnadviseSoftKeyboardEventSink** 方法會移除軟鍵盤事件接收器。

## <a name="syntax"></a>語法


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tid* \[在\]
</dt> <dd>

擁有軟鍵盤事件接收器的用戶端識別碼。 此值是在使用 [ISoftKbd：： AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)安裝事件接收器時傳遞。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                                   | 描述                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 此方法成功。<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | *Tid* 參數無效。<br/>                    |
| <dl> <dt>**CONNECT \_ E \_ NOCONNECTION**</dt> </dl> | 找不到 *tid* 所識別的建議接收器。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





