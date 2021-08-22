---
title: 'WM_CAP_SET_CALLBACK_YIELD 訊息 (Vfw .h) '
description: WM \_ CAP \_ SET \_ 回呼 \_ YIELD 訊息會在應用程式中設定回呼函式。 AVICap 會在串流捕捉期間產生捕捉視窗時呼叫此程式。 您可以使用 capSetCallbackOnYield 宏明確地傳送此訊息。
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee12db79a9e4808442618ca295694611aa9e098a87c8f72b25f04360e156c8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622233"
---
# <a name="wm_cap_set_callback_yield-message"></a>WM \_ CAP \_ 設定 \_ 回呼 \_ 產生訊息

**WM \_ CAP \_ SET \_ 回呼 \_ YIELD** 訊息會在應用程式中設定回呼函式。 AVICap 會在串流捕捉期間產生捕捉視窗時呼叫此程式。 您可以使用 [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Yield 回呼函數的指標，其類型為 [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)。 針對此參數指定 **Null** ，以停用先前安裝的 yield 回呼函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

應用程式可以選擇性地設定 yield 回呼函數。 針對串流捕獲期間所捕獲的每個影片框架，會至少呼叫 yield 回呼函式一次。 如果已安裝 yield 回呼函式，無論 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fYield** 成員狀態為何，都會呼叫它。

如果使用 yield 回呼函式，則必須先安裝它，才能啟動 capture 會話，且必須在會話持續時間內保持啟用狀態。 您可以在串流處理的結束之後停用此功能。

應用程式通常會在包含 [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea)、 [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)、 [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 迴圈的回呼函式中執行某種類型的訊息處理，如同 [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) 函數的訊息迴圈一樣。 Yield 回呼函式也必須篩選和移除可能造成重新進入問題的訊息。

應用程式通常會在 yield 程式中傳回 **TRUE** ，以繼續串流捕捉。 如果 yield 回呼函式傳回 **FALSE**，則捕獲視窗會停止 capture 進程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[影片捕獲訊息](video-capture-messages.md)
</dt> </dl>

 

