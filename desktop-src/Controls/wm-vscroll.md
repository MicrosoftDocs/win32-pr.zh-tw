---
title: 'WM_VSCROLL 訊息 (Winuser .h) '
description: '\_當捲軸事件發生在視窗的標準垂直捲動條時，會將 WM VSCROLL 訊息傳送至視窗。'
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL message Windows 控制項
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106152"
---
# <a name="wm_vscroll-message"></a>WM \_ VSCROLL 訊息

當捲軸事件發生在視窗的標準垂直捲動條時，會將 **WM \_ VSCROLL** 訊息傳送至視窗。 當控制項中發生滾動事件時，此訊息也會傳送給垂直捲動條控制項的擁有者。

視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

如果 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 sb THUMBPOSITION 或 sb THUMBTRACK， [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定捲動方塊的目前位置 \_ \_ ; 否則，就不會使用這個字。

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定捲軸值，指出使用者的滾動要求。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                  | 意義                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ 底部**</dt> </dl>                      | 滾動至右下角。<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> </dl>             | 結束滾動。<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl>                | 向下滾動一行。<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ 系列**</dt> </dl>                      | 向上滾動一行。<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> </dl>                | 向下滾動一個頁面。<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> </dl>                      | 向上滾動一頁。<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> </dl> | 使用者已拖曳捲動方塊 (thumb) 並放開滑鼠按鍵。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))表示捲動方塊在拖曳作業結束時的位置。<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ THUMBTRACK**</dt> </dl>          | 使用者正在拖曳捲軸方塊。 這則訊息會重複傳送，直到使用者放開滑鼠按鍵為止。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))表示捲動方塊拖曳至的位置。<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ TOP**</dt> </dl>                               | 滾動至左上方。<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

如果訊息是由捲軸控制項傳送，這個參數就是捲軸控制項的控制碼。 如果訊息是由標準捲軸傳送，此參數為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

\_當使用者拖曳捲動方塊時，應用程式通常會使用 SB THUMBTRACK 要求碼來提供意見反應。

如果應用程式會滾動視窗的內容，則也必須使用 [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) 函數重設捲動方塊的位置。

請注意， **WM \_ VSCROLL** 訊息只會攜帶16位的捲動方塊位置資料。 因此，僅依賴 **WM \_ VSCROLL** 的應用程式 (，以及用於捲軸位置資料之 [**wm \_ HSCROLL**](wm-hscroll.md)) 的應用程式，其實際最大位置值為65535。

不過，由於 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)、 [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)、 [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)、 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)、 [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)和 [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) 函數支援32位捲軸位置資料，因此可以規避 [**wm \_ HSCROLL**](wm-hscroll.md) 和 **wm \_ VSCROLL** 訊息的16位屏障。 如需技術的說明，請參閱 **GetScrollInfo** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[**WM \_ HSCROLL**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VSCROLL (的)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

