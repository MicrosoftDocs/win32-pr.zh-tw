---
title: 'WM_MOUSELEAVE 訊息 (Winuser .h) '
description: 當游標離開先前呼叫 TrackMouseEvent 所指定之視窗的工作區時，張貼至視窗。
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- WM_MOUSELEAVE 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464925"
---
# <a name="wm_mouseleave-message"></a>WM \_ MOUSELEAVE 訊息

當游標離開先前呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)所指定之視窗的工作區時，張貼至視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

當產生此訊息時，會取消 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) 要求的所有追蹤。 如果滑鼠需要進一步追蹤滑鼠停留行為，應用程式必須在滑鼠重新進入視窗時呼叫 **TrackMouseEvent** 。

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

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ NCMOUSELEAVE**](wm-ncmouseleave.md)
</dt> <dt>

**概念**
</dt> <dt>

[滑鼠輸入](mouse-input.md)
</dt> </dl>

 

