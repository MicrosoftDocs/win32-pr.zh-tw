---
title: 'WM_INITMENU 訊息 (Winuser .h) '
description: 當功能表即將變成作用中時傳送。
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968992"
---
# <a name="wm_initmenu-message"></a>WM \_ INITMENU 訊息

當功能表即將變成作用中時傳送。 當使用者按一下功能表列上的專案，或按下功能表鍵時，就會發生此問題。 這可讓應用程式在功能表顯示前修改功能表。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要初始化之功能表的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

只有在第一次存取功能表時，才會傳送 **wm \_ INITMENU** 訊息; 只會為每個存取產生一個 **wm \_ INITMENU** 訊息。 例如，在按住按鈕時將滑鼠移到數個功能表項目上時，不會產生新的訊息。 **WM \_INITMENU** 不會提供功能表項目的相關資訊。

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

[**WM \_ INITMENUPOPUP**](wm-initmenupopup.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>

 

