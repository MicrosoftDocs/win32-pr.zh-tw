---
title: 處理來自 SplitButtons 的 BCN_DROPDOWN 通知
description: 本主題說明在對話方塊程式中回應 BCN 下拉式通知的一個可能方法 \_ 。
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093403"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a>如何處理 \_ 分割按鈕的 BCN 下拉式清單通知

本主題說明在對話方塊程式中回應 [BCN \_ 下拉式](bcn-dropdown.md) 通知的一個可能方法。

C + + 應用程式會從通知標頭抓取按鈕的用戶端座標，並將其轉換為螢幕座標。 然後，它會建立快顯功能表，並將其顯示在按鈕的底部。 為了讓範例保持簡單，系統不會針對功能表執行鍵盤快速鍵。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a>步驟1：等候 BCN 的 *\_ 下拉式清單* 通知。


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a>步驟2：取得按鈕的螢幕座標。

您可以使用 [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) 函式，將按鈕左下邊緣的視窗座標轉換成螢幕座標。


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a>步驟3：建立功能表並新增專案。

使用 [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) 函式來建立功能表。 您可以使用 [**AppendMenu**](/windows/desktop/menurc/u) 函式，將專案加入至功能表中。 IDC \_ MENUCOMMAND1 和 idc \_ MENUCOMMAND2 是適用于功能表命令的應用程式定義常數。


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a>步驟4：顯示功能表。

[**Trackpopupmenu 讓**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu)函式會在指定的位置顯示快捷方式功能表，並追蹤功能表上的專案選取專案。


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a>完整範例


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[BCN \_ 下拉式通知碼](bcn-dropdown.md)
</dt> <dt>

[關於按鈕](about-buttons.md)
</dt> <dt>

[按鈕控制項參考](bumper-button-button-control-reference.md)
</dt> <dt>

[使用按鈕](using-buttons.md)
</dt> <dt>

[按鈕](buttons.md)
</dt> </dl>

 

 