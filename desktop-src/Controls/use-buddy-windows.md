---
title: 如何使用好友 Windows
description: 藉由將其他控制項設定為標題的合作者視窗，您就可以將這些控制項以標籤的形式自動放置在這些標題的結尾。
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6819e0f37f07a90ae08a623f14c6c26d1d67f55ea81143834dfd10816f74396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829051"
---
# <a name="how-to-use-buddy-windows"></a>如何使用好友 Windows

藉由將其他控制項設定為標題的合作者視窗，您就可以將這些控制項以標籤的形式自動放置在這些標題的結尾。

下圖顯示水準和垂直的橫條，兩者都有靜態控制項做為合作者視窗。

![顯示具有水準橫條和垂直橫條之對話方塊的螢幕擷取畫面](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-buddy-windows"></a>使用好友 Windows

下列程式碼範例會建立如圖所示的好友視窗。


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a>備註

**IDC \_>SLIDER1** 和 **IDC \_ slider2.value** 是 trackbars 在資源編輯器中建立的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 [使用] 控制項](using-trackbar-controls.md)
</dt> </dl>

 

 




