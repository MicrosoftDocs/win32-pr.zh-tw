---
description: 當 IME 視窗找不到可延伸組合視窗區域的空間時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: 'WM_IME_COMPOSITIONFULL 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195427"
---
# <a name="wm_ime_compositionfull-message"></a>WM \_ 輸入法 \_ COMPOSITIONFULL 訊息

當 IME 視窗找不到可延伸組合視窗區域的空間時，傳送至應用程式。 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
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

應用程式應該使用 [IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) 命令指定視窗的顯示方式。

IME 視窗（而不是 IME）會透過 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數傳送此通知訊息。

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
</dt> <dt>

[IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md)
</dt> </dl>

 

 
