---
title: 'WM_CONTEXTMENU 訊息 (Winuser .h) '
description: 通知視窗，使用者按一下滑鼠右鍵， (以滑鼠右鍵按一下視窗中的) 。
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c036bf0711f208bae25657d572102a7f4d82525076ee1d0b6f4ebd6598e8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472503"
---
# <a name="wm_contextmenu-message"></a>WM \_ CONTEXTMENU 訊息

通知視窗，使用者希望顯示內容功能表。  使用者可能按一下滑鼠右鍵， (在視窗中以滑鼠右鍵按一下) ，按下 Shift + F10 鍵，或按下應用程式鍵 (內容功能表鍵) 可在某些鍵盤上使用。


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

視窗的控制碼，使用者以滑鼠右鍵按一下該視窗。 這可以是接收訊息之視窗的子視窗。 如需有關處理此訊息的詳細資訊，請參閱「備註」一節。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位單字會指定游標在滑鼠按一下時的水準位置（在螢幕座標中）。

高序位單字會指定游標在滑鼠按一下時的垂直位置（以螢幕座標表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

視窗可以藉由使用 [**trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) 或 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) 函數顯示快捷方式功能表來處理此訊息。 若要取得水準和垂直位置，請使用下列程式碼。


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



如果視窗未顯示快捷方式功能表，則應該將此訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。 如果視窗是子視窗， **DefWindowProc** 會將訊息傳送至父視窗。 否則，如果指定的位置是在視窗的標題中， **DefWindowProc** 會顯示預設的快捷方式功能表。

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)會在處理 [**Wm \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)或 [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup)訊息或使用者輸入 SHIFT + F10 時產生 **wm \_ CONTEXTMENU** 訊息。 當使用者按下並釋放 [**VK \_ APPS**](/windows/desktop/inputdev/virtual-key-codes)金鑰時，也會產生 **WM \_ CONTEXTMENU** 訊息。

如果內容功能表是從鍵盤產生的，例如，如果使用者輸入 SHIFT + F10，則 x 和 y 座標為-1，而應用程式應該在目前選取範圍的位置顯示操作功能表，而不是在 (xPos、yPos) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**取得 \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**Trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

