---
description: 當使用者要求視窗還原為先前的大小和位置時，傳送至圖示。
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: 'WM_QUERYOPEN 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026767"
---
# <a name="wm_queryopen-message"></a>WM \_ QUERYOPEN 訊息

當使用者要求視窗還原為先前的大小和位置時，傳送至圖示。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_QUERYOPEN                    0x0013
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

如果可以開啟圖示，處理此訊息的應用程式應該會傳回 **TRUE**;否則，它應該會傳回 **FALSE** ，以防止開啟圖示。

## <a name="remarks"></a>備註

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數會傳回 **TRUE**。

處理此訊息時，應用程式不應該執行任何會導致啟用或焦點變更 (例如，建立對話方塊) 的動作。

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

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
