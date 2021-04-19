---
description: 在進入移動或調整強制回應迴圈之後，傳送一次至視窗。
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: 'WM_ENTERSIZEMOVE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996838"
---
# <a name="wm_entersizemove-message"></a>WM \_ ENTERSIZEMOVE 訊息

在進入移動或調整強制回應迴圈之後，傳送一次至視窗。 當使用者按一下視窗的標題列或調整框線，或是當視窗將 [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) 訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，而訊息的 *WParam* 參數指定 **sc \_ MOVE** 或 **sc \_ SIZE** 值時，此視窗會進入移動或調整大小的強制回應迴圈。 當 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 傳回時，作業就會完成。

不論是否已啟用完整視窗的拖曳，系統都會傳送 **WM \_ ENTERSIZEMOVE** 訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_ENTERSIZEMOVE                0x0231
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
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ EXITSIZEMOVE**](wm-exitsizemove.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
