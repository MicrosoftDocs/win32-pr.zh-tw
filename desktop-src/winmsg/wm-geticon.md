---
description: 傳送至視窗，以取得與視窗相關聯之大型或小型圖示的控制碼。 系統會在 ALT + TAB 對話方塊中顯示大型圖示，並在視窗標題中顯示小圖示。
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: 'WM_GETICON 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990335"
---
# <a name="wm_geticon-message"></a>WM \_ GETICON 訊息

傳送至視窗，以取得與視窗相關聯之大型或小型圖示的控制碼。 系統會在 ALT + TAB 對話方塊中顯示大型圖示，並在視窗標題中顯示小圖示。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要抓取的圖示類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                          | 意義                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**圖示 \_BIG**</dt> <dt>1</dt> </dl>          | 取出視窗的大型圖示。<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**圖示 \_小**</dt> <dt>0</dt> </dl>    | 取出視窗的小圖示。<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**圖示 \_SMALL2**</dt> <dt>2</dt> </dl> | 抓取應用程式所提供的小圖示。 如果應用程式不提供，系統就會針對該視窗使用系統產生的圖示。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

要抓取之圖示的 DPI。 這可以用來根據圖示大小提供不同的圖示。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HICON**

傳回值是大型或小型圖示的控制碼，視 *wParam* 的值而定。 當應用程式收到此訊息時，它可以將控制碼傳回至大型或小型圖示，或將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。

## <a name="remarks"></a>備註

當應用程式收到此訊息時，它可以將控制碼傳回至大型或小型圖示，或將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會傳回與視窗相關聯之大型或小型圖示的控制碼，視 *wParam* 的值而定。

沒有圖示的視窗會明確設定 (使用 **WM \_ SETICON**) 使用已註冊視窗類別的圖示，而在此情況下， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會傳回0作為 **wm \_ GETICON** 訊息。 如果將 **WM \_ GETICON** 訊息傳送至視窗會傳回0，接下來請嘗試呼叫視窗的 [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) 函式。 如果傳回0，則嘗試 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) 函數。

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

[**WM \_ SETICON**](wm-seticon.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
