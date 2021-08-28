---
title: 'SBM_GETSCROLLINFO 訊息 (Winuser .h) '
description: 傳送 SBM \_ GETSCROLLINFO 訊息以抓取捲軸的參數。
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fde18fe30e9d944e547305094e7ea69e6745d4e1e112d8697367cd82833588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919468"
---
# <a name="sbm_getscrollinfo-message"></a>SBM \_ GETSCROLLINFO 訊息

傳送 **SBM \_ GETSCROLLINFO** 訊息以抓取捲軸的參數。

應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollInfo** 函數才能正常運作。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構的指標。 在呼叫 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)之前，請將結構的 **cbSize** 成員設定為 **sizeof** (**SCROLLINFO**) ，並設定 **fMask** 成員以指定要取出的捲軸參數。 在傳回之前，訊息會將指定的參數複製到結構的適當成員。

**FMask** 成員可以是下列一或多個值。



| 值                                                                                                                                                      | 意義                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**SIF \_ 全部**</dt> </dl>                | SIF \_ 頁面、sif \_ POS、sif \_ 範圍和 sif TRACKPOS 的組合 \_ 。<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**SIF \_ 頁面**</dt> </dl>             | 將滾動頁複製到 nPage 成員。<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ POS**</dt> </dl>                | 將滾動位置複製到 nPos 成員。 <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**SIF \_ 範圍**</dt> </dl>          | 將捲軸範圍複製到 N 每天下限和 N 上限成員。 <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**SIF \_ TRACKPOS**</dt> </dl> | 將目前的捲動方塊追蹤位置複製到 nTrackPos 成員。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息抓取任何值，則傳回值為 **TRUE**;否則為 **FALSE**。

## <a name="remarks"></a>備註

表示捲軸位置、 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**WM \_ VSCROLL**](wm-vscroll.md)的訊息，只提供16個位的位置資料。 但是， **SBM \_ GETSCROLLINFO**、 [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)、 [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)和 [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)所使用的 [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構會提供32位的捲軸位置資料。 您可以在處理 **WM \_ HSCROLL** 或 **WM \_ VSCROLL** 訊息時使用這些訊息和函式，以取得32位捲軸位置資料。

若要取得捲動方塊的32位位置 (\_ 在 [**WM \_ HSCROLL**](wm-hscroll.md)或 [**WM \_ VSCROLL**](wm-vscroll.md)訊息中的 SB THUMBTRACK 要求程式碼期間) ，請在 GETSCROLLINFO 結構的 TRACKPOS 成員中，傳送 **SBM \_ fMask** 與 SCROLLINFO \_ 成員中 [](/windows/win32/api/winuser/ns-winuser-scrollinfo)的 SI光圈值。  訊息會傳回 **SCROLLINFO** 結構之 **nTrackPos** 成員中捲動方塊的追蹤位置。 這可讓您在使用者移動捲動方塊時取得捲動方塊的位置。 或者，您可以使用 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) 函數來取得相同的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

