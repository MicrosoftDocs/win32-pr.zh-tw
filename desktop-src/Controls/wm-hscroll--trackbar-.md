---
title: 'WM_HSCROLL (的)  (Winuser 通知碼) '
description: '\_當滑杆變更位置時，會將 WM HSCROLL 訊息傳送給水準的 [顯示] 控制項的擁有者。 視窗會透過其 WindowProc 函數接收此訊息。'
ms.assetid: EC4AF407-E13F-4562-A0A6-FA109C15101B
keywords:
- WM_HSCROLL (的程式碼段) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 10727b745900520e8af31561236c8e93eeeb3a81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025026"
---
# <a name="wm_hscroll-trackbar-notification-code"></a>WM \_ HSCROLL (的) 通知碼

當滑杆變更位置時，會將 **WM \_ HSCROLL** 訊息傳送給水準的 [顯示] 控制項的擁有者。

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

如果 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 tb THUMBPOSITION 或 tb THUMBTRACK， [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定滑杆的目前位置 \_ \_ 。 若為所有其他通知碼，高序位字是零;傳送 [**TBM \_ GETPOS**](tbm-getpos.md) 訊息來判斷滑杆的位置。

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定通知碼，指出使用者與該使用者的互動。 這個單字可以是下列其中一個值。



| 值                                                                                                                                                                  | 意義                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB \_ 底部**</dt> </dl>                      | 使用者按下 END 鍵 ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)) 。<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TB \_ ENDTRACK**</dt> </dl>                | 這些程式碼段收到了 [**WM 的 \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)，這表示使用者發行了一個已傳送相關虛擬金鑰程式碼的金鑰。 <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**TB \_ LINEDOWN**</dt> </dl>                | 使用者按下向右箭號 ([**VK \_ 右**](/windows/desktop/inputdev/virtual-key-codes)) 或向下箭號 ([**\_ 向下 VK**](/windows/desktop/inputdev/virtual-key-codes)) 按鍵。<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**TB 的 \_ 系列**</dt> </dl>                      | 使用者按下左方箭號 ([**VK \_ 左**](/windows/desktop/inputdev/virtual-key-codes)) 或向上箭號 [**(\_ 向上 VK**](/windows/desktop/inputdev/virtual-key-codes)) 鍵。<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB \_ PAGEDOWN**</dt> </dl>                | 使用者按一下滑杆下方或右邊的頻道 ([**VK \_ 下一個**](/windows/desktop/inputdev/virtual-key-codes)) 。<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TB \_ PAGEUP**</dt> </dl>                      | 使用者按一下滑杆上方或左邊的頻道 ([**VK \_ 之前**](/windows/desktop/inputdev/virtual-key-codes) 的) 。<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TB \_ THUMBPOSITION**</dt> </dl> | 這些程式碼段在 THUMBTRACK 通知碼之後收到了 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) \_ 。<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TB \_ THUMBTRACK**</dt> </dl>          | 使用者拖曳滑杆。<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB \_ TOP**</dt> </dl>                               | 使用者按下 HOME 鍵 ([**VK \_ home**](/windows/desktop/inputdev/virtual-key-codes)) 。 <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[處理] 控制項的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

\_當使用者拖曳捲動方塊時，提供意見反應的應用程式通常會使用 TB THUMBTRACK 程式碼。

請注意， **WM \_ HSCROLL** 訊息只會攜帶16位的位置資料。 因此，僅依賴 **WM \_ HSCROLL** (和 [**wm \_ VSCROLL**](wm-vscroll--trackbar-.md)) 的滑杆位置資料的應用程式，其實際最大位置值為65535。

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

[**WM \_ VSCROLL**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

