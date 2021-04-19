---
description: 當應用程式變更視窗的啟用狀態時傳送。
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: 'WM_ENABLE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985233"
---
# <a name="wm_enable-message"></a>WM \_ 啟用訊息

當應用程式變更視窗的啟用狀態時傳送。 它會傳送至已啟用狀態變更的視窗。 這則訊息會在 [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) 函式傳回之前傳送，但在啟用狀態之後 (視窗的 [**WS \_ 停用**](window-styles.md) 樣式位) 已變更。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出視窗是否已啟用或停用。 如果已啟用視窗，此參數為 **TRUE** ，如果視窗已停用，則為 **FALSE** 。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
