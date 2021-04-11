---
description: 當視窗即將隱藏或顯示時，傳送至視窗。
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: 'WM_SHOWWINDOW 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319204"
---
# <a name="wm_showwindow-message"></a>WM \_ SHOWWINDOW 訊息

當視窗即將隱藏或顯示時，傳送至視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出是否顯示視窗。 如果 *wParam* 為 **TRUE**，則會顯示視窗。 如果 *wParam* 為 **FALSE**，則會隱藏視窗。

</dd> <dt>

*lParam* 
</dt> <dd>

所顯示視窗的狀態。 如果 *lParam* 為零，則會因為呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函數而傳送訊息;否則， *lParam* 是下列其中一個值。



| 值                                                                                                                                                                                                                         | 意義                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <dt>**SW \_OTHERUNZOOM**</dt> <dt>4</dt> </dl>       | 因為已還原或最小化視窗，所以正在發現視窗。<br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <dt>**SW \_OTHERZOOM**</dt> <dt>2</dt> </dl>             | 視窗正由另一個已最大化的視窗所涵蓋。<br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <dt>**SW \_PARENTCLOSING**</dt> <dt>1</dt> </dl> | 視窗的擁有者視窗會最小化。<br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <dt>**SW \_PARENTOPENING**</dt> <dt>3</dt> </dl> | 正在還原視窗的擁有者視窗。<br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會依訊息的指定，隱藏或顯示視窗。 如果視窗在建立時有 [**WS \_ 可見**](window-styles.md) 的樣式，則視窗會在建立之後，但在顯示之前接收此訊息。 當 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 或 [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) 函式變更其可見度狀態時，視窗也會收到此訊息。

在下列情況下，不會傳送 **WM \_ SHOWWINDOW** 訊息：

-   使用 [**ws \_ 最大化**](window-styles.md) 或 **ws \_ 最小化** 樣式建立最上層的重迭視窗時。
-   在 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)函數的呼叫中指定 **SW \_ SHOWNORMAL** 旗標時。

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

[**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
