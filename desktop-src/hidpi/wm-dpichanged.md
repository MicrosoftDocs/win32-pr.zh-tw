---
title: 'WM_DPICHANGED 訊息 (WinUser .h) '
description: 當視窗的有效點 (DPI) 變更時傳送。
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED 訊息高 DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685991"
---
# <a name="wm_dpichanged-message"></a>WM \_ DPICHANGED 訊息

當視窗的有效點 (DPI) 變更時傳送。 DPI 是視窗的縮放因數。 有多個事件可能會造成 DPI 變更。 下列清單指出可能的 DPI 變更原因。

-   視窗會移至具有不同 DPI 的新監視器。
-   主控視窗的監視器 DPI 會變更。

視窗的目前 DPI 永遠等於 **WM \_ DPICHANGED** 所傳送的最後一個 DPI。 這是視窗應該針對感知 DPI 變更的執行緒進行調整的比例因數。


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*WParam* 的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含新的視窗 DPI 的 Y 軸值。 *WParam* 的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含新的視窗 DPI 的 X 軸值。 例如，96、120、144或192。 針對 Windows 應用程式，X 軸和 Y 軸的值是相同的。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/windows/desktop/api/windef/ns-windef-rect)結構的指標，提供針對新的 DPI 縮放的目前視窗的建議大小和位置。 預期應用程式會根據 *lParam* 在處理此訊息時所提供的建議，重新調整視窗的位置並調整其大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

這則訊息只適用于每個監視器感知 **\_ \_ \_ DPI \_ 感知** 應用程式的處理常式，或 **\_ \_ 每個 \_ 監視器 \_ 感知執行緒的 DPI 感知** 。 如果您的最上層視窗或進程以 **DPI** **感知或系統 DPI 感知** 的形式執行，則可能會收到特定 DPI 變更的相關資訊，但在這些情況下，可以放心忽略。 如需不同類型感知的詳細資訊，請參閱 [**處理 \_ DPI \_ 感知**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) 和 [**DPI \_ 感知**](/windows/desktop/api/windef/ne-windef-dpi_awareness)。 舊版 Windows 需要 DPI 感知才能系結至應用程式的層級。 這些應用程式會使用 **進程 \_ DPI \_ 感知**。 目前，DPI 感知系結至執行緒和個別的視窗，而不是整個應用程式。 這些應用程式會使用 **DPI \_ 感知**。

調整您的應用程式時，您只需要使用 X 軸或 Y 軸的值，因為它們是相同的。

為了正確處理此訊息，您將需要根據 *lParam* 和使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)所提供的建議，調整視窗的大小和位置。 如果您沒有這樣做，您的視窗就會隨著新監視器上的其他專案而成長或縮小。 例如，如果使用者使用多個監視器，並將您的視窗從 96 DPI 監視器拖曳至 192 DPI 監視器，則在 192 DPI 監視器上的視窗會顯示為與其他專案很大的一半。

DPI 的基底值定義為 **使用者 \_ 預設 \_ 畫面 \_ DPI** ，其設定為96。 若要判斷監視的縮放比例，請採用 DPI 值，並依 **使用者的 \_ 預設 \_ 螢幕 \_ DPI** 來分割。 下表提供一些範例 DPI 值和相關聯的縮放因數。



| DPI 值 | 調整百分比 |
|-----------|--------------------|
| 96        | 100%               |
| 120       | 125%               |
| 144       | 150%               |
| 192       | 200%               |



 

下列範例提供範例 DPI 變更處理常式。


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



下列程式碼會以線性方式將值從 100% (96 DPI) 調整為 *g \_ DPI* 所定義的任意 DPI。


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



調整值的替代方式是將 DPI 值轉換成縮放比例，然後使用該值。


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>WinUser。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DPI \_ 感知**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**進程 \_ DPI \_ 感知**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

