---
title: 'ISoftKbd AdviseSoftKeyboardEventSink 方法 (Softkbdc .h) '
description: ISoftKbd AdviseSoftKeyboardEventSink 方法會安裝一個軟鍵盤事件接收器，以處理來自軟鍵盤的 OnKeySelection 通知。
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- AdviseSoftKeyboardEventSink 方法文字服務架構
- AdviseSoftKeyboardEventSink 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，AdviseSoftKeyboardEventSink 方法
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a3a734e66bb319bb7e24b6ca3b27299f984f33b98772c1cc446c40e3f27426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877985"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>ISoftKbd：： AdviseSoftKeyboardEventSink 方法

**ISoftKbd：： AdviseSoftKeyboardEventSink** 方法會安裝軟鍵盤事件接收器，以處理來自螢幕小鍵盤的 OnKeySelection 通知。

## <a name="syntax"></a>語法


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwKeyboardId* \[在\]
</dt> <dd>

軟鍵盤的識別碼。

</dd> <dt>

*riid* \[在\]
</dt> <dd>

接收介面的介面識別碼。

</dd> <dt>

*punk* \[在\]
</dt> <dd>

由 *riid* 指定之接收器介面的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標。 這個參數不能設定為 **Null**。

</dd> <dt>

*pdwCookie* \[擴展\]
</dt> <dd>

緩衝區的指標，此方法會在其中抓取用來連接至用戶端的軟鍵盤「cookie」。 每個連接的 cookie 都必須是唯一的。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 一或多個參數無效。<br/> |



 

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

[**ISoftKbd::UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

