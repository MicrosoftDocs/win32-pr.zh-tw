---
title: 'WM_CAP_SEQUENCE_NOFILE 訊息 (Vfw .h) '
description: '\_若未將資料寫入檔案，則 [WM CAP \_ 序列 \_ NOFILE] 訊息會起始串流影片捕獲。 您可以使用 capCaptureSequenceNoFile 宏明確地傳送此訊息。'
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a08f470989b8000e9757c1cb81924b875b5303
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093976"
---
# <a name="wm_cap_sequence_nofile-message"></a>WM \_ CAP \_ 序列 \_ NOFILE 訊息

若未將資料寫入檔案，則 [ **WM \_ CAP \_ 序列 \_ NOFILE** ] 訊息會起始串流影片捕獲。 您可以使用 [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) 宏明確地傳送此訊息。


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息適用于結合影片串流或波形音訊串流回呼函式，可讓您的應用程式直接使用影片和音訊資料。

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

 

 





