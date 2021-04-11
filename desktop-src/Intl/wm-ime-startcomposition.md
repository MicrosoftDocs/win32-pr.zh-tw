---
description: 在輸入法產生組合字元串作為按鍵結果前立即傳送。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: 'WM_IME_STARTCOMPOSITION 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848055"
---
# <a name="wm_ime_startcomposition-message"></a>WM \_ 輸入法 \_ STARTCOMPOSITION 訊息

在輸入法產生組合字元串作為按鍵結果前立即傳送。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a>參數

此訊息沒有任何參數。

<dl></dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

這則訊息是 IME 視窗開啟其撰寫視窗的通知。 如果應用程式顯示覆合字元本身，就應該處理此訊息。

如果應用程式已建立 IME 視窗，則應該將此訊息傳遞至該視窗。 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會藉由將訊息傳遞至預設 IME 視窗來處理訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員訊息](input-method-manager-messages.md)
</dt> </dl>

 

 
