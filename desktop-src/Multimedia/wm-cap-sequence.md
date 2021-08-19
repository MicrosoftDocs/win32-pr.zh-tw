---
title: 'WM_CAP_SEQUENCE 訊息 (Vfw .h) '
description: WM \_ CAP \_ 序列訊息會起始串流影片和音訊捕獲至檔案。 您可以使用 capCaptureSequence 宏明確地傳送此訊息。
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023fd22d79fdfcd1df1f44b2862814ed809fd93c43ab9cd7122414ee1e27db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800263"
---
# <a name="wm_cap_sequence-message"></a>WM \_ CAP \_ 序列訊息

**WM \_ CAP \_ 序列** 訊息會起始串流影片和音訊捕獲至檔案。 您可以使用 [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) 宏明確地傳送此訊息。


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。

## <a name="remarks"></a>備註

如果您想要改變控制串流處理捕獲的參數，請在啟動 capture 之前，先使用 [**WM \_ CAP \_ SET \_ SEQUENCE \_ 安裝程式**](wm-cap-set-sequence-setup.md) 訊息。

根據預設，「捕獲」視窗不允許其他應用程式在捕捉期間繼續執行。 若要覆寫此屬性，請將 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fYield** 成員設為 **TRUE**，或安裝 yield 回呼函數。

在串流處理期間，[捕獲] 視窗可以選擇性地將通知發行至特定類型條件的應用程式。 若要安裝這些通知的回呼程式，請使用下列訊息：

-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態**](wm-cap-set-callback-status.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ YIELD**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ M**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)

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

 

 





