---
title: 'SBM_SETSCROLLINFO 訊息 (Winuser .h) '
description: 傳送 SBM \_ SETSCROLLINFO 訊息來設定捲軸的參數。
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- SBM_SETSCROLLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968188"
---
# <a name="sbm_setscrollinfo-message"></a>SBM \_ SETSCROLLINFO 訊息

傳送 **SBM \_ SETSCROLLINFO** 訊息來設定捲軸的參數。

應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollInfo** 函數才能正常運作。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定捲軸是否重繪，以反映新的捲動方塊位置。 如果此參數為 **TRUE**，則會重新繪製捲軸。 如果為 **FALSE**，則不會重新繪製捲軸。

</dd> <dt>

*lParam* 
</dt> <dd>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構的指標。 在呼叫 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)之前，請將結構的 **cbSize** 成員設定為 **sizeof** (**SCROLLINFO**) 、設定 **fMask** 成員以指出要設定的參數，並在適當的成員中指定新的參數值。

**FMask** 成員可以是下列一或多個值。



| 值                                                                                                                                                                           | 意義                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <dt>**SIF \_ DISABLENOSCROLL**</dt> </dl> | 除非捲軸的新參數使捲軸不是必要的，否則會停用捲軸，而不是移除它。<br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**SIF \_ 頁面**</dt> </dl>                                  | 將滾動頁設定為 **nPage** 成員中指定的值。<br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ POS**</dt> </dl>                                     | 將滾動位置設定為 **nPos** 成員中指定的值。 <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**SIF \_ 範圍**</dt> </dl>                               | 將捲軸範圍設定為 **n 每天下限** 和 **n 上限** 成員中指定的值。 <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是捲動方塊的目前位置。

## <a name="remarks"></a>備註

表示捲軸位置、 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**WM \_ VSCROLL**](wm-vscroll.md)的訊息，只提供16個位的位置資料。 但是， [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)、 **SBM \_ SETSCROLLINFO**、 [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)和 [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)所使用的 [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構會提供32位的捲軸位置資料。 您可以在處理 **WM \_ HSCROLL** 或 **WM \_ VSCROLL** 訊息時使用這些訊息和函式，以取得32位捲軸位置資料。

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

[**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

