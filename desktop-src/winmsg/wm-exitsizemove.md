---
description: 在離開移動或調整大小強制回應迴圈之後，傳送一次至視窗。
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: 'WM_EXITSIZEMOVE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f451e846f2a262a30ccc73121d52c3732dbdfb160fe529535dcf353f077c351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849250"
---
# <a name="wm_exitsizemove-message"></a>WM \_ EXITSIZEMOVE 訊息

在離開移動或調整大小強制回應迴圈之後，傳送一次至視窗。 當使用者按一下視窗的標題列或調整框線，或是當視窗將 [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) 訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，而訊息的 *wParam* 參數指定 **sc \_ MOV** E 或 **sc \_ 大小** 值時，此視窗會進入移動或調整大小的強制回應迴圈。 當 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 傳回時，作業就會完成。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ENTERSIZEMOVE**](wm-entersizemove.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
