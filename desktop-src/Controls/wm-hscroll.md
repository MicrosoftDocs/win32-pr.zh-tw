---
title: 'WM_HSCROLL 訊息 (Winuser .h) '
description: '\_當捲軸事件發生在視窗的標準水準捲軸時，會將 WM HSCROLL 訊息傳送至視窗。'
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- WM_HSCROLL message Windows 控制項
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104423"
---
# <a name="wm_hscroll-message"></a>WM \_ HSCROLL 訊息

當捲軸事件發生在視窗的標準水準捲軸時，會將 **WM \_ HSCROLL** 訊息傳送至視窗。 當控制項中發生滾動事件時，此訊息也會傳送給水準捲軸控制項的擁有者。

視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

如果 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 sb THUMBPOSITION 或 sb THUMBTRACK， [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定捲動方塊的目前位置 \_ \_ ; 否則，就不會使用這個字。

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定捲軸值，指出使用者的滾動要求。 這個單字可以是下列其中一個值。



| 值                                                                                                                                                                  | 意義                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> </dl>             | 結束滾動。<br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ 左方**</dt> </dl>                            | 滾動至左上方。<br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ 右邊**</dt> </dl>                         | 滾動至右下角。<br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ LINELEFT**</dt> </dl>                | 向左滾動一個單位。<br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ LINERIGHT**</dt> </dl>             | 向右滾動一個單位。<br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ PAGELEFT**</dt> </dl>                | 以視窗的寬度向左滾動。<br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ PAGERIGHT**</dt> </dl>             | 向右滾動視窗的寬度。<br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> </dl> | 使用者已拖曳捲動方塊 (thumb) 並放開滑鼠按鍵。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))表示捲動方塊在拖曳作業結束時的位置。<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ THUMBTRACK**</dt> </dl>          | 使用者正在拖曳捲軸方塊。 這則訊息會重複傳送，直到使用者放開滑鼠按鍵為止。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))表示捲動方塊拖曳至的位置。<br/> |



 

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

請注意， **WM \_ HSCROLL** 訊息只會攜帶16位的捲動方塊位置資料。 因此，僅依賴 **WM \_ HSCROLL** 的應用程式 (，以及用於捲軸位置資料之 [**wm \_ VSCROLL**](wm-vscroll.md)) 的應用程式，其實際最大位置值為65535。

不過，由於 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)、 [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)、 [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)、 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)、 [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)和 [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) 函數支援32位捲軸位置資料，因此可以規避 **wm \_ HSCROLL** 和 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息的16位屏障。 如需技術的說明，請參閱 **GetScrollInfo** 。

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

[**WM \_ HSCROLL (的)**](wm-hscroll--trackbar-.md)
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll.md)
</dt> </dl>

 

